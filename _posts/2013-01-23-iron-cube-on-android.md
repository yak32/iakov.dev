---
title: Iron Cube on Android
description: "A video of Iron Cube running on a Galaxy Note 2. Movement, shooting and rendering work; sound and AI are still to do."
date: 2013-01-23 15:27
tags: [game, iron-cube, rendering, ai, android]
image: /assets/img/2013/01/iron_cube_android.jpg
youtube: dqQ7ZjHgpYk
---
I made a video of [the Iron Cube game](http://www.moddb.com/games/iron-cube) running on a Galaxy Note 2. Movement, shooting and rendering are done, and what's left is sound and AI.

For AI navigation, the voxels can go directly into the [Recast](https://github.com/recastnavigation/recastnavigation) navigation library. The other option is to build navigation meshes from the final optimised mesh, the way I already do for physics.
