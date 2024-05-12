---
title: Responsive and editable donut charts components in Figma | Medium
date: 2022-08-14
src_link: https://www.notion.so/Responsive-and-editable-dataviz-in-Figma-Bootcamp-09a580cdde9645368a518ba0fd54f936
src_date: '2022-08-14 18:30:00'
gold_link: https://medium.com/@Double_Glitch/hacking-figma-to-create-responsive-and-customizable-dataviz-components-5e079595136
gold_link_hash: a80a6ced996f5e3eacf4d67e0b9dc2d1
tags:
- '#host_medium_com'
---

How to create PROPERLY responsive and editable chart components in Figma
========================================================================

[![](https://miro.medium.com/v2/resize:fill:88:88/1*PosQouTH4_hKBv1LQE35Ig.jpeg)](/@Double_Glitch?source=post_page-----5e079595136--------------------------------)9 min read·Jul 11, 2022--

![]()There is an infinite amount of data visualization libraries and plugins for Figma. Still, none of them, even the most sophisticated, seems to completely solve one fundamental problem: charts need to be responsive, so you could put them in the component library and reuse them across your designs in different cases. **And creating responsive components in Figma might be tricky.**

Check out these examples of responsive donut charts:

![]()![]()

See how the scaling behavior changes in the middle? It’s based on the width change only!

Looks pretty natural, huh? Well, that’s what you will be able to achieve by the end of this article, but **Figma doesn’t allow you to do this by default**. Here are some examples of how charts from the Figma Community libraries scale:

![]()

Free Community file (~5k downloads)

While stretching the content works well for bar or line charts, it doesn’t apply to shapes that have to be resized proportionally.

Although locking the content’s position in the middle partially solves the problem (and the majority of the libraries use this approach), it doesn’t often look very well:

![]()

One of the most-downloaded paid libraries

Of course, you could add some size variants for different breakpoints, but it will increase the component’s complexity, requiring double-checking if the proper variant is used in each case. And as the team grows, the chance of mistakes increases correspondingly.

I also found one interesting solution in [Mr.Biscuit](https://medium.com/u/594efe4707b8?source=post_page-----5e079595136--------------------------------)’s [**Data Visualization library**](https://www.figma.com/community/file/966692301708767071). While it works quite impressive, still, each dimension of the container has to be set manually:

![]()So here is the challenge I’ve faced: how to create a truly responsive donut chart component (or any chart that has to scale proportionally — pie/radial bar/spiderweb etc.) that adjusts automatically without overthinking from designers using it?

Let’s start with an easy one.

Horizontally-oriented chart
===========================

So first, we need to figure out how to resize both container and its content while keeping the aspect ratio fixed since Figma, surprisingly, still doesn’t have such functionality.

Luckily, there already is an answer. A couple years ago, my colleague [Solo Cube](https://medium.com/u/8e9528ce4716?source=post_page-----5e079595136--------------------------------) created one of the most mindblowing auto layout hacks:

[**This**](/@solo_cube/figma-components-with-a-fixed-aspect-ratio-elements-c7272e2ada9)

Let’s take one of the simplest components from this library—the 1:1 fixed ratio. Here is its structure:

![]()Unfortunately, it was suitable only for scaling images applied to the container as fill styles because there was no way to insert anything else into the stack without breaking the scaling behavior (except zero frames, but they don’t scale bidirectionally).

But now, its full power is unleashed with the new auto-layout update that allows applying absolute positioning for elements. That means any content with an absolute position and constraints set to “**Scale**” put inside our magical resizer will now repeat the scaling behavior of its parent!

To test that, let’s take the 1:1 fixed aspect ratio component and detach it since it’s not meant for what we are going to do with it. Now create a simple chart (donut in our case) and put it inside the detached component above the “Aspect ratio keeper” layer. After that, enable absolute positioning, align and resize the chart to fit the container, and set its constraints to “Stretch”.

![]()Now we just need to wrap it into a horizontal auto layout along with a legend and set their horizontal size to “Fill” with some spacing between them:

![]()There is still one small problem, though: when resizing, after a certain point, the layout becomes quite unbalanced because the spacing between the chart and the legend is fixed, while the white space on the right increases:

![]()The best option would be to set auto layout spacings in percentages, but it’s not possible in Figma yet. Instead, we can put the legend into a regular frame container with some left inner spacing so that the content would scale horizontally inside this frame (while the container itself still has a “Fill” width in auto layout):

![]()That’s it! Now you can make some copies with different options to turn them into component variants…

![]()…and use them as instances in other components.

![]()Vertically-oriented chart
=========================

Now the real fun begins because we will get even further in hacking Figma!

At first, I tried to apply the same approach as it was for the horizontal legend position. But since the chart scales at a 1:1 ratio, it looks too large after even a moderate resize:

![]()So I tried to apply another, more compact 2:1 aspect ratio:

![]()But again, there were resizing issues, only this time at a smaller size. If only we could create some breakpoint to change the scaling behavior depending on the frame width!

And I found one hack posted on Spectrum in 2018 (unfortunately the link is dead now). It’s based on an interesting resizing behavior. To recreate it, let’s make a frame that represents our content. Then wrap it in another frame (let’s call it “Delta frame”, you’ll see why in a bit) with constraints set to Left/Right and Top/Bottom and make sure that content clipping is disabled. After that, reduce this frame’s width while pressing Ctrl/Cmd so that it won’t affect its content. You should get the content that overflows its container:

![]()If you now try resizing the delta frame without Ctrl/Cmd pressed, you’ll see that content “flips” instantly when the width of the delta frame passes 0:

![]()Let’s wrap it into another, root frame, the same size as the initial content, and set constraints to the left and right. We will get an overlay that “disappears” (if “Clip content” is enabled for the root frame) at a certain point, revealing what’s below it. Here is a projection view for a better understanding:

![]()

The content of the delta frame is visible only above the breakpoint


> *Important note: when resizing frames using this hack, never leave them* *in the state below breakpoint — Figma “remembers” this state and the whole logic breaks. To overcome this, you can create a component from that frame and then resize its instances freely.*

As you can see, the difference between the default width and the breakpoint position equals the initial width of the delta frame, hence the name. So no matter what the default size is, you can always find or change the breakpoint position using this simple formula:

***Default width–Delta frame width=Breakpoint position***

Now we can combine this technique with the fixed aspect ratio hack to create a chart that scales only after a certain width. For that, put the 2:1 donut I’ve mentioned earlier inside the delta frame (don’t forget about constraints) — that will be the content above the breakpoint. Then duplicate it and drag below the delta frame in the layer list — it’s the content below the breakpoint. Remove auto layout and aspect ratio keeper of the duplicated frame and set chart constraints to Center and Top. Now let’s try resizing it all:

![]()Doesn’t look very smooth, but at least we have the transition. To make it seamless, we need both charts to have the same size right at the breakpoint. For that, we can decrease the size of the chart below the breakpoint, and since we are using a 2:1 aspect ratio here, this size should be exactly 1/2 of the breakpoint value. Re-center the chart after resizing and see how much better it is now:

![]()There is one significant issue, though: the height of the root frame is fixed for all breakpoints. To change that, we would need to apply an auto layout to both root and delta frames, so they adjust their height according to the content with a fixed aspect ratio. But since the width of this content exceeds its container, negative padding is required, which is impossible to set in Figma yet, so we have to find the other way around.

The content below the breakpoint is a full-size frame, so if we swap it with the content above the breakpoint, we can apply a horizontal auto-layout to the root frame and absolute position to the delta frame (keeping the constraints). But of course, it will swap the order as well: what was above the breakpoint now appears below it, and vice versa:

![]()

Not exactly what I wanted, but at least the height changes now 😄

So now we need to reverse the behavior while somehow keeping this layer structure. And after experimenting a bit, I found the solution: both the delta frame and its content should be **visually** shifted to the right outside their parent frames. That means that to preserve the layer structure, you have to use arrow keys instead of your mouse to move the layers. If done correctly, it should look like this:

![]()

“Clip content” is disabled.

Now the delta frame will flip **in** the root frame below the breakpoint instead of flipping out. Because of that, we need to mirror its content horizontally:

![]()Let’s test it out:

![]()Much better, but there is still one more issue: the frame’s height will scale down to zero because there is no minimum value. To prevent this, we need to add a zero-width frame to the stack. Its height equals the height of the chart below the breakpoint, which, as you remember, is 1/2 of the breakpoint value:

![]()And after all the improvements, we finally created a beautiful responsive chart! Now you can create a component and use it the same way as the horizontally-oriented chart:

![]()Known issues
------------

1. Creating pie/donut charts with the Arc tool allows you to edit them even in instances, but since this component technically consists of two independent charts, editing one of them won’t affect the other.
2. The same issue applies to editing text. But luckily, it can be fixed with the new Figma functionality called Text properties. You can add one property to different text layers, and they all will share the same content.
3. The component can only be resized horizontally. Attempting to resize it vertically breaks the behavior.
4. The sophisticated structure of this component complicates its modification according to your needs.

Conclusion
==========

While Figma provides many useful tools, it still lacks some key functionality. And while we can partially mimic it using different hacks, native implementation of these features would ease our lives so much:

* minimum/maximum width and height;
* resizing with fixed proportions;
* negative and percentage-based padding in auto-layouts;
* breakpoints.

Figma continues to grow and evolve, so I believe that one day we may see all of them and maybe even more.

**Explore the sample file:**