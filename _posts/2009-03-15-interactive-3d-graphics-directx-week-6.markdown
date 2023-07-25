---
date: 2009-03-15 19:19:21+00:00
title: Interactive 3D Graphics (DirectX) Week 6
categories:
  - Interactive 3D Graphics (DirectX)
---

This week i got my Camera colliding with the terrain fixed. I have been having trouble with it for the past few weeks as it was nearly working and kept crashing. The problem was with the way i was working out my Get Height method the spacing was wrong and needed to be negated to turn the value into a positive. After changing these two lines it worked and i was able to simulate walking on the terrain.

As we are remaking "de blob" i have flattened my terrain out as i plan to put the streets and buildings in. I have been making a zombie class and a zombie state to get a zombie loaded into my game at the moment he just runs round in circles but i should be able to apply the camera get height to the zombie so he can collide and walk on the terrain. I have also made a ResourceManager class which will manage the textures and meshes loaded in. The advantages of using this is if i already have a texture loaded in i don't need to waste memory by loading another copy in i can simply look in the std::map list for the texture name. At the moment it works fine for textures i am in the process or making it work for meshes as meshes work differently requiring a material to be stored. I have also made a WorldObjects class which lets me place zombies around my level it does this by taking the position and orientation and drawing it.

[![](/assets/images/2011/04/zombie.png)](/assets/images/2011/04/zombie.png)
