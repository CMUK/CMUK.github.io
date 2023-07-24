---
author: cmuk
comments: true
date: 2008-12-17 08:20:34+00:00
layout: post
link: https://mckellar.wordpress.com/2008/12/17/intro-to-3d-graphics-week-11/
slug: intro-to-3d-graphics-week-11
title: Intro to 3D Graphics Week 11
wordpress_id: 200
categories:
  - Intro to 3D Graphics
---

This weeks intro to 3D i fixed my gauraud shading. The problem i was getting was due to my interpolation calculation it was interpolating by the Y values but not the X values. The calculation i was using was the same one as my flat shading with my own rasteriser. To fix this i re did my interpolation calculation but a longer way finding out the difference and the gradient.

[![](http://i81.photobucket.com/albums/j223/CMUK/guru.png)](http://i81.photobucket.com/albums/j223/CMUK/guru.png)
