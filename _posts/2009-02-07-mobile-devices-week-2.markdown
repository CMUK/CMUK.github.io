---
author: cmuk
comments: true
date: 2009-02-07 13:21:29+00:00
layout: post
link: https://mckellar.wordpress.com/2009/02/07/mobile-devices-week-2/
slug: mobile-devices-week-2
title: Mobile Devices Week 2
wordpress_id: 253
categories:
  - Mobile Devices
tags:
  - J2ME
  - Java
  - Mobile
---

This week we learnt about **MIDlets**. This term means an application that runs under **Mobile Information Device Profile (MIDP)**.  So basically applications for mobiles, We looked the three abstract methods contained in the MIDlet class. these are:

-startApp - used to start the application can be called more than once.
-pauseApp - used for if someone is calling you it must stop any non essential threads.
-destoryApp - must terminate the application gracefully so saving any scores,progress. must terminate all running threads to stop memory leaks.

These must be implemented for the application to work.

MIDP applications have to run on many different devices from phones to pda's. The user interface has two ways of creating **Abstraction** or **Discovery**,

Abstraction - sets up the location of fields relative to the device.
Discovery - gives you control on where you place fields.

We then looked at **Commands** which are same as buttons such as Command.Exit.

This weeks task was to create a MIDlet application which took userinput and displayed it on screen. I found this quite easy as it was similair to C#. I did have to look up the different properties of TextField and the ChoiceGroup to work out how to do the different radio boxes. I have got the radio boxes working but im still having trouble displaying if more that one choice has been selected.

[![](https://mckellar.files.wordpress.com/2017/10/javatask.png)](https://mckellar.files.wordpress.com/2017/10/javatask.png)
