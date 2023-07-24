---
author: cmuk
comments: true
date: 2009-03-01 12:25:45+00:00
layout: post
link: https://mckellar.wordpress.com/2009/03/01/interactive-3d-graphics-directx-week-4/
slug: interactive-3d-graphics-directx-week-4
title: Interactive 3D Graphics (DirectX) Week 4
wordpress_id: 352
categories:
  - Interactive 3D Graphics (DirectX)
---

This week i have been implementing a State Based Manager. This allows the engine to go into different states such as loading. The terrainApp now inherits from StateBased and separates into a game component. I created a GameApp which is now my main engine where calls to init,update,draw get called. In this class i have my current state which is set to loading class. within this i forward calls to loading screens init,update,draw functions. I created a loading state which displays an image and waits for a certain amount of time before changing state to the terrainApp. i had problems getting the state based working at first i had just had the default blue screen which is when the screen gets cleared to that colour. I tracked this down to not calling the right method drawScene and render after calling the right method i got it changing state and trying to render the terrain. I got the problem where an error box would come up and wouldn't go away. Very helpful error box
[![](https://mckellar.files.wordpress.com/2017/10/error.png)](https://mckellar.files.wordpress.com/2017/10/error.png)

I found the problem was with having HR(gd3dDevice->BeginScene()); in my loading::drawScene method. I was already calling begin scene from my GameApp so it was getting called twice and causing it to crash. I also got this error box when i moved or lost focus on the loading screen window this was due to the device being lost and not reset. I fixed this by releasing the buffer and texture in my loading class. After getting font working in my loading class i decided to try and get a full screen quad texture to display. I got the texture loaded and rotating around. I also got height based lighting working which just sets the light intensity at the vertex y value. I am currently implementing a resource manager which is a central depot for resources. It will cache textures and meshes i use and avoid the program from reloading theses making it more efficient.

[![](https://mckellar.files.wordpress.com/2017/10/loading.png)](https://mckellar.files.wordpress.com/2017/10/loading.png)
[![](https://mckellar.files.wordpress.com/2017/10/heightbased.png)](https://mckellar.files.wordpress.com/2017/10/heightbased.png)
