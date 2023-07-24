---
author: cmuk
comments: true
date: 2009-02-22 21:38:07+00:00
layout: post
link: https://mckellar.wordpress.com/2009/02/22/applied-game-development-week-4/
slug: applied-game-development-week-4
title: Applied Game Development Week 4
wordpress_id: 332
categories:
  - Applied Game Development
---

The lecture this week was on **UML(Unified Modelling Language)** this is about planning out a project by breaking down the components into non techincal aspects. So describing an Object Orientated System without any reference to any programming language. there are 13 kinds of diagrams with two major categories **Structure Diagrams** which are static and describes how each component releates to each other. **Behaviour Diagrams** these are dynamic and describe how components act or what they do.

This week we worked on getting a build together. I solved the problem of text on screen and got that implemented I also got the track imported correctly in. The track problem was to do with the lighting type the artists used in Maya. I got the Maya file and had a play about with adding lights in and exported it into a .NIF file and it worked. I also had to re write part of Barrys Camera class so it would do rotations with an angle rather than a vector. Dom has been working on the framework and has had a bit of a disaster with losing work due to SVN problems. Martin has been doing the weapons and projectile class and working on use cases. Barry worked on an event system which has now been finished and will be implemented into the framework next week; He is also giving us a PowerPoint presentation on how it works. Andy has been working on the UML use cases based on items in the game and has worked more with the artists on the design document.

We had a publisher pitch in which Andy spoke about our game design ideas and the artists talked about their vision of the game, this went ok it could have gone better but we were restricted to time being the last group to do it. We had a few meetings with the artists and they had changed the idea slightly. Last week they wanted to have point to point racing but this week they said it would be too much work for them so we are having tracks instead while this doesnt effect us yet. we are giving them a lot of control on the level design. They made us a good a test track which we will be using from now on. We are still behind schedule but it was good to see the test track working in our framework and has boosted morale. The artists are going to light the track properly and apply bounding boxes to the track and cars so we can get test out collision next week.
