---
layout: post
title: Scratch your own fontend
date: 2018-05-07
type: post
parent_id: '0'
published: true
password: ''
status: publish
categories:
- Programming
tags: []
author:
  login: marcofognog
  email: marcofognog@gmail.com
  display_name: marcofognog
---

I had this itch that I was never able to scratch before: whenever I was in that **coding flow**, with both hands at the keyboard, sometimes I'd need to get one of them off to reach for the mouse. I know, I know ... the time that it takes might not justify my complaints, but it always feels super unconfortable and distracting.

After working for almost 7 years as Rails developer, mostly in the backend, I notice now I had a legit * desktop frontend * problem to solve. And the Linux frontend (X11, to be precise) development is a whole other world from what I was used to. Right then I knew it was going to be a fun litle project.

The result is this [* xmousable *](https://github.com/marcofognog/xmousable) app, it has an X in the name because it is a client of the X11 graphics server. Hey, I'm just serving the naming tradition, not trying to be cool.

### A simple idea

Instead of dragging the mouse pointer across the screen, each key on the keyboard would be mapped to a certain region of the screen. Once a key is pressed, the pointer would jump right at its corresponding region. Than the user would do the fine adjustments using the arrow keys.

Heres an ugly (but very didactic) gif from the project's [README](https://github.com/marcofognog/xmousable):

!["xmousable demo"](https://raw.githubusercontent.com/marcofognog/xmousable/master/xmousable-demo-1.gif "xmousable demo")

*TIP: it's possible to make it (link prettier) passing parameters to not show the letters.*

If it were a comercial software, in the *LEAN* community we'd call it *MVP*, in this case I'd call it a *prototype*: it's code is still clumsy but is enough to start testing in the real world (which is only my machine so far). If my approach is good enough, then I might want to invest more time and effort on improving it.

It's been interesting to feel how we can interact with the computer in different ways, and be more aware about how we deal with it. For instance, if I wanna just "float" the web (I wouldn't call it surfing ...) without a specific objective (facebook, twitter, etc...), it is better to use the good old mouse. But for clicking once or twice in the middle of the coding flow, [xmousable](https://github.com/marcofognog/xmousable) has been super convinient.

... Or maybe I am biased because it is MY PRECIOUS PROJECT?

Only time will tell.



