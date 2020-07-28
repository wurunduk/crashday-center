---
title: Shared Textures
date: 2019-09-21T14:48:37.610Z
updated: 2019-09-21T14:48:37.632Z
toc: false
category:
  - Documentation
  - Textures
---
Shared textures are textures that you can use in your model, without needing them in your mod's .cpk. Every texture that's located exactly in the `textures` folder, is considered a shared texture and can be used by any other mod. This includes the textures of all tiles, dynamics, pickups, wheels, drivers, etc.

The most important textures are the ones the base game cars use for miscellaneous parts, like *rubber*, *glass*, *carplas2*. These are just textures with usually a solid color, but with carefully made .tex files to make them look like their name would suggest. It is recommended to use these in your mod, because most of the time it's a simple time save, but adds much quality. Here's most of them:

* **"carplas2"**
  Perhaps the most commonly used and best looking shared texture, just a simple grey/black plastic texture. Could be used for any simple plastic part and even full bumpers.
* **"carplas3"**
  A reflective, black plastic texture. Could be used for the trim on the edges of glass for example. (the part connecting the roof and body on the Apachee for example)
* **"rubber"**
  As the name suggest, a black rubber texture. Mostly used to seperate the car body and the windows.
* **"glass"**
  Reflective, transparent glass, with a slight bit of a blue tint. Used for car windows. Has a damage map counterpart named **"glass2"** (use that to UV map your windows to).
* **"carplast"**
  A light grey, bright version of **carplas2**. Rarely seen use on cars.
* **"lighchrm"**
  A quite reflective chrome texture. Mainly used for chrome like surfaces in headlights, though can be used for other smaller parts like exhausts or trim pieces.  
* **"chrome01"**
  The main chrome texture, a slight bit darker and less reflective then **lighchrm**. This is the intended texture for trim pieces, and other bigger chrome parts. (The Ironhorze's trim pieces for example)
* **"chrome02"**
  An alternative to **"chrome01"**, slightly brighter version.
* **_"colblck", "colwhite", "colred" and "colgrey"_**
  Non reflective, just solid colors of black, white, red and grey respectively.
