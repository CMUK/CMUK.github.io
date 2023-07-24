---
author: cmuk
comments: true
date: 2014-05-06 18:36:00+00:00
layout: post
link: https://mckellar.wordpress.com/2014/05/06/webgl-3d-rendering/
slug: webgl-3d-rendering
title: WebGL 3D Rendering
wordpress_id: 642
categories:
  - WebGL
tags:
  - HTML5
---

WebGL 3D rendering is fast becoming the standard for displaying/rendering 3D interactive scenes without the need for any plugins to be downloaded and installed on the web browser. No more Silverlight/flash plugin/unity plugin.

I started to look at WebGL engines and came across:
Three.Js and Babylon.Js

I built a quick 3D model of an office environment using blender and loaded the model into both engines to see what performance I could achieve.

FPS Tests:

Three.Js offered an average of 35 frames per second which just above average for a game.

Bablyon.Js averaged at around 45 frames per second, 10 frames increase over three.js

Babylon.js

- Fast smooth fluid experience both in controls and rendering.
- High FPS around 45 in my demo
  +Built in editor is great for picking apart your scene, translation, rotation, adding in objects, changing colours.

* current version is lacking export options in blender, not all textures come through correct e.g. roof tiles for the air con units did no render in babylon but did in three.js

Three.js

- Easy to get up and running just requires script adding to the page.
- Rendering more natural /realistic with better lighting and shadows compared to babylon.
- Loads scene in better than babylon.js less artifacts and missing textures/models

* Lower FPS.
* No built in editor

Same camera both engines:

[gallery ids="686,687" type="slideshow"]

Video

https://youtu.be/A1Cw1Yb5dRA
Screenshots

[gallery ids="643,644,645,646" type="rectangular"]
