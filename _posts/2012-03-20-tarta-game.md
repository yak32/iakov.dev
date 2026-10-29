---
title: "New game prototype: Tarta"
description: "Tarta is a new voxel game prototype built in three weeks: an infinite random voxel world, terrain editing, a day/night cycle and PhysX."
date: 2012-03-20 14:41
tags: [game, voxel, rendering, lighting]
youtube: -Q3I_B19HCQ
---
I've started a new game prototype called Tarta. The video above is from the first prototype, which took 3 weeks to build.

So far the prototype has:

- an infinite random voxel world based on Perlin and Simplex noise
- landscape editing, either one voxel at a time or by volumes (boxes, spheres and so on)
- a day/night cycle
- physics through PhysX (press F5 to turn it on)
- HDR, lens flare, dynamic shadows, reflective and refractive water and deferred shading, all from the Glow engine

<!--more-->

It's obviously inspired by Minecraft, but it goes in a different direction. It will be more about survival, with various enemies and more shooter and adventure elements, and terraforming will play a big part in the gameplay. The gameplay document already runs to several pages of ideas.

Another video, showing a volume (a sphere) extracted from the voxel landscape:

{% include youtube.html id="p3I_j0qnuKg" %}

I've spent some time looking at Minecraft clones. Nearly everyone tries to make an exact copy, just with uglier or prettier graphics. Add sophisticated shaders, depth of field, dynamic clouds, SSAO, whatever you like, and bam, you have millions in your pocket. (The maker of Minecraft Fortress already got there.) The most interesting one I found is this:

{% include youtube.html id="ci9KzKEDLFk" %}

The gameplay possibilities of a voxel engine are endless, though. I deliberately haven't played Minecraft, so I can't copy its ideas even by accident.

I'll post the first prototype here later.
