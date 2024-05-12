---
title: Script Constraints, Primary and Foreign Keys for SQL Server Database
date: 2023-04-06
src_link: https://www.notion.so/Script-Constraints-Primary-and-Foreign-Keys-for-SQL-Server-Database-f520c3f6a8eb49f6bf662e9ab954fce4
src_date: '2023-04-06 09:39:00'
gold_link: https://www.mssqltips.com/sqlservertip/3443/script-all-primary-keys-unique-constraints-and-foreign-keys-in-a-sql-server-database-using-tsql/
gold_link_hash: 4adb5beb40af5de8ba3b9bdc39d3b417
tags:
- '#host_www_mssqltips_com'
---


```
--- SCRIPT TO GENERATE THE CREATION SCRIPT OF ALL PK AND UNIQUE CONSTRAINTS.  
declare @SchemaName varchar(100)  
declare @TableName varchar(256)  
declare @IndexName varchar(256)  
declare @ColumnName varchar(100)  
declare @is_unique_constraint varchar(100)  
declare @IndexTypeDesc varchar(100)  
declare @FileGroupName varchar(100)  
declare @is_disabled varchar(100)  
declare @IndexOptions varchar(max)  
declare @IndexColumnId int  
declare @IsDescendingKey int   
declare @IsIncludedColumn int  
declare @TSQLScripCreationIndex varchar(max)  
declare @TSQLScripDisableIndex varchar(max)  
declare @is_primary_key varchar(100)  
declare @PartitionColumn varchar(100)  
  
declare CursorIndex cursor for  
SELECT Schema_name(t.schema_id)             [schema_name],  
       t.NAME,  
       ix.NAME,  
       CASE  
         WHEN ix.is_unique_constraint = 1 THEN ' UNIQUE '  
         ELSE ''  
       END,  
       CASE  
         WHEN ix.is_primary_key = 1 THEN ' PRIMARY KEY '  
         ELSE ''  
       END,  
       ix.type_desc,  
       CASE WHEN ix.is_padded=1 THEN 'PAD_INDEX = ON, ' ELSE 'PAD_INDEX = OFF, ' END + CASE WHEN ix.allow_page_locks=1 THEN 'ALLOW_PAGE_LOCKS = ON, ' ELSE 'ALLOW_PAGE_LOCKS = OFF, ' END + CASE WHEN ix.allow_row_locks=1 THEN 'ALLOW_ROW_LOCKS = ON, ' ELSE 'ALLOW_ROW_LOCKS = OFF, ' END + CASE WHEN Indexproperty(t.object_id, ix.NAME, 'IsStatistics') = 1 THEN 'STATISTICS_NORECOMPUTE = ON, ' ELSE 'STATISTICS_NORECOMPUTE = OFF, ' END + CASE WHEN ix.ignore_dup_key=1 THEN 'IGNORE_DUP_KEY = ON, ' ELSE 'IGNORE_DUP_KEY = OFF, ' END  
       + 'SORT_IN_TEMPDB = OFF, FILLFACTOR ='  
       + Cast(ix.fill_factor AS VARCHAR(3)) AS IndexOptions,  
       ds.NAME                              FileGroupName,  
       CASE  
         WHEN ds.type_desc = 'PARTITION_SCHEME' THEN (SELECT c.NAME  
                                                        FROM sys.index_columns ic  
                                                             INNER JOIN sys.columns c  
                                                                     ON c.object_id = ix.object_id  
                                                                        AND c.column_id = ic.column_id  
                                                       WHERE ic.partition_ordinal = 1  
                                                         AND ic.index_id = ix.index_id  
                                                         AND ic.object_id = ix.object_id)  
         ELSE NULL  
       END                                  partition_column  
  FROM sys.tables t  
       INNER JOIN sys.indexes ix  
               ON t.object_id = ix.object_id  
       LEFT JOIN sys.data_spaces ds  
              ON ds.data_space_id = ix.data_space_id  
 WHERE 1 = 1  
   AND ix.type > 0  
   AND ( ix.is_primary_key = 1  
          OR ix.is_unique_constraint = 1 ) --and schema_name(tb.schema_id)= @SchemaName and tb.name=@TableName  
   AND t.is_ms_shipped = 0  
   AND t.NAME <> 'sysdiagrams'  
 ORDER BY Schema_name(t.schema_id),  
          t.NAME,  
          ix.NAME    
  
open CursorIndex  
fetch next from CursorIndex into  @SchemaName, @TableName, @IndexName, @is_unique_constraint, @is_primary_key, @IndexTypeDesc, @IndexOptions, @FileGroupName, @PartitionColumn  
while (@@fetch_status=0)  
begin  
   declare @IndexColumns varchar(max)  
   declare @IncludedColumns varchar(max)  
   set @IndexColumns=''  
   set @IncludedColumns=''  
   declare CursorIndexColumn cursor for   
   select col.name, ixc.is_descending_key, ixc.is_included_column  
     from sys.tables             tb  
    inner join sys.indexes       ix  on tb.object_id  = ix.object_id  
    inner join sys.index_columns ixc on ix.object_id  = ixc.object_id and ix.index_id   = ixc.index_id  
    inner join sys.columns       col on ixc.object_id = col.object_id and ixc.column_id = col.column_id  
   where ix.type>0 and (ix.is_primary_key=1 or ix.is_unique_constraint=1)  
     and schema_name(tb.schema_id)=@SchemaName and tb.name=@TableName and ix.name=@IndexName  
    order by ixc.index_column_id  
   open CursorIndexColumn   
   fetch next from CursorIndexColumn into  @ColumnName, @IsDescendingKey, @IsIncludedColumn  
   while (@@fetch_status=0)  
   begin  
    if @IsIncludedColumn=0   
      set @IndexColumns=@IndexColumns + @ColumnName  + case when @IsDescendingKey=1  then ' DESC, ' else  ' ASC, ' end  
    else   
     set @IncludedColumns=@IncludedColumns  + @ColumnName  +', '   
         
    fetch next from CursorIndexColumn into @ColumnName, @IsDescendingKey, @IsIncludedColumn  
   end  
   close CursorIndexColumn  
   deallocate CursorIndexColumn  
   set @IndexColumns = substring(@IndexColumns, 1, len(@IndexColumns)-1)  
   set @IncludedColumns = case when len(@IncludedColumns) >0 then substring(@IncludedColumns, 1, len(@IncludedColumns)-1) else '' end  
  --  print @IndexColumns  
  --  print @IncludedColumns  
    
  set @TSQLScripCreationIndex =''  
  set @TSQLScripDisableIndex =''  
  set  @TSQLScripCreationIndex='ALTER TABLE '+  QUOTENAME(@SchemaName) +'.'+ QUOTENAME(@TableName)+ ' ADD CONSTRAINT ' +  QUOTENAME(@IndexName) + @is_unique_constraint + @is_primary_key + +@IndexTypeDesc +  '('+@IndexColumns+') '+   
   case when len(@IncludedColumns)>0 then CHAR(13) +'INCLUDE (' + @IncludedColumns+ ')' else '' end + CHAR(13)+'WITH (' + @IndexOptions+ ') ON ' + concat(QUOTENAME(@FileGroupName), '(' + @PartitionColumn + ')')  + ';'    
    
  print @TSQLScripCreationIndex  
  print @TSQLScripDisableIndex  
  
fetch next from CursorIndex into  @SchemaName, @TableName, @IndexName, @is_unique_constraint, @is_primary_key, @IndexTypeDesc, @IndexOptions, @FileGroupName, @PartitionColumn  
  
end  
close CursorIndex  
deallocate CursorIndex  
  
  

```