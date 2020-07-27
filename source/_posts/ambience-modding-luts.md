---
title: 'Ambience modding: LUT''s'
date: 2019-05-09T19:20:15.970Z
updated: 2019-05-09T19:20:17.653Z
toc: true
category:
  - Tutorials
---
Crashday now supports color LUT's (Lookup Table) which allow much easier color management for ambience mods. You can think of a LUT as an actual table. Before rendering any frame, the game will get every pixel, take it's color as a position of the table. Look at our LUT and change the starting pixel to the pixel in the table. Luckily, a lot of modern painting software let's us work on LUT's easily.

To get started, download the following [neutral color LUT](https://cdn.discordapp.com/attachments/556249164900466688/570278209430618113/neutral_lut.tga) and place it in `user/mod_testing/[modname]/content/textures/ambience`.

At this point, we should decide which ambience we want to base our mod off of. I'll choose the Day ambience, meaning I'll copy the following files from our previously created reference directory `content/textures/ambience`:

* day.tex
* day.tga
* day_bd.dds
* day_bg.tex
* day_lut.tex
* day_lut.tga
* dayh.tex
* dayh.tga

and day.amb from `content/ambience`

If you want to just slightly adjust the feel of the existing ambience, feel free to open the `day_lut.tga` with your image editor. But if you want to make new and precise look, replace `day_lut.tga` with the `neutral_lut.tga` we downloaded, and open it.

What you are looking at now, is our color Lookup Table. As you might notice, the image has a resolution of 16x16x16. Wait what? Yes. This is actually a color cube, where each axis represents a basic color channel (red, green and blue). After that the cube was sliced on the blue axis and the slices were stacked to the right. 

![Color cube sliced explanation](/media/color_cube_explanation.png "Color cube sliced  explanation")

As stated before, the game looks at the coordinates of the frame's pixel and takes the color of the lut at given position. This means, that if you were to make this LUT "negative", all the 3D rendered objects in the game will appear in negative. Feel free to try it if you'd like!

There are many other things one can do with the LUT, like simulating color blindness (there are mods for that on the Workshop, actually), black and white, sepia effects. 

But also we can make really small and nice looking adjustments now. Firstly, we're going to need to make some reference images. Start the game with mod_testing enabled and making sure to select the Day ambience we are overwriting, take some screenshots that will make good references. Make sure you capture shadows, various greens, industrial tiles, cars, etc. Also make sure you capture them losslessly, using the print-screen button on your keyboard, or otherwise a program that saves them as _PNG_ or _BMP_ will do just fine.

Now import the best reference shots into your picture editing project and create an image of all the useful portions of the reference shots. After doing that, I recommend putting the LUT layer in there in the top-let corner, so we can easily grab it later.

Now we can start adjusting the colors. Using our reference images we'll be able to tune the colors to get the result we want. Make sure that any color corrections you make are applied to the layer with the LUT!

Please refrain from using tools or plugins that only affect a limited range. This can quickly cause artifacts that will be noticeable in-game. Brightness, Contrast, Hue, Saturation are all great tools. You can also adjust color curves if you wish.

Do NOT use things like blur, glow, sharpen and so forth, as the results of those won't translate to the game. Remember, we are adjusting colors via a color lookup table. That's all the game is able to read from the LUT.

When you're satisfied, go the Canvas Resize the image and Anchor is to the Top-Left. Enter 256 for width and 16 for height. If you put your LUT in the top-left, you'll end up with only our Color LUT afterwards!

Now save the LUT over the old `day_lut.tga` and test your ambience in-game! If you still want to make some adjustments, just undo a few steps until you have your reference images back and adjust some more from there.
