---
author: cmuk
comments: true
date: 2009-02-07 11:18:24+00:00
layout: post
link: https://mckellar.wordpress.com/2009/02/07/directx-week-1/
slug: directx-week-1
title: Interactive 3D Graphics (DirectX) Week 1
wordpress_id: 247
categories:
  - Interactive 3D Graphics (DirectX)
tags:
  - C++
  - Direct3DDevice9
  - DirectX
---

In this weeks lecture we learnt about DirectX. We went over the very basics and history around Direct X, for this module i will be using DirectX 9 as the machines we use are XP. I began by setting up the direct X librarys and folders in visual studio. I then looked over the the SDK sample browser and was set the first 3 tasks to get us used to directX.

These were:

Creating the device - this involved creating a Direct3DDevice9 object and getting a blue screen to show.
Vertices - this involved using Direct3D 9 to draw 3 points to make a triangle with basic flat shading colour.
Matrices - in this sample you create a triangle that spins around using matrices to work out rotations.

After getting to grips with the basics and seeing the similarities to my software renderer, which was made from scratch in the intro to 3d module it felt a bit too easy. After writing rotation functions for my renderer and now having directX just use its own librarys and functions it was good to know the inner workings.

We were set some more tasks to do for next week these were:

Get 3 triangles on screen all differently coloured each rotating around a different axis

[![](http://i81.photobucket.com/albums/j223/CMUK/DXtrianglesAxis.jpg)](http://i81.photobucket.com/albums/j223/CMUK/DXtrianglesAxis.jpg)

Using only vertices create a cube rendering and rotating in wireframe mode

[![](http://i81.photobucket.com/albums/j223/CMUK/VertCube.jpg)](http://i81.photobucket.com/albums/j223/CMUK/DXtrianglesAxis.jpg)[![](http://i81.photobucket.com/albums/j223/CMUK/WireframeCube.jpg)](http://i81.photobucket.com/albums/j223/CMUK/WireframeCube.jpg)

Get 3 types of lighting - Directional,Point and Spotlight. This task has taken me quite a while as i had troubles with point which would make nothing appear on screen, i found out that i was missing some properties such as attenuation0. The spot light i cant get anything to show at the moment i have read up on it and found out it requires all D3DLIGHT9 properties. It is a bit hard to tell from the screenshot below but the point light is red and top right of the cube, The Directional light is in the top left corner and is green. the cube is also rotating and shows the green directional light intensity changing when it rotates. The spot light is blue infont of the box.

![](http://i81.photobucket.com/albums/j223/CMUK/DXPointDirLighting-1.png)

The spot light is different to a normal directional light as it has a focused point. It uses two angles Phi and Theta that are float values that deterine the size of the cone.

Phi - This is the outer cone angle
Theta - This is in the inner cone angle
