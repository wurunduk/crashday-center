---
title: General notes
date: 2019-05-02T16:27:04.538Z
updated: 2019-05-02T16:27:04.654Z
toc: false
category:
  - Documentation
  - Other
---
* All distance units in Crashday are measured in meters, i.e. 1 unit is representing 1 meter. 
* The Crashday coordinate system is defined as follows: when looking "into your screen" the X axis goes from left to right (increasing rightwards). The Y axis defines the vertical direction from bottom to top (increasing upwards). The Z axis is the depth extension and points into the screen.
* Car models should be aligned as follows: the car's front points towards the positive Z direction, i.e. "into the screen". 
* Even when working with .dds textures, you should reference to .tga (e.g. if you specify `glass2.dds` in your car info file, define it as `glass2.tga`). Crashday internally only works with uncompressed .tga textures. Whenever it is asked to look for a certain .tga, it first checks whether a .dds alternative is available. You can for example work with .tga files only in your modeling application and even if the in-game textures are only available as .dds, this is no problem. 
* Every new texture you add requires a shader .tex file with the same name.
* In files that are based on user-readable text, the hash character "#" defines the beginning of a comment that ends at the end of the same line. Everything in the comment is ignored by the game.
* All files auto-generated for the mods by the game will be put into **crashday/user/__tmp00.cpk**. You can put those files into your mod later, so it will load faster.
* Do **NOT** use spaces or capital letters in any file names. CD will mostly likely break with those.
