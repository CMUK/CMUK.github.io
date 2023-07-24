---
author: cmuk
comments: true
date: 2008-11-24 08:28:11+00:00
layout: post
link: https://mckellar.wordpress.com/2008/11/24/console-dev-week-8/
slug: console-dev-week-8
title: Console Dev Week 8
wordpress_id: 167
categories:
  - Console Development
---

This week we look in more detail at the gnu compiler and the different commands for it.
"gcc -v" command which is verbose it basically outputs what the compiler is doing.
"gcc -s" this command shows information for the separate source file such as hello_world.c
"gcc - c" this command compiles the program but does not link to the prx. It outputs binary and hex values.

We then looked at the tool chain and the different stages when compiling code. The makefile contains the parameters for how the file will be built. The "make" command will build a prx file out of the source files .c and the object files .o. "make clean" will delete all the files and build a new files much like the clean solution in visual studio.

Following on from last weeks tasks in the same group we are going to give a presentation on how you can use mutiple source files .c in the same project and how it all comes together to form one prx file. We have split the 2 source files between the members in the group and one person is writing the makefile and the main. We are doing a simple program that works out a sum and passes it onto a printer source file which then outputs it. We hope to put the code in to display it the PSP screen.
