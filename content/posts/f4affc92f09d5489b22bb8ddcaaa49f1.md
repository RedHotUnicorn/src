---
title: Set Up GTD in Logseq in 3 Steps - Face Dragons
date: 2023-06-17
src_link: https://www.notion.so/Set-Up-GTD-in-Logseq-in-3-Steps-Face-Dragons-5f664ce29a3d4f1d9c5477a5d0d34372
src_date: '2023-06-17 21:50:00'
gold_link: https://facedragons.com/productivity/gtd-in-logseq/
gold_link_hash: f4affc92f09d5489b22bb8ddcaaa49f1
tags:
- '#host_facedragons_com'
---



[![](data:image/svg+xml,%3Csvg%20xmlns='http://www.w3.org/2000/svg'%20viewBox='0%200%20150%20150'%3E%3C/svg%3E)](https://facedragons.com/gregory-gaynor/)
##### [Gregory J. Gaynor](https://facedragons.com/author/gregory-j-gaynor/)



[Meet Gregory](https://facedragons.com/gregory-gaynor/), a writer and the brains behind **Face Dragons**. He's the go-to guy for [getting things done](https://facedragons.com/category/productivity/). Gregory's been living the [digital nomad life](https://facedragons.com/tag/digital-nomad/) in Asia for as long as anyone can remember, helping clients smash their goals. He writes on topics like software, personal knowledge management (PKM), and [personal development](https://facedragons.com/category/personal-development/). When he's not writing, you'll catch him at the local MMA gym, nose buried in a book, or just chilling with the family.
* Gregory J. Gaynor
https://facedragons.com/author/gregory-j-gaynor/
[Don't Try the Same Digital Detox Over and Over](https://facedragons.com/health/digital-detox/)
* Gregory J. Gaynor
https://facedragons.com/author/gregory-j-gaynor/
[How to Develop Grit in Three Steps](https://facedragons.com/personal-development/how-to-develop-grit/)
* Gregory J. Gaynor
https://facedragons.com/author/gregory-j-gaynor/
[Maximize These Masculine Traits and Dragons Will Fear You](https://facedragons.com/personal-development/maximize-these-masculine-traits/)
* Gregory J. Gaynor
https://facedragons.com/author/gregory-j-gaynor/
["I Wasted My Twenties" What to Do About It](https://facedragons.com/personal-development/i-wasted-my-twenties/)


There are so many apps to choose from when it comes to setting up a GTD system. But why download and install something new when you are already using the perfect GTD application? If you use Logseq for taking notes or doing research, why not set up your GTD in Logseq too? Here’s hows to do it!


Despite what Cal Newport says, Getting Things Done is not dead! Just like Bruce Lee’s Jeet Kune Do, GTD is a framework, and you have to make it your own by using what works and discarding what doesn’t. And using Logseq for GTD works!


How to Set Up GTD in Logseq
---------------------------


Setting up GTD in Logseq doesn’t need to be a long, complicated process; you can get everything you need set up in just a few minutes. If you already use Logseq as a zettelkasten or a second brain, you can create a second knowledge graph for your GTD system. Still, [I suggest combining your PKM and GTD together](https://facedragons.com/productivity/gtd-and-second-brain/) in one complete life and knowledge management system.


Follow these steps for creating your GTD system, then below, I’ll show you how to use each feature.


### Step 1: Create Pages


1. Create a New Page called “Capture” to capture all your ideas and potential tasks.
2. Create a New Page for each of your contexts, such as “@HOME,” “@OFFICE,” “@Computer,” and “@WIFE” (Learn [all about contexts here with examples](https://facedragons.com/productivity/what-are-contexts-in-gtd/))
3. Create a New Page called “Projects List.”
4. Create a New Page, “[Areas of Focus](https://facedragons.com/productivity/areas-of-focus-examples/)“
5. Create a New Page for the other Horizons, “Goals,” “Vision,” and “Life Purpose.”


### Step 2: Add Queries for Action Lists


1. Add a Query to each of your Action Lists/Context Pages. You can paste the following (change the @HOME to whatever your template is called) though I recommend you use the alternative method below.



```
{{query (and (task TODO DOING NOW IN-PROGRESS LATER WAIT WAITING) [[@OFFICE]])(task TODO DOING NOW IN-PROGRESS LATER WAIT WAITING)}}
```

Alternatively, you can create the query yourself. **Type /query to start**


![](data:image/svg+xml,%3Csvg%20xmlns='http://www.w3.org/2000/svg'%20viewBox='0%200%201024%20576'%3E%3C/svg%3E)
1. Click the + sign to Add a Clause and select Task
2. Check the task states you will use (follow the image above if unsure)
3. Add a “Page Reference” Clause
4. Select the name of your context, e.g., @OFFICE


Repeat this process for each of your context lists or action lists.


### Step 3: Create a Project Planning Template


Create a New Page, “Templates,” if you don’t already have one, and create the following template.



```
- <% current page %>
	- [[Projects]]
	- Deadline:
	- ## Brainstorm
	- ## Plan
	- ## Tasks
		- TODO
```

Check out this [guide for Logseq Templates with lots of examples](https://facedragons.com/foss/logseq-templates/) you can use if you’re unsure how to create Templates.


Now every time you have a new project, you can:


1. Create a New Page with the name of the project
2. Use this project planning template within the new project page (by typing /template)


Doing this does two things. First, it gives you a place to brainstorm and [make a project plan](https://facedragons.com/productivity/why-your-project-management-is-a-mess-in-gtd/), and even add tasks relevant to the project. And secondly, the new project will automatically appear on your Projects List in the section labeled “Linked References.”


Capture in Your New GTD System in Logseq
----------------------------------------


If this is the first time you have ever used GTD, you will need to do a brain dump to get everything out of your head and into your system. Your initial brain dump, or capture, will take a long time to complete; I spent an entire weekend doing my initial “collect” when I started GTD many years ago. [Using a trigger list](https://facedragons.com/productivity/essential-gtd-trigger-list/) will make this process much more accessible but don’t try to rush through it. The more complete your initial brain dump or collection is, the more success you will have using GTD.


Of course, even experienced GTDers need to do a brain dump sometimes. David Allen calls it falling off the wagon when he stops using his system; a few days or weeks of ignoring your system is pretty common, especially when you have important life things going on. The brain dump is the way to get you back on the wagon.


Go through a trigger list and write everything on the “capture” page you made earlier.


You’ll also use the capture page whenever a new thought occurs to you, when a potential task appears in your world, or when someone asks you for something. Anything which might require some action in the future is something you should write onto the capture page. Remember, “Your head is for having ideas, not for storing them.”


Clarify & Organize: Key to Getting Things Done
----------------------------------------------


In the old days of GTD, these were separate processes, but today, when you’re doing GTD in Logseq, you can do them both at once.


Clarify usually means rewriting the idea you captured; you must:


* Make it Actionable
* Make it Specific


So your capture of “Speak to John” becomes “Call John” or “Email John” The difference may seem inconsequential but making the decision ahead of time on how you will “speak to John” makes you much more likely to do it and reduces decision fatigue. While deciding to pick up the phone might not seem like a considerable effort (you’d be surprised at what little things cause people to procrastinate, though,) if you’re making a hundred of these little decisions each day, fatigue quickly sets in.


Organizing means adding the correct TODO state and page reference to your captures. In Logseq, this is easy to do.


* Hit Ctrl + Enter to turn any line into a task. Hit them again to cycle through the TODO states.
* Add a link to the relevant context page, e.g., “[[@OFFICE]]”


Reflect or Review
-----------------


If you make all these lists and capture your thoughts but don’t look the list over before you start your day, you’re not really doing GTD. The point of making action lists is to look them over before you act.


David Allen doesn’t recommend any prioritization method; this can throw some new GTDer for a loop. Priorities change. If you tell yourself writing a report is the highest priority for the day, but then you get a call saying your kid has broken his arm at school, you’re not going to write that report.


That’s why you must reflect. Don’t give yourself a false priority at the start of the day; just look at the relevant context list for where you are and decide what you need to do next. When you check it off, reflect again.


Logseq Won’t Help You Engage
----------------------------



> “The last step of positively engaging with your world, is to engage *positively* with your world.”
> 
> David Allen – Making It All Work


In some sense, this is the most obvious part of GTD; you have to do something. But it can also be the hardest. No tool will help you with this; even [the best Logseq plugins](https://facedragons.com/foss/logseq-plugins/) won’t get you off the couch.


The best way to stay motivated and engaged with your tasks is to curate a list of things you want to do. In the book, David recommends a list of “braindead” tasks, easy things you can do when you’re fried. Perhaps you need a list of things you love.


Motivation will also help; listening to a motivational speech compilation before starting a period of intense work might help get you fired up.


Final Thoughts
--------------


GTD is a deep subject, and there is so much that Logseq can do, especially when you add in plugins, but this simple guide to Getting Things Done in Logseq, should get you started quickly. Use this setup as a framework and customize it till you have the GTD system you’ve always wanted.


And feel free to let me know what you did with your GTD system in Logseq over on [Twitter](https://twitter.com/FaceDragons)!