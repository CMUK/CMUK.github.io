---
author: cmuk
comments: true
date: 2009-02-27 17:56:44+00:00
layout: post
link: https://mckellar.wordpress.com/2009/02/27/console-development-semester-2-week-4/
slug: console-development-semester-2-week-4
title: Console Development Semester 2 Week 4
wordpress_id: 341
categories:
  - Console Development Semester 2
---

This week we learnt about floating point numbers. We took a step back and looked at the maths and different types of numbers.  Looking at Unsigned binary integers with 8 bits up to 256 patterns ranging from 0..255. 16 bits up to 65,536, 32 bit with up to 4 billion patterns. Signed binary integers take into account negative numbers such as 8 bit = {-128..0..+127}

Non-integer representations these include fractions and ratios. The floating point number 3.14 is split up into 3.  + 1/10 + 4/100 with a finite expansion. Looking at the PSP FPU Pipeline it takes 28 cycles to do divide or square roots whereas simple maths such as adding takes 1 cycle to complete. This week’s task was to implement a 32-bit IEEE754 arithmetic unit we are to only use ints to represent floats.
