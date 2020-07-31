---
title: Publishing and updating workshop items
date: 2019-05-09T18:58:51.073Z
updated: 2019-05-09T18:58:52.417Z
toc: true
category:
  - Tutorials
---
So you have got your amazing mod or map ready to share with the rest of the world? Nice, you came to the right place.

# Publishing to workshop

## Mod packing

You only need this step if you are uploading a mod. Head to your `user/mod_testing` folder and find the mod you want to publish. Now you want to put the contents of that folder into a .zip archive. This step is different depending on what archiver you have, but make sure you are packing into **`.zip`** archive. After you have done that make sure that when opening, the only folder there is `content`. After that rename the extensions of the file to `.cpk` instead of `.zip`. Now we are ready to publish it. 

## Publishing

Launch _Crashday tools_ from `Steam` or `cdwstool.exe` from `Crashday/tools` folder. After the tools are loaded, click _Publish Workshop Item._ The new window will appear, where you need to fill the mod or map name, description and picture.

* **Title**: the name of the track that will be showed in _Steam Workshop_. Please note that only ASCII characters are supported.
* **Preview**: the image of the track or mod as shown in _Steam Workshop_. Must be _JPG_ or _PNG_ with less than 1MB. Use "_Browse..._" to upload the image from your hard drive.
* **Visibility**: sets the visibility of your item on _Steam Workshop_.
* **Tags**: for tracks, select checkbox "Track" and leave the other checkboxes rest blank. For mods select one or multiple tags, except "Track" describing your mod.
* **Content**: select the `.trk` map or `.cpk` package you want to upload. For tracks please note that the name of the file will be displayed as the name of the track in-game as well (e.g. "finals2.trk" will show up as "finals2" in-game)
* **Description**: the text description of the item shown in _Steam Workshop._
* **Item Id**: if you are uploading a new track or mod, leave this blank. 
  * If you want to update an existing track or mod, please enter the Id of your previously created Workshop item here. You can obtain the ID from "Your Workshop Items" inside the Mod Uploader tool.
* **Submit**: Click this when you are done. Congrats, your mod should be uploaded!
