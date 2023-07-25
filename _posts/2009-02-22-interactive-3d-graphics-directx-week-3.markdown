---
date: 2009-02-22 18:11:04+00:00
title: Interactive 3D Graphics (DirectX) Week 3
categories:
  - Interactive 3D Graphics (DirectX)
---

This week we looked at a framework based on Frank D Luna’s Hello3DApp. We learnt about **Lost Devices** and **Resetting Device**.

A** Lost Device** is when something else seizes the device memory. This is can happen by ALT+Tab will get the focus of another window and the current program will have lost focus. The program needs to respond to these situations and does this by pausing and freeing up any memory stored. A silent failure is when rendering methods can return success codes even though the rendering operations have failed

**TestCooperativeLevel()**
This function waits for the program to get focus back and tells us when it has been found.
The next step is to **Reset** the device, This involves releasing all the device’s memory resources. It will always fail unless all resources allocated in the **D3DPOOL_DEFAULT** are released. You then have to re-create the resources.

After putting my Terrain App into the new framework and setting up the **Lost Device** and **Reset** methods I looked at getting text to display on screen. This involved creating a stats class which would calculate the time between frames and print debug information such as frame rates and poly counts. I then added another **Draw Text** method which would let me pass in an array to be displayed. I had a lot of trouble getting text to work, at first I thought it was the way I was passing in the array but I eventually tracked it down to using the wrong method, in **ID3DXFont **there is a method DrawTextW that takes a **WCHAR** which is the type of array I was passing in.  I did this so I could pass in the controller input information from my Terrain App class to test input. Following on from text I added support for keyboard and 360 controllers. I used **Xinput** for the 360 controller and made a separate class to manage input. Again I had troubles with the arrays I was using the copy function **strcpy_s** but as I was using **WCHAR** it didn’t like it so I changed it to use wide-character **wcscpy_s**. I then went on to make a new camera class so I could get more control out of the camera. I followed Frank D Luna’s book sample in creating a flexible camera class and got it working without any problems. I then got the 360 thumb sticks hooked up to the camera class to control the pitch and yaw.

Overall this week a lot of time has been spent on DirectX not just implementing new classes but refactoring my code and making it easier to read. I hope to get texturing and lighting done by next week and start to look at basic collision with the terrain.

[![](/assets/images/2011/04/textdebug1.png)](/assets/images/2011/04/textdebug1.png)
