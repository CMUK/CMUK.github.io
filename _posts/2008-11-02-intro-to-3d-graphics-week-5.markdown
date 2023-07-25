---
date: 2008-11-02 12:17:25+00:00
title: Intro to 3D Graphics Week 5
categories:
  - Intro to 3D Graphics
---

This week i have been looking at getting the model to display on screen using GUI. I have had to implement a couple of new classes such as the MyApp class which is used as the rendering pipleline this is where everything gets made and rendered to the screen. I have ran into a few problems with implementing this but should get this sorted out tomorrow. Everything else is working good i manged to get my model loader working which takes basic MD2 files and stores there polys and verts into an array which will be used to display the model to the screen. In the lecture we learnt about FOV in games and how it works which is just modifying the view frustrums horizontal and vertical FOV angles. We then looked at the view frustrum and its near and far clip planes we looked at a video of the game Turok which showed bad far clipping distance and was masked with fog.

{% include video id="PaBUQexnSfI" provider="youtube" %}

### **Simulating lighting in the virtual world**

**Local lighting**

This where the object lights itself none of the other objects in the scene matter. It only uses ambient, directional, point and spotlights.

**Global illumination**

This is where all the objects get lit from a source and provides more realistic lighting reflections, refractions, and shadows.

### **Types of Light Sources**

**Ambient**

Ambient light is constant colour that doesnt appear to be coming from a fixed position. It lights the whole scene.

**Directional**

A point in space far away with lights pointing in the same direction. Typical example is the sun in the scene.

**Point (omni or spherical lights) **

A point light is light emitting from a singe point the center going in every direction and creating like sphere shape with the light intensity decreasing futher away from the center. Examples include light bulbs, lamps, fires.

**Spotlight**

The spotlight has a position and a direction. It produces a cone like shape. It is used in flashlights, headlights and spotlights.

**Phong Reflection Model**

This model gets the light reflection off the object to our eyes giving it a shiny appearance.

![](http://upload.wikimedia.org/wikipedia/commons/thumb/6/6b/Phong_components_version_4.png/800px-Phong_components_version_4.png)

**Types of Shading**

**Flat Shading**

This is where it uses a single light value for the entire triangle. Star fox is a game which uses this technique.
**
Gouraud Shading (vertex shading or interpolated shading)**

The lighting is done at vertex level. These values are then linearly interpolated
across the face of the polygon
