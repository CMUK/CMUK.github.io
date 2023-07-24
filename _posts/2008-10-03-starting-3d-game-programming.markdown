---
author: cmuk
comments: true
date: 2008-10-03 19:26:31+00:00
layout: post
link: https://mckellar.wordpress.com/2008/10/03/starting-3d-game-programming/
slug: starting-3d-game-programming
title: Starting 3D Game Programming
wordpress_id: 10
categories:
  - Other Projects
tags:
  - 3D
  - C++
  - Games
  - Graphics
  - Programming
  - XNA
---

Over this summer i have been looking at starting 3D game programming. I started off looking at XNA as i had been using it to create 2D games last year. I did the riemers tutorials and had my first 3D game up and running It was a simple racing game. I looked at complex collision tutorials and implemented one. After making my track bigger i found a huge problem my game was getting slow this was from using the complex collision which was only ment for small complex collisions not a whole track. I began looking into simple bounding box/sphere collision again and implemented it this time i figured out perfect collision and everything turned out great. I originally planned to do a racing game but decided to turn it into a fun mario kart block fort clone.

Current features:

- Multiplayer - xbox live 2 players, Live for windows,LAN,Voice support
- Particle effects - bullets,gravity lift
- Sky box - night and day cycle
- Animation - cars will flip when shot at, Lift goes up and down, Radar
- Different Camera angles and bullet track cam
- 360 pad support
- Map editor

![](http://i81.photobucket.com/albums/j223/CMUK/BlockFort1.png)![](http://i81.photobucket.com/albums/j223/CMUK/BlockFort2.png)

<blockquote>Basic collision code

if (car.position.Z < fortressCollision[i].Min.Z)
{
car.position.Z = fortressCollision[i].Min.Z - 450;
car.Velocity.Z = -car.Velocity.Z;
}</blockquote>

After creating this game in XNA i wanted to look at C++ and game engines. I bought the book Programming a multiplayer FPS in DirectX. I gave it try and found it quite complex and have only got about half through it. I will return to it at some point when i gain more experience with DirectX later in the year.

Over the next comming weeks i will be writing a developers diary on my progress on building a software 3D renderer from scratch using C++
