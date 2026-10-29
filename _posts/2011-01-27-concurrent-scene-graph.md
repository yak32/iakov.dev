---
title: Concurrent scene graph
subtitle: Multithreading
description: "Three ways to give physics, audio and rendering concurrent access to the Glow engine's scene graph, and the trade-offs of each."
date: 2011-01-27 01:42
tags: [engine, rendering, physics, performance, android]
---
I am thinking about a concurrent scene graph.

Several modules in the engine need to query the scene graph: physics, audio, rendering. In the future, several threads (tasks) inside a single module will also need concurrent access to it.

<!--more-->

I see a few ways to do this:

1. A copy of the scene graph in every module. This approach is [used](https://dl.acm.org/citation.cfm?id=569679) in OpenSceneGraph too. It needs more memory, but each copy only has to hold the object types its module cares about, so the physics module holds only physics objects and so on. It still doesn't solve concurrent access within a module later on.
2. Concurrent containers in the scene graph. Maybe the best solution, but I can't find a good fit for it yet. It also looks hardware-dependent and not robust enough. Intel Threading Building Blocks has concurrent containers, but [it's not perfect](http://software.intel.com/en-us/forums/showthread.php?t=60494) and doesn't support Android or iOS.
3. Mutexes around the queries. A mutex [is not a good thing](http://www.1024cores.net/home/lock-free-algorithms/scalability-prerequisites) for scalable multithreading, but for some usage patterns it may be fine. In my case the pattern is a single producer with multiple consumers.

Can anyone suggest robust cross-platform concurrent containers? A hash_map or a vector at least.

[1024cores.net](http://www.1024cores.net/) is an excellent blog about concurrency and scalability.

Update: I was wrong about Intel TBB. It is a powerful library. I am not yet sure how to use it on iOS or Android, but it is open source and ports exist for different platforms.
