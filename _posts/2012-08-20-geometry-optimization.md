---
title: Geometry optimisation for voxel meshes
description: "A new voxel mesh generator cuts vertex data by a factor of three to four, at the cost of slightly slower generation."
date: 2012-08-20 13:04
tags: [engine, voxel, lighting, performance]
image: /assets/img/2012/08/screen_detail1.jpg
---
I've optimised the mesh generation. Until now the voxel mesh was generated as is, and the only thing I removed was the internal faces. That produces a huge amount of vertex data, which is slow to load into the GPU, slow to process on the CPU, and so on.

The new algorithm reduces vertex data by a factor of three to four, though it makes mesh generation slightly slower. There is one more possible downside. The result is no longer a regular mesh, so ambient occlusion based on vertices will be hard to apply. I hope my version of SSAO will handle it.

This is the new version of the mesh generation:

![Voxel terrain built with the new optimised mesh generation](/assets/img/2012/08/tarta_greedy1.jpg)
