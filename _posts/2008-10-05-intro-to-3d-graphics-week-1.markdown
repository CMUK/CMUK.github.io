---
date: 2008-10-05 14:05:23+00:00
title: Intro to 3d Graphics Week 1
categories:
  - Intro to 3D Graphics
tags:
  - 3D
  - Graphics
  - Maths
  - Programming
---

This week ive been looking at GDI+ in C++. In the lesson i created my first GDI+ window which i drew lines and shapes on ([pic](/assets/images/GDI.png)). I looked at loading images onto the window which was very easy with help from the MSDN. After having a play with GDI+ i looked at Vector maths. This weeks tasks were maths based and important for later weeks.

## **Vectors**

**Magnitude**

**2D magnitude**

Example (Xh,Yh) = (3,4)  ,  (Xt,Yt) = (1,1)

Magnitude is 3-1 (xh-xt) = 2          (Yh-xt)  4-1 = 3

√(2 squared + 3 squared) = 3.606

**3D magnitude**

\*\*\*\*Example (1,2,3)

√(1 squared + 2 squared + 3 squared) **= 3.741**

**Scalar**

A scalar is doubling or halving the vector

n = (2,4,6)   n2 = (4,8,12)

**Adding/Subtracting a vector**

r        s
x|3|    x|2|       3+2 = x[5]
y|4| + y|4|   =  4+4 = y[8]
z|5|    z|1|       5+1 = z[6]

Subtracting 3D vectors

x|3|    x|2|       3-2 =  x[1]
y|4| - y|6|   =  4-6 = y[-2]
z|5|    z|1|       5-1 =  z[4]

**Unit Vectors**

A unit vector is a vector that has a magnitude of 1 and is useful when it comes to vector multiplication
Converting a vector into a unit form is called normalizing and is achieved
by dividing a vector’s components by its magnitude

r = [1]
[2]
[3]

||r|| =       1 squared + 2 squared + 3 squared = √14

ru =    1  [1]     [0.267]    <  1/ √14
√14 [2]  =      [0.535]    <  2/ √14
[3]        [0.802]    <  3/ √14

**The dot product (scalar product)**

R = [6]     S = [2]
[-3]           [4]
[2]             [9]

||s||.||r|| cos(β) = 6x2 + (-3)x4 + 2x9 = **18** Dot product

Taking this a step further we can work out the angle between two vectors

||r|| = √62 + (-32) + 22 = 7
||s||= √22 + (-42) + 92 = 10.049

7 x 10.049 x cos(β) = 18

cos(β) =          18
10.049x7        =    0.255

β = cos-1(0.255) = 75.2 degrees

**Cross-product (The Vector Product)**

The vector product, which is
also called the cross product because of the ‘×’ symbol used in its notation. It
is based on the definition that two vectors r and s can be multiplied together
to produce a third vector t:
r × s = t

a = 8i – 3J + 6k
b = -2i – 4J – 8K

I          J           K
8         -3          6
-2        -4         -8

I = (-3x-8) – (-4x6) = 24 - - 24 = 48
J = (8x-8) – (-2x6) = -64—12 = -52 Reverse J so answer is 52
K = (8x-4) – (-2x-3) = -32-6 = -38

axb = [48,52,-38]

---

---
