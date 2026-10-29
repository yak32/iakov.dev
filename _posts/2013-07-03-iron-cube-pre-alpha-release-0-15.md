---
title: Iron Cube 0.15
subtitle: Tank multiplayer combat in a voxel world
description: "Iron Cube 0.15 adds AI bots, dynamic navigation meshes, flood-fill voxel lighting, an OpenGL renderer with water and a working level editor."
date: 2013-07-03 07:31
tags: [game, iron-cube]
youtube: gOde2vm685M
---
[![Download Iron Cube 0.15 from Mod DB](http://button.moddb.com/download/medium/56386.png)](http://www.moddb.com/games/iron-cube/downloads/iron-cube-015)

I spent several weeks preparing this Iron Cube release, version 0.15. It has a lot of new features: AI bots, dynamic navigation meshes, new voxel-based lighting, and a new OpenGL renderer with water.

The AI bots are in the game now, and they are fairly smart. A bot can still shoot a teammate who wanders into its line of fire, but I will fix that soon. Bots follow their leader (the player), find a good route to the enemy and move out of the player's way. I'm already wondering how to make them a little dumber.

The bots use a new navigation system built on an updated version of the Recast library. The navigation meshes are dynamic: when voxels change, the meshes are rebuilt.

![AI bots moving across a voxel level in Iron Cube](/assets/img/2013/07/iron_cube_ai.jpg)

Here is how the dynamic navigation meshes work:

{% include youtube.html id="I1bS-wjuFks" %}

The new lighting system is voxel-based. Sunlight is ambient and gives smooth shadows, or as smooth as the pixelated style allows. It works as a modified flood fill of skylight from the top of the world down.

![Iron Cube level lit by the new flood-fill skylight](/assets/img/2013/07/iron_cube_lighting.jpg)

I also switched the renderer from DirectX with deferred shading to OpenGL with simple voxel-based lighting, so the game will be ready for mobile ports later. It is faster, and you can play it on old hardware.

A lot of the work went into the editor, which is now fully functional. You can render arbitrary polygonal models into the voxel world, edit the meshes, and set up lighting and AI.

This puts me one step closer to the final release.
