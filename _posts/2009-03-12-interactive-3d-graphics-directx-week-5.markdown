---
author: cmuk
comments: true
date: 2009-03-12 09:22:55+00:00
layout: post
link: https://mckellar.wordpress.com/2009/03/12/interactive-3d-graphics-directx-week-5/
slug: interactive-3d-graphics-directx-week-5
title: Interactive 3D Graphics (DirectX) Week 5
wordpress_id: 364
categories:
  - Interactive 3D Graphics (DirectX)
---

This week i have been looking at rays and there uses. A ray is used to find all sorts of information in the scene. It gets cast in with a start point and a direction and intersects with objects or meshes in the scene and provides information such as hit count, distance and normal. It is most commonly used in games for the bullets hitting targets or to work out collision with the heightmap you would cast a ray down. It can be used in complex ways such as AI path finding by casting rays on objects or to check if the AI can see the player. I managed to implement my ray methods using the DirectX sample picking. it shows which triangle i select when i click on my terrain mesh. I also added a grass texture to the terrain to make it look better this was just one line of code as i had already set up texture support. We got the assignment this week which is to recreate the game[ "De Blob"](http://en.wikipedia.org/wiki/De_Blob) this came as quite a shock to everyone as compared to last years simpler assignment this is going to be a very hard challenge.
