---
title: Recast navigation with the Havok physics engine
description: "A video of Recast navigation meshes running together with the Havok physics engine in my engine."
date: 2009-10-20 10:26
tags: [engine, ai]
youtube: WzFJMvE0L60
---
This video shows [Recast](https://github.com/recastnavigation/recastnavigation) navigation working together with the Havok physics engine.

Recast builds the navigation mesh, and in August I added support for dynamic objects to it. Havok handles the physics. Anything that physics pushes around has to be taken into account by the navigation mesh, which is the job of the tile updates I described in [my post about the Intel Level Up demo](/2009/08/intel-level-up-demo-and-dynamic-navmesh/).
