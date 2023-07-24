---
author: cmuk
comments: true
date: 2010-12-19 13:07:29+00:00
layout: post
link: https://mckellar.wordpress.com/2010/12/19/opengl-particle-engine-finished/
slug: opengl-particle-engine-finished
title: OpenGL Particle Engine Finished
wordpress_id: 494
categories:
  - OpenGL
---

[![](https://mckellar.files.wordpress.com/2017/10/shapes3.jpg)](https://mckellar.files.wordpress.com/2017/10/shapes3.jpg)

[![](https://mckellar.files.wordpress.com/2017/10/snowstate.jpg)](https://mckellar.files.wordpress.com/2017/10/snowstate.jpg)

Here it is my finished particle engine in OpenGL, The project has been a success I have hit my 60FPS and 60,000 particle goal, infact I can get double 120,000 particles with around 87 FPS with optimisations, The first 5 weeks of OpenGL were tough, I had problems with it not displaying things on screen due to calls being ordered wrong, I would be swapping two calls which were above and below each other around and it would suddenly work, I found the OpenGL support to be very limited, I had to really think about how to set things up I couldn’t find any sort of standard framework to build off which made me think I was doing it wrong a lot of the time, I did see some similarities in the draw calls that are found in DirectX, setting up the view and proj matrices, the popping and pushing of the stack was familiar to me when I developed on the Sony PSP. Setting up a window was surprisingly very easy compared to directX, literally only one or two lines of code, the lost and found device was also simple, the most time consuming thing was setting up OpenGL, I used freeGlut which provides a lot of helper functions and GLEW.h, setting these up and getting them linking was quite painful experience as it never just worked, I had spend a lot of time searching for extensions an fixing linker problems, It wasn’t a simple case of dropping them in the system folders, I needed to link to them within the project so it would work on any machine.

After week 5 I had points drawing on screen, I decided to look at shaders, I had a lot of trouble getting openGLs shaders working in fact I’m sure it was something to do with my graphics card not supporting something, I switched to NVIDIAs CG shader language and this worked fine, I went on to develop my particles, on researching particles they are very much implemented the same way, they each have a life, they die and respawn again, they have a position and a velocity, the container is often an array to hold all the particles and gets updated and drawn by looping through each individual particle.

I got drawing points working so one vertex coloured for each particle, I then went on to look at quads which are 4 points in each corner which makes a rectangle which you then put a texture on it to make it seem more realistic, for each particle there’s now 4 verts and a texture to render, this wasn’t very efficient and quite an old technique my frame rate dropped a lot, I looked at optimising this with something called a point sprite, this is going back to the single vert or point but applying a texture to this point, so your cutting out 3 of 4 points but still having the texture, once I got this working and the frame rate went back up again, however I now had a big problem, point sprites don’t scale.

[![](https://mckellar.files.wordpress.com/2017/10/scalingissue-1.jpg)](https://mckellar.files.wordpress.com/2017/10/scalingissue-1.jpg)

To fix this I looked around the forums and found there to be a point sprite ARB extension, I found there to be an attenuation value which I could find the distance between the camera and the sprite and scale the sprite based on this value, This solved the issue and now the particles scaled the same size as if they were quads. Other optimisations were code refactoring, by unravelling loops and looking at using quad lists I got some of the GL calls down which were the main bottleneck, Overall I’m pleased with the way it turned out, Its more graphical than I thought it would be but behind the scenes I’m pleased my code layout and the efficiency I got from the CPU, my only regret is not having the time to work with the shaders as I could of put the position and velocity vectors onto the GPU and calculated them there, increasing FPS and particle count. After getting past the setting up of OpenGL I actually like programming in OpenGL more than I thought I would, I will be using it again the fututre but aslo will be using directX I think it all depends on the project and what you want to achieve. It was refreshing to use something other than directX however I have more experience with directX and would probably have achieved better results using it as I would have had the time to work with the shaders, I still dont regret chosing OpenGL and please with the end result.

http://www.youtube.com/watch?v=TDIgXSDb0tU
http://www.youtube.com/watch?v=Lq4jD_jOvoI
