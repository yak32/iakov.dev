---
title: CPU voxel lighting in Iron Cube
subtitle: New voxel-based lighting
description: "Iron Cube gets new CPU-calculated voxel lighting, split into sky and local light and baked in the editor to help mobile devices."
date: 2013-03-29 12:18
tags: [game, iron-cube]
image: /assets/img/2013/03/iron_cube_lighting.jpg
---
I implemented new lighting for Iron Cube that runs on the CPU, which makes rendering easier on mobile devices.

There are two parts, sky lighting and local lighting. The sky emits light from the top of the voxel world downwards, so it casts shadows and makes caves darker. Local lights don't have shadows yet, but they do use the normals of objects.

All of it is calculated in the editor and saved to the level file. On a phone the game only has to load the result, which keeps loading times down.
