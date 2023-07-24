---
author: cmuk
comments: true
date: 2009-02-15 13:39:31+00:00
layout: post
link: https://mckellar.wordpress.com/2009/02/15/interactive-3d-graphics-directx-week-2/
slug: interactive-3d-graphics-directx-week-2
title: Interactive 3D Graphics (DirectX) Week 2
wordpress_id: 314
categories:
  - Interactive 3D Graphics (DirectX)
---

This week we learnt about Terrain, we had a lecture on terrain we looked at loading terrain in from a .RAW file and also the different techniques to procedurally generate terrain. We were given a basic Grid class and had to adapt it to make it load terrain in. It was a big step up from last weeks looking at the first few tutroials on the sample browser however i adapted to it quite well. I managed to get the terrain loading a RAW file which simply contains the bytes of the image. This required writing a heighmap class to store the heights in a list of vectors. The loader needed to look into the heightmap class and use the verts .y value to store its value.  As you can see below i have the RAW file and wireframe render of the terrain

[![](https://mckellar.files.wordpress.com/2017/10/terrainraw.png)](https://mckellar.files.wordpress.com/2017/10/terrainraw.png)[![](https://mckellar.files.wordpress.com/2017/10/terrain.png)](https://mckellar.files.wordpress.com/2017/10/terrain.png)
[![](https://mckellar.files.wordpress.com/2017/10/bart2.png)](https://mckellar.files.wordpress.com/2017/10/bart2.png)[![](https://mckellar.files.wordpress.com/2017/10/bart.png)](https://mckellar.files.wordpress.com/2017/10/bart.png)

**Fault Formation**

After loading in RAW files I had a look at Fault Formation. This algorithm starts by drawing a random line and adds an offset value to each value on one side of the line. It then decreases the height value and draws a new line. It repeats this process until a sufficient level of detail is generated. The problem with this method is at low iterations the terrain can look very unrealistic and at higher levels the terrain can appear to have lines over it like it’s been sliced as there is sharp divisions between the neighbouring cells. To get round this it goes through a low-pass image filter this makes it more smooth and realistic and simulates erosion.

[![](https://mckellar.files.wordpress.com/2017/10/terrainfractal.png)](https://mckellar.files.wordpress.com/2017/10/terrainfractal.png)

**MidPoint Displacement**

This method simulates the lateral pressure from the movement of tectonic plates which causes the surface to wrinkle up like fabric, pushing up mountain ranges. This algorithm is sometimes known as plasma fractal or the diamond-square algorithm. You start out by calculating the 5 midpoints in a rectangle these are the four sides and middle of the rectangle. Average the corner values and the midpoints of the adjacent rectangles. Add a random value between -dHeight/2 and +dHeight/2. By passing in a rough value (float) you can alter the terrain.

[![](https://mckellar.files.wordpress.com/2017/10/terrainplasma.png)](https://mckellar.files.wordpress.com/2017/10/terrainplasma.png)

**Lighting the terrain
**
To light the terrain the terrain needed normal’s rather than computing all these manually I instead converted the terrain into a mesh. This gave me access to the D3DXComputeNormals function which would create the normal’s for me however this method takes a lot to compute. I set up a basic directional light and change the render mode to solid instead of wireframe. I’m having troubles getting height based colours working it should look into the height map and return the value for y which can then be used to change the light intensity.

[![](https://mckellar.files.wordpress.com/2017/10/lighting1.png)](https://mckellar.files.wordpress.com/2017/10/lighting1.png)

This is after creating the normals and adding a white directional light. This is before i changed the lighting.

[![](https://mckellar.files.wordpress.com/2017/10/blue.png)](https://mckellar.files.wordpress.com/2017/10/blue.png)

This blue was created by using just the heightmaps y value for colour this gave it a blue tint and looks like a planet.

[![](https://mckellar.files.wordpress.com/2017/10/crazy.png)
](https://mckellar.files.wordpress.com/2017/10/crazy.png)
This multicolour effect was created by a mistake i did this by setting the y value to the z value of the heightmap colour.[](https://mckellar.files.wordpress.com/2017/10/crazy.png)
