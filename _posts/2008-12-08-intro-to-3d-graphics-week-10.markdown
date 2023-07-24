---
author: cmuk
comments: true
date: 2008-12-08 08:56:35+00:00
layout: post
link: https://mckellar.wordpress.com/2008/12/08/intro-to-3d-graphics-week-10/
slug: intro-to-3d-graphics-week-10
title: Intro to 3D Graphics Week 10
wordpress_id: 189
categories:
  - Intro to 3D Graphics
---

This weeks intro to 3D ive been struggling with the gouraud lighthing/shading i got stuck on a problem that was my model was black on screen even after i hardcoded the colour values. I spoke to adam and found the problem the makeARGB i was using it without putting Color:: infront. After this my model was still not shading correctly i decided to try and implement gouraud point lighting and this seemed to work fine but it should of been harder to do than directional gouraud lighting. I am going to get directional done this week and try optimising my code to improve frame rate.

Flat no gouraud

[![](http://i81.photobucket.com/albums/j223/CMUK/flat.png)](http://i81.photobucket.com/albums/j223/CMUK/flat.png)

Point Gouraud

[![](http://i81.photobucket.com/albums/j223/CMUK/gurupoint1.png)](http://i81.photobucket.com/albums/j223/CMUK/gurupoint1.png)

Directional Gouraud wrong

[![](http://i81.photobucket.com/albums/j223/CMUK/gurudirectionalwrong.png)](http://i81.photobucket.com/albums/j223/CMUK/gurudirectionalwrong.png)
