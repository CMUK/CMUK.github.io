---
author: cmuk
comments: true
date: 2013-05-12 14:46:58+00:00
layout: post
link: https://mckellar.wordpress.com/2013/05/12/leap-motion-bowling/
slug: leap-motion-bowling
title: Leap Motion Bowling
wordpress_id: 833
tags:
  - Csharp
  - Leap Motion
  - Programming
  - XNA
---

Leap motion is due out in the next few months, I was lucky enough to get on the developer program and was sent a development kit, I decided to make a bowling game which uses your index finger to control the game.

![](https://images-na.ssl-images-amazon.com/images/I/713rS-8XOJL._SX1200_.jpg)

![Bowling1.PNG](https://mckellar.files.wordpress.com/2013/05/bowling1.png)![Bowling2.PNG](https://mckellar.files.wordpress.com/2013/05/bowling2.png)

Simple controls are:

extended index finger moving left and right moves the ball left and right.

extended index finger moving your arm back controls the power of the shot.

more than one finger detected launches the ball.

I used XNA as the game engine as I have a lot of past experience with it and could quickly get a game up and running. For the physics I used the [BEPU Phsyics engine](https://bepuphysics.codeplex.com/).

For leap motion I used LeapCSharp.NET4.0.dll to hook into.

Movement constrained to the x axis:

<blockquote>if (leapRunner.fingerCount > 0 && !ballLaunched)
{
var position = leapRunner.fingerPosition.z * 0.2f;
Camera.Move(new Vector3(leapRunner.fingerPosition.x * 0.1f + 10f, Camera.Position.Y, MathHelper.Clamp(position, 43, 57)));
}</blockquote>

Launch ball:

<blockquote>if (leapRunner.fingerCount > 1 && !ballLaunched)
{
bowlingBallSphere.IsAffectedByGravity = true;
ballLaunched = true;

power = (leapRunner.fingerPosition.z \* 0.2f );
if (power > 50)
{
power = 50;
}

bowlingBallSphere.LinearVelocity = new Vector3(0, 0, -1) \* power;

}</blockquote>

https://youtu.be/3OlQ6Km6_XI

Leap motion is a great fun to develop for and will only get more accurate in the future, personally I will not be developing apps or games aimed at the leap motion as I don't think the market is ready just yet, I will however keep a close eye on devices such as leap motion and any virtual reality devices.
