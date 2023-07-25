---
date: 2008-10-12 14:55:36+00:00
title: Intro to 3D graphics week 2 Matrices
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

Matrices are a useful way of presenting data in a neat tabular form. A matrix is a rectangular array of numbers with each element being a number of the array. n rows and m columns

A = 1,2,3
4,5,6
7,8,9

**Adding two matrices together**

3,-2,5         7,8,4    =    3+7,-2+8,5+4    =     10,6,9
1,3,4     +   3,2,5    =    1+3,3+2,4+5      =      4,5,9
5,-4,6         3,6,4    =    5+3,-4+6,6+4    =    8,2,10

**Taking away**

3,-2,5          7,8,4     =     3-7,-2-8,5-4      =       -4,-10,1
1,3,4     -    3,2,5     =     1-3,3-2,4-5         =      -2,1,-1
5,-4,6         3,6,4     =    5-3,-4-6,6-4       =       2,-10,2

**Multiplying by a scalar**

k = 3

3,-2,5      = (3)3,(3)-2,(3)5             9, -6,15
1,3,4        = (3)1,(3)3,(3)4       =     3, 9, 12
5,-4,6      = (3)5,(3)-4,(3)6             15,-12,18

premultiply of A by B means forming BA and postmultiplication of A by B means forming AB

**Transpose of a matrix**

first row becomes first column and second row becomes the second column

A,D,G               A,B,C
B,E,H      =       D,E,F
C,F,I                G,H,I

**Matrix Identity**

Square matrix with 1s on the main diagonal and zeros everywhere else

100
010
001

**Multiply Matrices**

Row by column

3,-2,5           7,8,4
1,3,4     x      3,2,5
5,-4,6          3,6,4

=    (3x7 + -2x3 + 5x3),(3x8 + -2x2 + 5x6),(3x4 + -2x5 + 5x4) = 10,50,2
=    (1x7 + 3x3 + 4x3),(1x8 + 3x2 + 4x6),(1x4 + 3x5 + 4x4) = 28,38,35
=    (5x7 + -4x3 + 6x3),(5x8 + -4x2 + 6x6),(5x4+-4x5+6x4) = 41,68,24

**Obtaining the inverse** **of a 3x3 matrix**

determinant A must be non-zero

2, 4, 6
2, 7, 8      =    2   |7, 8| -4|2, 8| + 6|2, 7| = (-2)-(40)+(54) = 12 Det
1, 8, 9                 | 8, 9|     |1, 9|      |1, 8|

|7, 8| (7x9-8x8 )   |2, 8|               |2, 7|
|8, 9|  = -1                |1, 9|  = 10    |1, 8| = 9

|4, 6|                          |2, 6|               |2, 4|
|8, 9|  = -12             |1, 9|  = 12    |1, 8| = 12

|4, 6|                          |2, 6|               |2, 4|
|7, 8|  = -10             |2, 8|  = 4    |2, 7| = 6

-1, 10, 9                  + - +                -1, -10, 9                                -1, 12, -10
-12, 12, 12      x       - + -        =      12, 12, -12         Transpose > -10, 12, -4
-10, 4, 6                  + - +               -10, -4, 6                                   9, -12, 6

Inverse =
-1/12, 12/12, -10/12                     -0.833, 1, -0.833
-10/12, 12/12, -4/12             =     -0.833, 1, -0.333
9/12, -12/12, 6/12                          0.750, -1, 0.500

**Dot Product(Scalar Product)**

The dot product is used to calculate the angles between two vectors used mainly in lighting calculations. It is the sum of the products of the corresponding components.

[4, 6] . [-3, 7] = (4)(-3) + (6)(7) = 30

**Cross Product
**

Creates a vector which is [perpendicular](http://en.wikipedia.org/wiki/Orthogonal) to the plane containing the two input vectors.

a = 8i - 3j + 6k

b = -2i - 4j - 8k

I    J    K

8   -3   6

-2  -4  -8

I = (-3 x-8 ) – (-4x6) = 24 - -24 = 48

J=(8x-8)-(6x-2)= -64 - -12 = -52 > 52   REVERSE J SIGN

K=(8x-4)-(-2x-3)=-32-6= -38
