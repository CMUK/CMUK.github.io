---
author: cmuk
comments: true
date: 2008-10-26 12:28:21+00:00
layout: post
link: https://mckellar.wordpress.com/2008/10/26/intro-to-3d-graphics-week-4/
slug: intro-to-3d-graphics-week-4
title: Intro to 3D graphics week 4
wordpress_id: 97
categories:
  - Intro to 3D Graphics
---

This week i have been looking at virtual cameras in 3D space. I learnt about the uses of a virtual camera in that it is used as if it was your eyes looking around the world space. We looked at the Roll(Z axis),Pitch(X axis),Yaw(Y axis) this is used to rotate the camera using a matrix to apply rotation. We then looked at a funny a thing called Gimbal Lock as mythical as it sounds its actually a problem that occurs with Eulers angles theory. It is hard to explain without seeing so here is a diagram

[youtube=http://www.youtube.com/watch?v=rrUCBOlJdt4]

Basically Gimbal Lock is when two axis align and you lose a degree of freedom

We then had lecture on World Space and the Camera view. This was hard to get my head around but if you are moving the camera around your game you want to apply one big matrix that has your rotations and your translations in you are moving the world space to the camera position. To get everything to work you have to get the view matrix to be an inverse of the world space. To do this the rotations need to be negative the easiest way to do this is to transpose the matrix. Then to get the translation right you have to make them negative. After this you should have 1 big view matrix that is working right in your 3D world. After this we looked at the Projection Matrix this is hard to explain but its like how far you see in depth and how it gets projected to a plane.

You have your plane and your object. You have lines(projectors) coming from your object to your plane unlike 2D where they are parallel in 3D they meet up to a point called the center of projection. The center of projection where the lines meet is in front of the plane this causes the image to invert much like the human eye. Moving your object further away from the plane causes the perspective projection to get smaller.

Projection Matrix

d   0     0     0
0   d     0     0
0   0     d     0
0   0  1/d    0

The view frustum

This the volume of space visible to the camera. It is shaped like a pyramid with the point being closest to the camera it isn't a point but a chopped off rectangle that makes the near clip plane and the base of the pyramid is the furthest away. Its job is to limit what you see this is called clipping. It does this by having 6 sides of the pyramid. The base is called the Far clip plane which limits the distance the camera can see.

Field of View

This is effectively the camera zoom. This works by two angles a horizontal and a vertical angle. zoom measures the objects size relative to 90 degrees. To zoom in you increase the FOV to zoom out you decrease the FOV.

This weeks tasks are to implement a camera class which works out the camera matrix for camera view and camera projection. Also have to implement a model class which will import basic Quake models however i wont be able to see them just the debug info on them. Once this math side is all implemented i can start having fun with rendering to the screen
