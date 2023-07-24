---
author: cmuk
comments: true
date: 2009-02-15 10:31:41+00:00
layout: post
link: https://mckellar.wordpress.com/2009/02/15/mobile-devices-week-3/
slug: mobile-devices-week-3
title: Mobile Devices Week 3
wordpress_id: 305
categories:
  - Mobile Devices
---

This week we learnt about Displayable Objects. We looked at classes that inherit from screen these were Alert, Form, List and TextBox. The changes to these are displayed instantly with no refresh to the display. Using the List object then adding something to the list automatically rearranges the list.

**Canvas**

This is the base class for handling graphics calls in order to use it you must make a subclass of it. It gives you methods to handle key events, game actions and pointer events.
**
GameCanvas**

This is a sub-class of Canvas that is used heavily in gaming. It provides off-screen graphics buffer and ability to query key state.

Paint() is abstract and must provide implementation in the subclass.
