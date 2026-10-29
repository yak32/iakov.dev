---
title: Dynamic paths in the Glow engine
description: "Why I picked Mikko Mononen's Recast library for path-finding in my engine and added support for dynamic objects to it."
date: 2009-08-18 05:17
tags: [engine, ai]
youtube: V9yTlJaXJSc
---
Here is how I got dynamic paths working in my engine.

First I went through the path-finding engines that are available and didn't find one I could use. Some cost money, and the others weren't complete enough.

A month ago I saw a demonstration of the [Recast](https://github.com/recastnavigation/recastnavigation) library by [Mikko Mononen](http://digestingduck.blogspot.com/). It takes a triangle soup, voxelises it and generates correct paths from the result. I was impressed, so I downloaded it and added support for dynamic objects. The video shows the result. I described the tile update steps in [my previous post about the Intel Level Up demo](/2009/08/intel-level-up-demo-and-dynamic-navmesh/).
