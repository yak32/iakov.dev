---
title: Greedy meshing with baked ambient lighting
subtitle: Greedy mesh generation for a voxel field
description: "My greedy voxel mesh generator now supports ambient lighting prerendered into a texture, and the same mesh goes to Bullet physics."
date: 2012-11-09 09:01
tags: [game, iron-cube, rendering, lighting, voxel]
image: /assets/img/2012/11/screen_greedy_ambient_grid.jpg
---
I've upgraded the greedy mesh generation algorithm I described [in August](/2012/08/geometry-optimization/). It now supports ambient lighting prerendered into a texture. The voxel world is made of cubes, so there are only so many ways ambient light can fall on the side of a cube, and I can prerender every combination into a texture. That also answers my worry from August that vertex-based ambient occlusion would be hard to apply to the optimised mesh.

Greedy mesh generation should speed up both rendering and physics updates a lot. Voxels go to physics as a mesh, and it's the same mesh I use for rendering, passed straight to Bullet physics.

![Greedy mesh with prerendered ambient lighting and its triangle wireframe; the stats show 112 triangles](/assets/img/2012/11/screen_greedy_ambient_grid.jpg)

The previous, "dumb" mesh generation:

![The same scene with the previous mesh generation: 2176 triangles](/assets/img/2012/11/screen_grid.jpg)
