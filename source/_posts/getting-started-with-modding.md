---
title: Getting started with modding
date: 2019-05-09T17:42:43.083Z
updated: 2019-05-09T17:42:45.542Z
toc: true
category:
  - Tutorials
---
Modding Crashday is fairly easy in some aspects and incredibly difficult in others. This tutorial hopefully will help you in your journey. 

# Preparing your workspace

To start modding the game we will need some basic setup steps. Firstly, you should download _Crashday Tools_ from _Steam._ You can find them after you bought the game in _LIBRARY -> TOOLS -> Crashday Redline SDK._ This will download CD tools and put them into `Crashday/tools/` folder. Launching tools from _Steam_ will launch Crashday's workshop upload tool.

After we got the tools, it's a good idea to get reference mod content. If you go into `Crashday/data/` you will find .cpk archives with all of Crashday's data. In here you should unpack needed packages in the same folder, so you will get a content folder. To check what packages you want to unpack, visit [Content Packages](https://crashdaycenter.com/d/content-packages/).

# Understanding Crashday loading

Firstly to understand how we want to build our mod we will need to take a look at the process of mod loading. In general, it looks like this:\
At first stage the game takes all the .cpk files from `Crashday/data/` and unpacks them into some imaginary folder (Just like we did). If any of the original files are edited or corrupted at this point, the game will crash on us.\
After that, the game starts to unpack mods from workshop in to the same imaginary folder, in order from top to bottom of our launcher list, overwriting original files if necessary. This way mods can add their own files to the game system, as well as overwrite original ones.

If user has enabled _mod development mode_ in the launcher, our test mods will also be loaded after that. These can be placed as .cpk archives in `Crashday/user/` folder, or as uniquely named folders in `Crashday/user/mod_testing/`

# Creating your first mod

Now as we got the basics out of the way, lets create a simple test mod. If we take a look at the `content` folder of our unpacked packages, we can see a `dbs` folder containing `game.dbs` file. This file has all the different common parameters the game uses. Lets try and edit it!

Now head to `user/mod_testing/` and create a folder named `my_awesome_mod`. As you remember, now contents of this folder will be dropped into our imaginary CD folder and after that the game will load. This means if we want to change the game.dbs file of the game, we need to replace the original on game load. If the original file lies in `imaginary_folder/content/dbs/game.dbs` we need to put ours in `my_awesome_mod/content/dbs/game.dbs`, so it overwrites the original. 
So enter our folder and create `content` folder, in which we need our `dbs` folder. As we want to edit .dbs file, we can just copy the original from our unpacked reference and copy it into our mod folder. Now we can edit it. Most of Crashday files, as well as .dbs can be opened with a text editor. For more info about every type file visit [File Types](https://crashdaycenter.com/d/file-types/). After opening it you will see a list of all Crashday's parameters.

Let's change `Physics.Gravity 9.806650` to `Physics.Gravity 3.1415` and save the edited file.

Now launch Crashday, select _MODS_ and enable _mode development mode._ 

> If you encounter any bug while testing your mod, or the game takes to long to load, try the _Disable workshop mods_ option. It will not load any workshop mods, but will still load testing mods.

Now we are ready to play and test the mod! If you did everything correctly, after launching any mode you should have much lower gravity. Congratulations, your first mod is ready!
