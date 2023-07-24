---
author: cmuk
comments: true
date: 2010-11-12 20:06:40+00:00
layout: post
link: https://mckellar.wordpress.com/2010/11/12/ai-generic-perception-system/
slug: ai-generic-perception-system
title: AI Generic Perception System
wordpress_id: 522
categories:
  - AI
---

In this project I made an AI perception demo based on Frank Puig Placeres in the AI Games Programming Wisdom 4 book, AI perception means perceiving the world around you and making sense of it to use for decisions. The article explains two types of sensing static and dynamic sensing, in static sensing the AI will detect walls and stationary objects, in dynamic sensing it will sense anything which moves this can also be footsteps or audio sensing such as noises.

The AI agent will have sensors which it needs based on its type, such as a guard would have a tactical sensor which scans for ambush points and good spots to hide or use for combat, An environment sensor to detect walls and obstacle, a beacon sensor to detect dynamic objects or sensors.

All the information that gets detected by the agent gets processed and acted upon it is important to note the agent is trying to simulate human behaviour and sensors, Games which make full use of AI perception tend to be of the stealth genre, these perceptions have to be very fast, reliable and quite complex, splinter cell for example the AI has to seem intelligent and life like by responding to events the player causes such as, throwing a bottle near the AI it should detect a noise and work out roughly where it got thrown from,  The AI won’t need to fully sense like humans it will reject sensing something humans cant, for example it won’t detect noises far away unless instructed to, it also only cares about agents and players close to them, even the sense time is not realistic in speed and reaction but is good enough to fool the player and free up more CPU cycles for other areas such as physics calculations.

In my demo I use an environment sensor for walls and barrels, various beacon sensors for detecting footsteps, gunshot sounds, dead bodies and enemies

[![](https://mckellar.files.wordpress.com/2017/10/demo.jpg)](https://mckellar.files.wordpress.com/2017/10/demo.jpg)
http://www.youtube.com/watch?v=52U3mW9NpHg
