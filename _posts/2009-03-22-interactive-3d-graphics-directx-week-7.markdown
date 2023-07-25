---
date: 2009-03-22 16:54:06+00:00
title: Interactive 3D Graphics (DirectX) Week 7
categories:
  - Interactive 3D Graphics (DirectX)
---

This week I have been fixing my resource manager to work with meshes. To begin with I began passing in the mesh properties to the resource manager this was really inefficient and was a quick fix I didn’t like this way of doing it so I wrote a mesh class which would store the different properties of a mesh. Then for my resource manager I just needed to pass in a pointer to the mesh object.

This worked fine to begin with but I started getting memory leaks and problems with the lost and reset devices. I fixed the major problem of it crashing on lost device and got my memory leaks from 7 down to 2. The last two memory leaks took longer than I thought to track down. I ended up commenting out code and doing tests to see if they had gone. I found out by moving the window would cause the memory leaks to multiply by 2 this singled out the memory leak to being either the lost device or reset device. I eventually figured out it was because I was calculating and generating the bounding box every time the device would reset resulting in two new pointers. I moved these into the create method so they would only be called once and it fixed it.

Another big problem was minimizing the program would cause a crash which was caused by the mouse trying to acquire before the window had a focus. I tried rearranging my code but couldn’t get it work I found a forum where someone had the same problem and tried there solution which is to change the mouseCoopFlags from Foreground to Background this solved the problem. I made some other small fixes to my code and got rid of 5 warnings.
I have started to implement a bounding volume class which will help with collision and work with ray to box or sphere collision.
