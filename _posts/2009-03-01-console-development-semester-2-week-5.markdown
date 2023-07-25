---
date: 2009-03-01 11:34:02+00:00
title: Console Development Semester 2 Week 5
categories:
  - Console Development Semester 2
---

This week we followed on from last weeks look at floating points. We look more in depth with how they are represented Binary floating point is setup with (Sign) Mantissa x Base ^ Exponent for example 9.3_¹º \_x 10 ^ 6 miles

**IEEE 754 standard**

This is set out like (-1)**S** x (1+**F**) x 2(**E** –bias)  **S**= Sign **F **= Fraction or Mantissa **E** = Exponent
Single precision is a 32 bit value **1** sign /**8** exponents and **23** mantissa bits.
1             8                            23
0|10110101|11010101001010101011010
S             E                                F

At the start of the Mantissa there is an implicit **1.** so there is in fact 24 bits. Values range from 1 ≤ F < 2-2²³   or 1 ≤ F < 2
The exponent is repesented by 8 bits ranging from 0 - 255 single precision the bias is 127 making the range go from -126 ≤ E ≤127

When comparing two Mantissas the exponent must be looked at as if one mantissa is larger than the other but the other has a larger exponent then it will be larger.
The largest value for the Mantissa in single precision is (2-2-²³)x 2 ^127 and the smallest being ...2 ^ -126.

When adding floating point numbers you have to get the Exponents the same. Two values in registry the exponents get looked at first in the small ALU 8 bits and returns the difference. The next step is alignment one of the signifcants get shifted by the difference so the Exponents get aligned.

(-1)s¹ x F1 x 2E¹ + (-1)s² x F2 x 2E²
if  E¹ > E² then
(-1)s¹ x F1 x 2**E¹ **+ (-1)s² x F2' x 2**E¹**
F2' = F2/2 **E¹ - \*\***E²\***\* **This is involves bit shifting right
Result = (-1)s¹ x **(F1 + F2') **x 2E¹ This value will be unormalised and may need normalising. If it is too large it will need to be shifted to the right and the exponent will be adjusted.

Multiply is similar

(-1)s¹ x F1 x 2E¹ + (-1)s² x F2 x 2E²
= (-1)s¹ xor s² x (F1 x F2) x 2E¹ + E²
if (F1 x F2) exceeds 2 it will need normalising this is done by dividing by 2 and incrementing the Exponent.

Division

You need to check that F2 is no equal to 0.
(F1 ÷ F2) x2 ^ E1 - E2
.5 < (F1 ÷ F2) < 2

Underflow and Overflow with underflow setting the value to 0. Loss of significance is where the remaining bits are lost due bit shifting this makes the number less accurate.
