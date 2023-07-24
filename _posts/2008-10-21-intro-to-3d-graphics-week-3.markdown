---
author: cmuk
comments: true
date: 2008-10-21 15:00:01+00:00
layout: post
link: https://mckellar.wordpress.com/2008/10/21/intro-to-3d-graphics-week-3/
slug: intro-to-3d-graphics-week-3
title: Intro to 3D graphics week 3
wordpress_id: 71
categories:
  - Intro to 3D Graphics
tags:
  - 3D
  - Graphics
  - Maths
  - Matrices
  - Matrix
  - Programming
---

This week i have been implementing a Matrix class into my program. Here are some of the Matrix transforms

Matrix Transforms

Translation

x     100 xshift
y  = 010 yshift
z     001 z shift
w    0001

To move along the x,y or z axis you just change the x,y,z shift to the value you want to move by you can use minus to move one direction and positive for the other direction.

Scaling

x   xscale      0  0   0
y   0     yscale     0  0
z   0   0    zscale     0
w  0   0     0            1

Scaling is simply increasing the x,y,z scale in the direction you want to increase.

Rotation

![](http://i81.photobucket.com/albums/j223/CMUK/MatrixRotation.png)

Transform function

passing in the transform matrix and the vector to be transformed and also a blank vector for the result. The matrix gets applied to the vector your passing in and stores it in a result vector giving you the transformed vector. In the method below it performs a dot product to give the result in vector form

void Matrix::Transform(const Matrix& m, const Vector& v, Vector& result)
{

result.\_x =  v.\_x _ m.\_m[0][0] + v.\_y _ m.\_m[1][0] + v.\_z _ m.\_m[2][0] + v.\_w _ m.\_m[3][0];
result.\_y =  v.\_x _ m.\_m[0][1] + v.\_y _ m.\_m[1][1] + v.\_z _ m.\_m[2][1] + v.\_w _ m.\_m[3][1];
result.\_z =  v.\_x _ m.\_m[0][2] + v.\_y _ m.\_m[1][2] + v.\_z _ m.\_m[2][2] + v.\_w _ m.\_m[3][2];
