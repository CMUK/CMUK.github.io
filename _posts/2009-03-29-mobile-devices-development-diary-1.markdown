---
date: 2009-03-29 18:12:13+00:00
title: Mobile Devices Development Diary 1
categories:
  - Mobile Devices
---

Sunday 29th March – The start

Today I started my Battleships project, I started off by planning out what to do. I wrote down a few ideas for implementation of battleships. I decided to go with the approach of making one grid to start off with, this will make it easier for me to develop around. I looked at game canvas and how to draw sprites to the screen. After doing researching into graphics I have decided to go with Tiled Layers. These enable me to do animation and keep all my images in one image. After having a play about with a Tiled Layers example I began making a grid. I had to take into account the size of the grid and how big the squares are to make the game last longer. I decided on making an 8x6 grid size which takes up about half the screen on the mobile device. The great thing about tiled layers is it acts as a 2D array allowing you to get the contents with a simple getCell(x, y) or setCell(x,y,value). Using two for loops nested I can set the cell to = the tile index in the image. Filling the grid with the first index in the image set my grid up. This was my first Phase milestone 1 reached.
