---
title: Shared Textures
date: 2019-09-21T14:48:37.610Z
updated: 2019-09-21T14:48:37.632Z
toc: true
category:
  - 'CD:RE SDK'
  - Misc
---
Basically, Shared textures are textures that you can "refer" to in your model, without needing them in your mod's .cpk. Every texture that's located in the _textures_ folder, but not another folder in that folder, is considered a shared texture. This includes the textures of all tiles, dynamics, pickups, wheels, drivers, etc.

The most important textures are the ones the base game cars use, like rubber, glass, carplas2. These are just textures with usually a solid color, but with carefully made .tex files to make them look like their name would suggest. It is recommended to use these in your mod, because most of the time it's a simple time save, but adds much quality. Here's most of them: (pictures soon!)

* **_"carplas2"_**\
  Perhaps the most commonly used and best looking shared texture, just a simple grey/black plastic texture. Could be used for any simple plastic part and even full bumpers.
* **_"carplas3"_**\
  A reflective, black plastic texture. Could be used for the trim on the edges of glass for example. (the part connecting the roof and body on the Apachee for example)
* **_"rubber"_**\
  As the name suggest, a black rubber texture. Mostly used to seperate the car body and the windows.
* **_"glass"_**\
  Reflective, transparent glass, with a slight bit of a blue tint. Used for car windows. Has a damage map counterpart named **"glass2"** (use that to UV map your glasses to).
* **_"carplast"_**\
  A light grey, bright version of _carplas2_. Rarely seen use on cars.
* **_"lighchrm"_**\
  A quite reflective chrome texture. Mainly used for chrome like surfaces in headlights, though can be used for other smaller parts like exhausts or trim pieces.  
* **_"chrome01"_**\
  The main chrome texture, a slight bit darker and less reflective then lighchrm. This is the intended texture for trim pieces, and other bigger chrome parts. (The Ironhorze's trim pieces for example)
* **_"chrome02"_**\
  An alternative to **"chrome01"**, slightly brighter version.
* _**"colblck", "colwhite", "colred" and "colgreyl"**_\
  Non reflective, just solid colors of black, white, red and grey respectively.
