---
author: cmuk
comments: true
date: 2008-11-09 12:33:11+00:00
layout: post
link: https://mckellar.wordpress.com/2008/11/09/intro-to-3d-graphics-week-6/
slug: intro-to-3d-graphics-week-6
title: Intro to 3D Graphics Week 6
wordpress_id: 138
categories:
  - Intro to 3D Graphics
---

Here it is finally after many hours of frustration i have my model rendered to screen with rotation

[![](http://i81.photobucket.com/albums/j223/CMUK/1-2.png)](http://i81.photobucket.com/albums/j223/CMUK/1-2.png)[![](http://i81.photobucket.com/albums/j223/CMUK/2-2.png)](http://i81.photobucket.com/albums/j223/CMUK/2-2.png)[![](http://i81.photobucket.com/albums/j223/CMUK/3-1.png)](http://i81.photobucket.com/albums/j223/CMUK/3-1.png)[![](http://i81.photobucket.com/albums/j223/CMUK/4-1.png)](http://i81.photobucket.com/albums/j223/CMUK/4-1.png)

To begin with every time I ran my programme it would close. I debugged my way through every line and came across a silly mistake. In my main message loop for the window I had changed if (msg.message == WM_QUIT) to if (msg.message = WM_QUIT) causing it to quit straight away as its assigning and not checking the equality. After changing this my programme would stay open however there was nothing on screen. I re tested my matrix and vector classes but they all worked the problem was with my Trans Verts I was missing a column on my 2D array after adding this it all rendered to screen. It still needs optimising and I am currently working on backface culling.
