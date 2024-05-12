---
title: 'GitHub - ObsidianPublisher/obsidian-github-publisher: Github Publisher helps
  you to publish your notes on a preconfigured GitHub repository from your Obsidian
  Vault, for free, and more!'
date: 2023-03-22
src_link: https://www.notion.so/GitHub-ObsidianPublisher-obsidian-github-publisher-at-obsidian-iceberg-86040abc1474423dbc68f6973c0b0fe2
src_date: '2023-03-22 17:38:00'
gold_link: https://github.com/ObsidianPublisher/obsidian-github-publisher
gold_link_hash: ea26e46efdfa5a52a1be0b36bc1240bc
tags:
- '#host_github_com'
---



| order |
| --- |
| 1 |


[![](https://camo.githubusercontent.com/04b8069c1578368042017687c758d7bfa02c1c1151d4264afa8b19c64f483ead/68747470733a2f2f696d672e736869656c64732e696f2f62616467652f64796e616d69632f6a736f6e3f6c6f676f3d6f6273696469616e26636f6c6f723d253233343833363939266c6162656c3d646f776e6c6f6164732671756572793d2532342535422532326f6273696469616e2d6d6b646f63732d7075626c69736865722532322535442e646f776e6c6f6164732675726c3d68747470732533412532462532467261772e67697468756275736572636f6e74656e742e636f6d2532466f6273696469616e6d642532466f6273696469616e2d72656c65617365732532466d6173746572253246636f6d6d756e6974792d706c7567696e2d73746174732e6a736f6e)](https://camo.githubusercontent.com/04b8069c1578368042017687c758d7bfa02c1c1151d4264afa8b19c64f483ead/68747470733a2f2f696d672e736869656c64732e696f2f62616467652f64796e616d69632f6a736f6e3f6c6f676f3d6f6273696469616e26636f6c6f723d253233343833363939266c6162656c3d646f776e6c6f6164732671756572793d2532342535422532326f6273696469616e2d6d6b646f63732d7075626c69736865722532322535442e646f776e6c6f6164732675726c3d68747470732533412532462532467261772e67697468756275736572636f6e74656e742e636f6d2532466f6273696469616e6d642532466f6273696469616e2d72656c65617365732532466d6173746572253246636f6d6d756e6974792d706c7567696e2d73746174732e6a736f6e)


GitHub Publisher
================


Publish your notes in your own GitHub repository for free and do whatever you want with them. ✨


This allows you to set up any template: Jekyll, Mkdocs, Hugo, or custom-made ones!


📑 [Documentation](https://obsidian-publisher.netlify.app/)
----------------------------------------------------------


Here, you will only get a quick setup!


🪄 Features
----------


* Converting `[[wikilinks]]` to markdown links
* Linking to other notes and updating the links according to your settings
* Cleaning the repo by removing depublished and deleted files
* Folder notes (renaming them to a specific name, like `index.md`)
* All dataview queries are supported (including `dataviewjs`, inline DQL and inline `dataviewJS`.)
* Supporting any markdown syntax supported by your template, as well as other formats like Mermaid or Latex
* And many more ✨


Warning

Do not use this plugin to sync or save your Obsidian Vault!
Avoid opening the converted files from your repository in Obsidian!




---


🖥️ Initial setup
----------------


There are plenty of options available, some of which are pre-configured and others are optional.


Before you begin, you will need to configure your GitHub repository.


1. Fill in your username, repository name, and branch.
2. Generate a GitHub token from the settings link and paste it here.
3. Click the button to check if everything is working as intended.
4. Now, let's try publishing your first note! To achieve this, you need to set the key `share: true` in the frontmatter of a file, like this:

```
---
share: true
---

```
5. Now, run the command to publish: `Upload single current active note`
6. If everything is good, a PR will be created on your repository and will be automatically merged (this can be disabled if desired!).


That's it! However, there are many options that a simple README cannot cover, so please refer to the documentation for more information. 💕.


⚙️ Usage
--------


The plugin adds 8 commands in the palette, one of which is also available in the right-click menu.


* `Upload single current active note` (*available in the right-click menu*)
* `Upload all notes`
* `Upload unpublished notes`
* `Refresh published and upload new notes`
* `Refresh all published notes`
* `Purge depublished and deleted files`
* `Test the connection to the configured repository`
* `Check the rate limit of the GitHub API`


Each of the commands are explained [here](https://obsidian-publisher.netlify.app/Commands).


🤖 How it works
--------------


1. The plugin will create a branch named after your vault, where spaces are replaced by a `-`.
2. The plugin will perform all conversion (based on your settings) and push the note(s) into the branch.
3. By default, the branch will be merged once all the notes (and their embedded files) have been processed.


Warning

Sometimes, the branch may not be merged due to merge conflicts. This can occur if you push too frequently.


🪛 Developing
------------


You can :


🪧 Looking for something?
------------------------




---


If you find this plugin and workflow useful, you can give me some coffee money!  

[![](https://camo.githubusercontent.com/938f57e4b1f4ee91d585cbf7cb943e60b2381cc9a07317e2c18086b89fceb77c/68747470733a2f2f63646e2e6b6f2d66692e636f6d2f63646e2f6b6f6669312e706e673f763d33)](https://ko-fi.com/X8X54ZYAV)