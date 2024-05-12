---
title: Dashboard and workflow for Obsidian at work (sales) - Share & showcase - Obsidian
  Forum
date: 2022-12-11
src_link: https://www.notion.so/Dashboard-and-workflow-for-Obsidian-at-work-sales-Share-showcase-Obsidian-Forum-da09c74c580441619c3d095def0aabee
src_date: '2022-12-11 18:12:00'
gold_link: https://forum.obsidian.md/t/dashboard-and-workflow-for-obsidian-at-work-sales/34794
gold_link_hash: 68aacb84dbbb50ddb0cf5f8c3e11065d
tags:
- '#host_forum_obsidian_md'
---


[Gnopps](https://forum.obsidian.md/u/Gnopps)

 March 28, 2022, 9:45am
 
1

I’ve been using my setup for working with customers and projects in Obsidian for a while, and thought I wanted to share how Obsidian can be used in a work environment. It uses templates and scripts a lot to automate processes.


My work is within sales, and so I have many customer meetings as well as customer projects I’m working on. The reason for posting here is for other people finding inspiration on how to setup their own systems, with every use case of course being unique. This is what works in my worklife, maybe some parts of it will be useful to you as well ![](https://forum.obsidian.md/images/emoji/apple/slight_smile.png?v=12 ":slight_smile:")


A sample vault [can be downloaded here](https://github.com/Gnopps/ObsidianScripts/blob/main/VaultToShare.zip). Please read the note “README FIRST” in it.


Below I first show how I work with Obsidian, then how it has been implemented.


Most notes are just typed on the go, such as knowledge I want to save into Obsidian. But the system has the below recurring note types.


This is the page I go to whenever I’m not actively working on a task. It lists all the things I need to do, things I need to be aware of and provides quick links to active projects.


It contains the following components:


1. **Must do today**: Tasks with a hard due-date of today or earlier.
2. **Meetings**: Upcoming meetings today, or past meetings where I haven’t reviewed the notes yet.
3. **Inbox**: Tasks I need to assign a date to. All tasks must have either a due-date (external due date that can’t be missed) or a scheduled-date (date by wish I’d like to complete it).
4. **Try to do today**: Tasks with a scheduled date of today or earlier, i.e. no hard due date but would be good to get done
5. **Upcoming**: Tasks with a hard due-date in the next days. I check this to see that I have enough time to complete them, and to see on Fridays that there are no tasks with due-dates over the weekend
6. **Pomodoros / Tasks completed**: Separate lines for cumulative number of pomodoros (red) and tasks (blue) I’ve completed during the last week. Depending on the number of meetings this is a very uneven figure, but I try to keep it above 10 for the last 7 days. There is a green line always showing where 10 is, so I know if I am above or below my target.
7. **All todos**: Expandable menu that shows all todos I have, i.e. those with due- or scheduled-date further on in the future
8. **Recent cases**: A list of all customer cases I have touched in the last 14 days. I use it to quickly access customers, as well as to be able to review what I’ve been working on.
9. **Recent files**. Just shows recent files for quick access
10. **File manager**: Tree-view of files, I use this to check my inbox
11. **Linked mentions**: We all know this one I hope ![](https://forum.obsidian.md/images/emoji/apple/slight_smile.png?v=12 ":slight_smile:")


Here is the page when you expand “All todos”:  




Each customer has its own note with the most needed information about the customer. The page pulls in tasks and meeting notes so that I can search everything related to this customer in one page.


The sections here are


1. **General**: Shows meta-data used by dataview. These 3 fields are in a separate section as they are pretty static for the whole customer projects
2. **Info**: Here I add important links for the project, as well as things I learn about the customer.
3. **Todos**: Pulls in todos from this particular note as well as from all meetings relating to this customer.
4. **Activities**: Every time I do something relating to a customer, I note it on the customer’s page, under a bullet point with today’s date. Here I also add general tasks relating to this customer.
5. **Meetings**: All meetings about or with this customer, transcluded to easily search their contents in one place.


For every meeting I create a standard template. The template automatically inserts the meeting date into metadata and note title, along with customer name in note title. I copy agenda from the meeting invite, and add all attendees (for future reference).


Recurring meetings (for example with my manager) have a file that rolls them all up into that file and then I create a separate note with that file as project for every separate meeting.


My daily notes are mainly used for everything that is not related to customer cases.


I use these parts for it:


1. **Activity**: Things I’ve done today that I wish to remember
2. **Learnings**: My job involves plenty of knowledge required and I try to keep all knowledge I need to know in Obsidian. Often I will just put a link to the topic itself and add the new knowledge there.
3. **New cases**: Whenever I’m assigned a new customer I make a note of how and create the link to the customer page here
4. **Todos**: All tasks I have to do that are not related to a customer I add under the daily note (or meeting note if occur in a meeting)
5. **Pomodoros / Tasks done**: Automatically added by the pomodoro and rewarder plugins.


I would like to add plenty of notes around the people I interact with, as my memory struggles to keep up. However I often share my screen and then it can look kind of bad when I’ve made so many notes about people, thus I keep this as a very simple reference only (this might change in the future).


[Dashboard.md](https://github.com/Gnopps/ObsidianScripts/blob/main/Dashboard)



The sections are done by using admonitions. Within each section I setup the columns using CSS. The data comes from Obsidian tasks, Dataview and Obsidian tracker. I’ve styled the tasks in my own way both using CSS as well as a minor hardcode-change in the tasks plugin itself (to style backlinks in tasks differently). I won’t explain how to do this hardcode-change as it can break stuff and if you know what to do then you’re able to do this yourself ![](https://forum.obsidian.md/images/emoji/apple/slight_smile.png?v=12 ":slight_smile:")


I have a hotkey (Ctrl D) that opens the dashboard in reading mode.

Whenever I get a new customer assigned I create an empty note and run a hotkey (Ctrl -) that executes this QuickAdd-macro.


The macro first inserts [this template](https://github.com/Gnopps/ObsidianScripts/blob/main/New%20case%20template) and then [this script](https://github.com/Gnopps/ObsidianScripts/blob/main/SetupNewCustomer.js).



The template adds the sections, tasks and dataview-rollups as well as link to the customer logo.


The script creates a new folder for the customer, as well as a folder with customer files, and then moves the note to the newly created folder. Finally it opens Google image search to search for the customer logo. I save the logo to the logo-folder and then run [PowerToys](https://github.com/microsoft/PowerToys) image resizer to make sure the image is within size limits to look good with dataview.

PowerToys resizer:  

![](https://forum.obsidian.md/uploads/default/original/3X/d/3/d3e64b9700467bd7846ee09b16e0ed33148cdb60.png)


New meetings are created through backlinks or simply be creating a new note. I then run a hotkey (Ctrl M) to execute [this QuickAdd macro script](https://github.com/Gnopps/ObsidianScripts/blob/main/AskForDateForMeeting.js). The script will ask for the meeting date (e.g. “25mar”) and then insert that date into the meeting note and the note title. The scripts also asks for the customer or project and inserts that into the note. The script then runs another QuickAdd-command that inserts [the meeting-template](https://github.com/Gnopps/ObsidianScripts/blob/main/New%20meeting%20template%20for%20QuickAdd) along with a task with due-date day before meeting to prepare for the meeting.



To get attendees for the meeting I use [this excellent Outlook-script](https://www.zsolt.blog/2020/12/my-GTD-Meetings-and-ToDo-in-Roam.html#outlookscript) that I modified slightly.


Files I create for the meeting or need to have available I store in the “Files”-folder and link to in the meeting note, using Obsidian’s linking availability (i.e. not external link). For this to work you must enable Obsidian to show all files, not just compatible files.


Once the meeting is finished and I have reviewed the notes, I click the *Finish meeting*-button. This button runs [this QuickAdd-script](https://github.com/Gnopps/ObsidianScripts/blob/main/FinishMeeting.js) that changes the tags to go from #future to #held, and then moves the note to the customer folder. This way the meeting is no longer shown in my dashboard.

My daily notes template is very simple and just inserts the headings. It is accessed using a shortcut (Ctrl Space).



One thing to note is that whenever I have an e-mail I wish to quickly access I simply drag it from Outlook to Obsidian (and remove the automatically inserted exclamation-mark), it then becomes clickable there so I don’t have to look it up in Outlook when I want to answer. Many tasks thus are “Answer email” with an indendet bullet point below with the message itself.

All people I interact with get their own page. Whenever I noticed that a person hasn’t been assigned an employer I open the person page and click my shortcut (Ctrl R). The shortcut will launch [this QuickAdd-script](https://github.com/Gnopps/ObsidianScripts/blob/main/CRM_Macro.js) that asks for the employer and inserts that. If the employer is the same as mine then a tag #Colleague is inserted, otherwise #Customer is inserted. The note is then moved to my CRM-folder.


I use a pretty flat structure, and only use a limited set of tags. I access my notes mainly through the quick-switcher or search/linking. The folders I use are:


* **\_Inbox**: All new notes end up here and are moved either by my scripts or by myself manually.
* **Customers**: All customer notes are in this main folder. Below it a folder with the customer name is created, and within that folder a “Files”-folder is created. The customer folder has all the notes and the Files-folder has all attachments and files I’m working on for this customer.
* **CRM**: Contains all my People-notes.
* **Daily\_notes**: Contains all my daily notes.
* **Files**: Contains all attachments
* **Logos**: Contains customer logos
* **Scripts**, **Templates**: Self-explanatory


All other notes (not customer-related) are stored at root level.


I tried many themes but eventually settled for [Primary theme](https://github.com/ceciliamay/obsidianmd-theme-primary), because I like the way it transcludes notes - making every transcluded note visible as transcluded. This makes the customer pages easier to read. I also like its use of colours for headings.


* **[Dashboard.css](https://github.com/Gnopps/ObsidianScripts/blob/main/Dashboard.css)**: Adjusts how tasks are displayed on the dashboard (more compact). It also enables column-view for the dashboard and tries to remove some whitespaces.
* **[Dataview.css](https://github.com/Gnopps/ObsidianScripts/blob/main/Dataview.css)**: Adds a line between rows in dataview.
* **[Use full length for note.css](https://github.com/Gnopps/ObsidianScripts/blob/main/Use%20full%20length%20for%20note.css)**: For my notes I prefer to have a limited width for easier reading as default, this makes it possible to utilise full width for specifc notes.


* **[Admonition](https://github.com/valentine195/obsidian-admonition)**: Though this is nowadays included in Obsidian, I keep the plugin to be able to put code within the admonition.
* **[Advanced tables](https://github.com/tgrosinger/advanced-tables-obsidian)**: Makes working with tables a lot easier.
* **[Another quick switcher](https://github.com/tadashi-aikawa/obsidian-another-quick-switcher/)**: Allows me to use diacritics when opening notes (i.e. I can type “ö” and it will search for “ø”), along with other benefits.
* **[Auto note mover](https://github.com/farux/obsidian-auto-note-mover)**: Automatically moves notes I tag with #CRM to the CRM-folder (simply because I installed it before I started writing the QuickAdd-scripts).
* **[Buttons](https://github.com/shabegom/buttons)**: To be able to have the “Finish meeting”-button for my meetings
* **[Calendar](https://github.com/liamcain/obsidian-calendar-plugin)**: To have a small calender always visible in the bottom right corner
* **[Contextual typography](https://github.com/mgmeyers/obsidian-contextual-typography)**: To make more styling possible
* **[Dataview](https://github.com/blacksmithgu/obsidian-dataview/)**: To be able to show customers on dashboard, and meetings on the customer pages.
* **[Excel to markdown table](https://github.com/ganesshkumar/obsidian-excel-to-markdown-table)**: Makes it easier to paste tables into notes.
* **[File path to URI](https://github.com/MichalBures/obsidian-file-path-to-uri)**: Allows me to paste links to local files in markdown-format instead of Windows-format.
* **[Hider](https://github.com/kepano/obsidian-hider)**: Hides metadata in reading view.
* **[Homepage](https://github.com/Rainbell129/Obsidian-Homepage)**: Always launches Obsidian with my dashboard as the start page.
* **[LanguageTool Integration](https://github.com/Clemens-E/obsidian-languagetool-plugin)**: To check my spelling
* **[MetaEdit](https://github.com/chhoumann/MetaEdit)**: Used by my QuickAdd-scripts to edit notes.
* **[Natural Language Dates](https://github.com/argenos/nldates-obsidian)**: Allows me to type “@today” for example to insert today’s date
* **[Obsidian Rewarder](https://github.com/Gnopps/obsidian-rewarder)**: Used for logging of completed tasks. Can also be used for getting rewards upon completing tasks. Developed by myself.
* **[QuickAdd](https://github.com/chhoumann/quickadd)**: Allows me to run various scripts on notes to automate processes
* **[Recent files](https://github.com/tgrosinger/recent-files-obsidian)**: Shows recent files I’ve been working on in a separate pane.
* **[Sortable](https://github.com/alexandru-dinu/obsidian-sortable)**: Allows me to sort dataview-tables.
* **[Status bar pomodoro timer](https://github.com/kzhovn/statusbar-pomo-obsidian)**: Logs my pomodoros
* **[Style settings](https://github.com/mgmeyers/obsidian-style-settings)**: Allows some customisation of the theme
* **[Supercharged links](https://github.com/mdelobelle/obsidian_supercharged_links)**: Adds an emoji to all my coworkers and another emoji for employees of customers that I interact with.


The setup looks like this:
* **[Tasks](https://github.com/schemar/obsidian-tasks)**: Allows rollups of all tasks I work on.
* **[Templater](https://github.com/SilentVoid13/Templater)**: Let’s me insert templates with for example today’s date automatically.
* **[Tracker](https://github.com/pyrochlore/obsidian-tracker)**: Shows the pomodo-chart on the dashboard.


I’m not using live preview at all, as I find it difficult and it can make navigation messy when you are using dataview and tasks.


Please remember that Obsidian [is not free](https://obsidian.md/pricing) when you use it in a professional context. Also sending a donation to the creators of themes and plugins is a good practice.


Some inspiration came from [this post](https://forum.obsidian.md/t/dashboard-a-simple-organization-and-navigation-method-for-obsidian-vaults/33197), thank you! Also thanks to the various people who have created the themes, plugins, Outlook-scripts, Obsidian and shared their workflows/setups for inspiration.


I am of course glad to hear your comments and ideas!


Repository and example vault updated with the below changes.


* Dashboard chart now shows completed tasks as well as completed todos.
* Dashboard chart now has a green line showing aspiration, by default set to 10 (i.e. try to do more than 10 tasks & pomodoros each over the last weeek)
* Dashboard list of active cases now shows last update based on when last meeting was held, last page in same folder was updated or page itself was updated. Previously listed last update based on the page itself only.
* Dashboard list of all due tasks now has no limit, useful if you need to check upcoming duedates over a longer period.
* Daily notes now show completed tasks (using my own plugin Obsidian Rewarder)
* Removed emojis from file paths as some syncing services unable to handle them



54 Likes
[Laboratory Notebook & Integrated Task Management System for Bench Scientists](https://forum.obsidian.md/t/laboratory-notebook-integrated-task-management-system-for-bench-scientists/45338)
[a\_wue](https://forum.obsidian.md/u/a_wue)

 March 28, 2022, 10:45am
 
2
Wow, thanks for sharing! Very generous.


1 Like
[Chrisg](https://forum.obsidian.md/u/Chrisg)

 April 5, 2022, 3:40am
 
3
Really nice. Any chance you have an example vault to play with


[Gnopps](https://forum.obsidian.md/u/Gnopps)

 April 5, 2022, 6:25am
 
5
Good idea and [added here](https://github.com/Gnopps/ObsidianScripts/blob/main/VaultToShare.zip).


3 Likes
[Chrisg](https://forum.obsidian.md/u/Chrisg)

 April 6, 2022, 9:16pm
 
6
Just playing with it now. Thanks


[liuyxpp](https://forum.obsidian.md/u/liuyxpp)

 May 25, 2022, 2:25am
 
7
Very inspiring. Thank you!


[PencilMing](https://forum.obsidian.md/u/PencilMing)

 May 31, 2022, 5:42pm
 
8
It looks nice and is very inspiring. Thanks.


[Gnopps](https://forum.obsidian.md/u/Gnopps)

 June 3, 2022, 10:09am
 
9
Thank for your kind words! I’ve improved some parts and will try to get the example vault updated.


[HermannW](https://forum.obsidian.md/u/HermannW)

 June 22, 2022, 3:29pm
 
10
First of all, thank you very, very much for sharing this. It’s invaluable for me as an Obsidian beginner to have somethingh like this.



I only discovered Obsidian a few weeks ago and I am still trying to understand everything. For instance I tried to modify one of the templates but I noticed that the modifications are not applied. For instance I replaced “Preparation” in the “New meeting template” with “Time”. But when I create a new meeting, it still shows Preparation. I even deleted the template file and I could still create a new meeting.


On the other hand, I had to remove the icons from the CRM and Customer folder because Dropbox wouldn’t synch those folders. When I create a new Daily note, I get a message that <icon> Customer folder does not exist.


Can anyone please point me in the right direction how to fix these?


1 Like
[scholarInTraining](https://forum.obsidian.md/u/scholarInTraining)

 June 22, 2022, 6:09pm
 
11
Check what folder your templating system’s settings tab is using to find its templates. (I think the example vault uses Templater, so check for a settings tab with that name, towards the bottom of the list of settings pages.) Double-check that the meeting note template you were adjusting was in that folder? Your daily note template should also be in there: check for any mentions of your renamed customer folder, including inside code blocks!


Someone who knows this vault could give you more precise advice on what to change, but if you want to get started here are some suggestions for finding other things you need tp change:


* You’ll also need to change the name of the Customers folder in some of the JS scripts - I just randomly looked at “FinishMeeting.js” and it uses the emoji version of the Customers folder name. You’ll need to open the JS files in some other text editor; they won’t open in Obsidian.
* Finally, in the QuickAdd settings tab, you might need to change folder names in some of the individual QuickAdd actions. Even without knowing what precisely anything is doing, it should be easy to look through for the changed folder name and remove the emoji. Look for gear buttons in the list of actions, then also click Manage Macros, the Configure button on each macro, and look for gear buttons in the lists there.


[HermannW](https://forum.obsidian.md/u/HermannW)

 June 22, 2022, 6:18pm
 
12
Thanks for the quick answer! I’ll give it try and see what comes up… ![](https://forum.obsidian.md/images/emoji/apple/slight_smile.png?v=12 ":slight_smile:")


1 Like
[Gnopps](https://forum.obsidian.md/u/Gnopps)

 June 30, 2022, 1:56pm
 
13
Thanks for your answers [@HermannW](/u/hermannw) and [@scholarInTraining](/u/scholarintraining). Did you get it sorted [@HermannW](/u/hermannw)?


I’ve now updated the sample vault to be without the emojis in the file structure as that messed up some syncing services. Also other changes as outlined in the first post.


1 Like
[HermannW](https://forum.obsidian.md/u/HermannW)

 July 6, 2022, 11:48pm
 
14
Yes, [@Gnopps](/u/gnopps) I did sort it out and made some more changes to fit my purpose. I will check out your modifications because I noticed that the tasks are not shown correctly in the Dashboard.



Thanks again for sharing!


[concentration](https://forum.obsidian.md/u/concentration)

 July 9, 2022, 7:20pm
 
15
Emailed the sample vault to myself and got:


– 1 attachment contains a virus or blocked file. Downloading this attachment is disabled.


[Gnopps](https://forum.obsidian.md/u/Gnopps)

 July 9, 2022, 7:40pm
 
16
That is odd, I would guess it is one of the script files that is interpreted as a virus as the script makes changes to your files. I’ve got anti-virus installed on my computer and have not gotten anything.


Would you have a more detailed error report?


[concentration](https://forum.obsidian.md/u/concentration)

 July 9, 2022, 8:23pm
 
17
That’s about all the details Gmail gives. On a Mac so don’t have a regular antivirus installed. Could be that, just letting you know.


[Gnopps](https://forum.obsidian.md/u/Gnopps)

 July 10, 2022, 6:38am
 
18
Found the problem now: It is not a virus but the problem is with Gmail that automatically blocks any script files as attachment. See screenshot with their own explanation below:


As a side note, I’ve been using Fastmail instead of Gmail since many years and can highly recommend it (just tried, and there you are allowed to attach .js-files). Here is a [referral link](https://ref.fm/u14512137) or click here for [non-referral link](https://www.fastmail.com).


1 Like
[Glowgal](https://forum.obsidian.md/u/Glowgal)

 July 14, 2022, 6:47am
 
19
**This**is what I’ve been looking for aaaalllll my life!



(Allow me the poetic license to Express out my gratitude?)


Hey,Gnopps?Thanks for sharing in such detail. Am lost no more. Will use your example vault,hope you updated it. Will let you know how I adopt this for my use case.


2 Likes
[Jadoch](https://forum.obsidian.md/u/Jadoch)

 September 27, 2022, 10:03am
 
20
Really happy to have found this detailled setup instructions. Thanks a lot!


I only adopted a couple of addons and templates for my usecase but it really feels like they completed my style of working with obsidian.


[gregb](https://forum.obsidian.md/u/gregb)

 October 4, 2022, 7:07am
 
21
Thanks so much for putting this together to download, I’ve been using Obsidian basically as a notepad replacement the last year or so and really starting to see the potential for using it in my role as a PM more and more with Dashboards.


A question for your meetings, I’ve been looking into a solution to pull in meeting direct from Outlook using iCalbuddy, is this something that you’ve researched? Looks like it would be a great addition


1 Like