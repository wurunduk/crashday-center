---
title: Paint.net tips and tricks
date: 2020-04-24T09:40:42.599Z
updated: 2020-04-24T09:40:43.414Z
toc: true
category:
  - Tutorials
---
### **Introduction**

Paint.net is a free program and relatively simple in terms of interface and UI compared to it's other 'rivals', like Gimp or Photoshop, while still featuring many tools and features, like layers and effects. Such effects and adjustments can still be expanded thanks to Paint.net's community based focus and customizable nature, with the help of plugins, some of which are very useful for modding this game. So overall, thanks to it's simplicity, it's recommended for beginners, and thanks to it's customizability it's very useful to more advanced modders aswell.  [Download here](https://www.getpaint.net/download.html)

With that out of the way, it should be noted that these tips will be more focused for more novice users, who want to improve their work's quality and/or create mods in similiar quality to the vanilla assets (or even better).

### **Layer types**

These can be chosen by clicking *Wrench* icon *(a.k.a. Properties)* on the *Layers* window, while having your desired layer selected. They are best explained on their official page [here](https://www.getpaint.net/doc/latest/BlendModes.html), and it's probably best to look at it in Paint.net yourself for experimenting, but there's one mode that's universally used for all vanilla game liverys:

**Multiply:** This, when added to an above layer, takes the colors of the layer below it, and multiplies/mixes them together, making the above layer a sort of mask. 

With *Normal* Blend Mode

![](/media/multip_layer1.png "On *Normal* Blend Mode")

With *Multiply* Blend Mode

![](/media/multipl_layer2.png "On *Mutiply* Blend Model")

This is very useful sort of 'baking' liverys onto an Ambient Occlusion baked body texture and if you want to replicate how vanilla game liverys look like (as they were probably made this exact way).\

### **The Alpha Channel and Masks**

To make most use of the method above and have parts of the car body paintable ingame, you will have to utilize Alpha Masks, but first, a little introduction to the Alpha Layer or Channel itself. 

The Alpha Channel is present in any image supporting transparency, and it basically defines how transparent parts of the image should be using the RGB values in the channel. While it can use any type of image, even colored ones as an alpha layer, the channel will always be greyscale when it's used as an Alpha Layer, so it's more practical to create the Alpha Masks in black and white, so you even see the exact opacity values easier thanks to the RGB values being the same.

The above mentioned Alpha Mask is the actual image that gets used as an alpha layer for your texture, and when it's applied, part of the image will turn transparent or half-transparent according to the black and white parts in the Alpha Mask.

More explanation W.I.P.