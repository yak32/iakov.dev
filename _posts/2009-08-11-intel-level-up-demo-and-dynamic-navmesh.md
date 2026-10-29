---
title: Intel Level Up demo and dynamic navigation meshes
description: "I finished my Intel Level Up 2009 demo, and here is how the dynamic navigation meshes in my engine rebuild tiles when objects move."
date: 2009-08-11 09:25
tags: [engine, game, rendering, ai, contest]
youtube: Y4KM32uYOgY
---
Today I finished the game demo for Intel Level Up 2009. It cost me three nights without sleep. Some things are still not implemented, but the overall picture is good. I'll prepare a longer video and the demo itself later.

For now, here is a short video of the dynamic navigation meshes in my engine. They are based on TileMesh and they are fast: the whole level (300x300) builds in a separate thread in 5 seconds on a single-core PC, with a tile size of 32. Don't look at the frame rate. That's deferred shading on an old PC.

<!--more-->

Here is how it works:

1. Render the static mesh and keep it.
2. Render the dynamic objects and remember which objects sit in each tile.
3. When an object moves, add the tile under its old bounding box to the update list.
4. If an object that hasn't moved intersects a tile being updated, add it to that tile too.
5. Render the updated tiles with their objects.
6. Connect the tiles into the mesh with the Recast library.
