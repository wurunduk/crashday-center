---
title: Launch parameters
date: 2019-05-24T12:06:24.864Z
updated: 2019-05-24T12:06:26.588Z
toc: true
category:
  - 'CD:RE SDK'
  - Misc
---
Crashday has multiple launch parameters but sadly none were described by the devs. If you find how any of the parameters behave and it is not written here already, let us know!

To launch a game with any of the parameters, right click the game in _Steam_, select _Properties_, click "_Set Launch Options_". Write any parameters you want, separated with a space.

Here is a list of known parameters:

* \-windowed (Launches the game in window)
* \-skiplauncher (Skip the launcher and load the game with the last used settings)
* +connect_lobby _lobbyid_ (instantly connect to the lobby with given _lobbyid_ on launch)
* +connect (unknown? same as +connect_lobby?)
* +password (use this password when joining a lobby)
* \-watcher
* \-override_mods
* \-show_diffuse 
* \-show_shadows (in game will show were textures are applied by the game. Textures will be white)
* \-show_texture 
* \-show_alpha (instead of the textures will draw it's alpha channel)
* \-disable_postfx (disable all screen effects when drawing)
