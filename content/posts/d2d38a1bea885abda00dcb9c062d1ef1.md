---
title: Stop Taking Regular Notes; Use a Zettelkasten Instead
date: 2022-01-05
src_link: https://www.notion.so/Stop-Taking-Regular-Notes-Use-a-Zettelkasten-Instead-59dedf74e6f843fbb0b735a36b2aa60c
src_date: '2022-01-05 21:47:00'
gold_link: https://eugeneyan.com/writing/note-taking-zettelkasten/
gold_link_hash: d2d38a1bea885abda00dcb9c062d1ef1
tags:
- '#host_eugeneyan_com'
---


In the [previous post](/writing/reading-note-taking-writing/), I shared about reading -> note-taking -> writing. Note-taking is a key step that converts what you read and learn into writing. This post expands on note-taking.


What’s wrong with regular note-taking?
--------------------------------------


From personal experience, **regular note-taking doesn’t work**.


Okay, that’s a sweeping statement. To *some* extent, it does. Scribbling on the margins is helpful for quickly recording insights and ideas that come while reading. Making summaries of books, articles, and papers help distil the gist and review the knowledge in future. Highlighting is… nope, highlighting doesn’t work—it’s just too passive.


Why do I say regular note-taking doesn’t work then?


Because the notes stay as **separate** notes. Ideas and knowledge remains scattered as individual pieces. In regular note-taking, connections between ideas are **not made by default**. When reviewing a note, other relevant notes (i.e., ideas) don’t present themselves. If your notes are digital, you might do a free-text search. If not, you might flip through your notebooks, or worse, not bother.


![](/assets/information-knowledge.png)


Information vs. Knowledge (by [@gapingvoid](https://twitter.com/GapingvoidArt))


I didn’t realise this was an issue until I stumbled upon the Zettelkasten, which *emphasizes* building connections between notes.


What is a Zettelkasten?
-----------------------


Zettelkasten is German for “slip-box”. It originates from German sociologist Niklas Luhmann.


One thing you should know about Luhmann—he was *extremely* productive. In his 40 years of research, he published more than 70 books and 500 scholarly articles.


How did he do accomplish this? He credits it to his Zettelkasten which focuses on **connections between notes**. He realised early that a note is **only useful in its context**, specifically, the other notes it is related to.


Here’s how a Zettelkasten works:


* Write each idea you come across on a card.
* Link idea cards to other relevant idea cards (idea -> idea link).
* Sort cards into broader topic boxes (idea -> topic link).


This is oversimplifying it, but I hope you get the gist. The key is to make connections between ideas during note-taking, *way before* you need to review them for your work. This forces you to actively connect the dots (during note-taking) and lets you find relevant ideas with ease in future.


Luhmann built a massive Zettelkasten of 90,000 notes with handwritten index cards and a wooden cabinet. Thankfully, we have digital alternatives that make it easier to navigate (and read otherwise illegible handwriting).


![](/assets/luhmanns-notes.png)


Niklas Luhmann's index cards


(There are many good articles on Luhmann, his Zettelkasten, and how he used it; I’ve listed some for further reading at the end of this post.)


How to implement your digital Zettelkasten
------------------------------------------


Some free, digital Zettelkastens include [zettelkasten.de](https://zettelkasten.de), [zettlr](https://www.zettlr.com), and [roamresearch](https://roamresearch.com). I use Roam. It has a minimal set of features required for my workflow and is actively being developed and improved on by [Conor White-Sullivan](https://twitter.com/Conaw).


Here’s my note-taking approach based on the Zettelkasten and Roam. I made tweaks to keep the process lightweight and thus easier to maintain as a habit.


### Literature note


Every (useful) book, article, or paper I read is added as a literature note. Each literature note has the following metadata: (i) tag for `#literature note`, (ii) source (e.g., book title, URL), and (iii) author.


Then, I summarise the content as how I usually would, condensing each key idea as a simple sentence, in my own words. (This sentence will be converted to a permanent note later.) Then, I elaborate on this key idea with a few bullet points. Here’s how a sample literature note looks like.


![](/assets/literature-note.jpg)


Metadata in the first two bullet points with content right after


### Permanent note


*Some* key ideas in a literature note are converted into a permanent note (hey, not all ideas are useful, right?) How do I choose what to make a permanent note? There are two general criteria:


* Is this an idea I would explore further and apply in my work/writing? Or;
* Is this an idea I can connect to other relevant ideas in my Zettelkasten?


Making a permanent note is easy in Roam—just wrap the sentence in `[[ ]]` brackets. Permanent notes have slightly more metadata:


* Tag for `#permanent note`.
* Topic tags such as `#machine learning`, `#recsys`.
* Source, which is just a link to the literature note.
* Relevant permanent notes and a short explanation of how it is relevant.
* Summary of the idea in prose.


Here’s how a permanent note looks like. It is based on the previous literature note.


![](/assets/permanent-note.jpg)


Connections made via relevant notes and `#topic` tags


Writing a permanent note takes effort. More effort than say… highlighting. You need to make connections with other notes and explain how they are related. You need to summarise the idea and knowledge in *your own words*, ensuring you *really understood*.


But putting in the effort upfront, during note-taking, makes it significantly easier to review and use your notes to synthesize content when writing.


### Topics


If you diligently added `#topic` tags, this is already done. Topic tags make navigating permanent notes easy in Roam. Clicking on `#permanent note` presents all permanent notes. You can then filter with `#topic` tags.


Here’s an example of my `#permanent notes` and some tags it has.


![](/assets/filtering-on-tags.jpg)


It's easy to see what you've been focusing on


After a few weeks, here’s how the graph of my Zettelkasten notes looks like. The biggest blue dot close to the bottom centre is the `#permanent note` node. I find watching how this knowledge graph grows satisfying. You can track how your knowledge, and the connections between them, grows.


![](/assets/note-graph.png)


This is **not** an artificial neural network


Further reading on how to use Roam for note-taking is included at the end of this post. Shu Omi’s short, hands-on video is highly recommended.


Conclusion
----------


Though it’s still early days, adopting a Zettelkasten has been one of my most productive habits. Writing the [previous post](/writing/reading-note-taking-writing/) was easier by consulting my notes on topics for `#reading`, `#note-taking`, `#writing`, and `#learning`. Finding related notes was also much simpler.


Further reading
---------------


If you found this post useful, share this tweet with your friends. Help them write more useful notes. =)



> Update: Wow this really blew up on [Hacker News](https://news.ycombinator.com/item?id=23386630) (>600 points).


  

If you found this useful, please cite this write-up as:



> Yan, Ziyou. (Apr 2020). Stop Taking Regular Notes; Use a Zettelkasten Instead. eugeneyan.com.
> https://eugeneyan.com/writing/note-taking-zettelkasten/.


or



```
@article{yan2020zettelkasten,
  title   = {Stop Taking Regular Notes; Use a Zettelkasten Instead},
  author  = {Yan, Ziyou},
  journal = {eugeneyan.com},
  year    = {2020},
  month   = {Apr},
  url     = {https://eugeneyan.com/writing/note-taking-zettelkasten/}
}
```

  

Share on: 
![](/assets/icon-twitter.svg)
![](/assets/icon-linkedin.svg)
![](/assets/icon-facebook.svg)
![](/assets/icon-mail.svg)