---
title: Ambient lighting with vertex colours
subtitle: New ambient lighting implementation
description: "I moved Iron Cube's ambient lighting into vertex colours. It looks the same as before but should render faster."
date: 2014-09-24 13:48
tags: [game, iron-cube, rendering, lighting, voxel]
image: /assets/img/2014/09/ambient_vertex_colors.jpg
---
I rewrote the ambient lighting in Iron Cube. The ambient term is now stored in the vertex colours of the voxel mesh.

The screenshot from the editor shows the result on plain white voxels. The tops of the stepped hill are lit from above, while the sides and the gaps between the steps go dark.

Visually there is no difference from the old version, but it should be faster. Iron Cube also runs on Android phones, so every bit of rendering time I save counts there.
