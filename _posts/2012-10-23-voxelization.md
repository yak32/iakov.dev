---
title: Automatic voxelisation of a 3D model
description: "I voxelised a tank model into a 50x50x50 voxel field by rasterising it polygon by polygon, much like a 2D scanline algorithm."
date: 2012-10-23 17:46
tags: [game, iron-cube, voxel]
---
I've been playing with automatic voxelisation of a 3D model, using the tank for my new game as the test.

The original model:

![The original polygonal tank model](/assets/img/2012/10/tank_original.jpg)

The model after voxelisation:

![The same tank after voxelisation into a 50x50x50 voxel field](/assets/img/2012/10/tank_voxelized.jpg)

I voxelised it into a 50x50x50 voxel field, so the resolution definitely needs to go up. The model is rasterised into the voxel field one polygon at a time, in a similar way to the 2D scanline algorithm.
