---
author: cmuk
comments: true
date: 2008-12-01 09:05:27+00:00
layout: post
link: https://mckellar.wordpress.com/2008/12/01/intro-to-3d-graphics-week-89/
slug: intro-to-3d-graphics-week-89
title: Intro to 3D Graphics Week 8+9
wordpress_id: 175
categories:
  - Intro to 3D Graphics
---

Past 2 weeks i have been trying to make my own rasteriser which will allow me to do advanced shading techniques such as Gouraud shading. I have been struggling getting my head around making my own rasteriser figuring out the scan lines that go across the screen,Interpolation and setting the individual pixel. I came across many problems on my way and had it rendering to screen to begin with it just looked like some dodgy particle system but a mess with random pixels being drawn. Then it got better i could see the start of my Cartman model. Then it got even better it looked like Cartman just very square and then finally i worked out the problem through lots of debugging and number taking. The interpolation of the x value between the two vertices was adding too itself in the for loop. The next problem was the blockyness this was due to my interpolation calculation being the wrong way round after changing this it rendered to screen. I am now trying to implement Gouraud lighting and shading which will store colours in the verts and will make everything seem smoother.

[![](http://i81.photobucket.com/albums/j223/CMUK/mess.png)](http://i81.photobucket.com/albums/j223/CMUK/mess.png)[![](http://i81.photobucket.com/albums/j223/CMUK/mess2.png)](http://i81.photobucket.com/albums/j223/CMUK/mess2.png)[![](http://i81.photobucket.com/albums/j223/CMUK/mess3.png)](http://i81.photobucket.com/albums/j223/CMUK/mess3.png)[![](http://i81.photobucket.com/albums/j223/CMUK/mess5.png)](http://i81.photobucket.com/albums/j223/CMUK/mess5.png)[![](http://i81.photobucket.com/albums/j223/CMUK/mess6.png)](http://i81.photobucket.com/albums/j223/CMUK/mess6.png)
