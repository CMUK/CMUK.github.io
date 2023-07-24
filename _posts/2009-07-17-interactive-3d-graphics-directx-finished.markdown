---
author: cmuk
comments: true
date: 2009-07-17 14:13:30+00:00
layout: post
link: https://mckellar.wordpress.com/2009/07/17/interactive-3d-graphics-directx-finished/
slug: interactive-3d-graphics-directx-finished
title: Interactive 3D Graphics (DirectX) Finished
wordpress_id: 416
categories:
  - Interactive 3D Graphics (DirectX)
---

[youtube=http://www.youtube.com/watch?v=5qnjSXQWs0Y]

It’s been a while since my last update but after many weeks I’ve finished my De Blob remake, while it is finished to the deadlines I am still carrying on working on it, I will work more on shaders and some advanced directX techniques. As its stands it’s more of a tech demo than a game, I have taken this approach from the start since it began as a terrain demo, then to a zombie demo and now to almost a game. I am very happy with the way it has turned out, it has been the hardest work I’ve taken on yet, as directX was all new to me and learning the techniques and how it all works took some time.

As from my last update a lot has changed, before it was a blob changing colour on collision with three zombies. Since then I have got boundingBox collisions/Textured Meshes/Buildings/Shaders for the Blob/Particles/Road/Skybox/Car/Helicopter/Multiple camera angles/State system these are just a few of the recent additions. I have also optimised the code and refactored a lot of the classes to make it easier to work with and be more efficient.

It was near the end of the project that i started to think more about structure and making it into a game, I looked at inheritance and was able to get the car, helicopter and zombies all inheriting from a base object class. In Hindsight this approach should have been taken at the start but as it was at the experimental stages i took my time learning and applying the techniques learned each week.
