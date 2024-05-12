---
title: Git Large File Storage | Git Large File Storage (LFS) replaces large files
  such as audio samples, videos, datasets, and graphics with text pointers inside
  Git, while storing the file contents on a remote server like GitHub.com or GitHub
  Enterprise.
date: 2023-02-07
src_link: https://www.notion.so/Git-Large-File-Storage-Git-Large-File-Storage-LFS-replaces-large-files-such-as-audio-samples-vi-888db9a2f5d84fe1b0dd6a88151c110c
src_date: '2023-02-07 16:00:00'
gold_link: https://git-lfs.com/
gold_link_hash: 9e1ba9d8fce357c39ab4dff6debf743a
tags:
- '#host_git-lfs_com'
---


Getting Started
---------------


1. Download and install the Git command line extension. Once downloaded and installed, set up Git LFS for your user account by running:
 



```
git lfs install
```

You only need to run this once per user account.
2. In each Git repository where you want to use Git LFS, select the file types you'd like Git LFS to manage (or directly edit your .gitattributes). You can configure additional file extensions at anytime.



```
git lfs track "*.psd"
```

Now make sure .gitattributes is tracked:



```
git add .gitattributes
```

Note that defining the file types Git LFS should track will not, by itself, convert any pre-existing files to Git LFS, such as files on other branches or in your prior commit history. To do that, use the [git lfs migrate(1)](https://github.com/git-lfs/git-lfs/blob/main/docs/man/git-lfs-migrate.adoc?utm_source=gitlfs_site&utm_medium=doc_man_migrate_link&utm_campaign=gitlfs) command, which has a range of options designed to suit various potential use cases.
3. There is no step three. Just commit and push to GitHub as you normally would; for instance, if your current branch is named `main`:



```

git add file.psd
git commit -m "Add design file"
git push origin main
```

Check out our [wiki](https://github.com/git-lfs/git-lfs/wiki?utm_source=gitlfs_site&utm_medium=wiki_link&utm_campaign=gitlfs), [discussion forum](https://github.com/git-lfs/git-lfs/discussions?utm_source=gitlfs_site&utm_medium=discussions_link&utm_campaign=gitlfs), and [documentation](https://github.com/git-lfs/git-lfs/tree/main/docs?utm_source=gitlfs_site&utm_medium=docs_link&utm_campaign=gitlfs) for help with any questions you might have!


Git LFS is an open source project
---------------------------------


To start a discussion, file an issue, or contribute to the project, head over [to the repository](https://github.com/git-lfs/git-lfs?utm_source=gitlfs_site&utm_medium=repo_link&utm_campaign=gitlfs)
 or read our [guide to contributing](https://github.com/git-lfs/git-lfs/blob/main/CONTRIBUTING.md?utm_source=gitlfs_site&utm_medium=contributing_link&utm_campaign=gitlfs).


If you're interested in integrating Git LFS into another tool or product, you might want to read the
 [API specification](https://github.com/git-lfs/git-lfs/blob/main/docs/api/README.md?utm_source=gitlfs_site&utm_medium=api_spec_link&utm_campaign=gitlfs)
 or check out our [reference server implementation](https://github.com/git-lfs/lfs-test-server?utm_source=gitlfs_site&utm_medium=reference_servedr&utm_campaign=gitlfs).