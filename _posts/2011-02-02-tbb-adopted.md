---
title: Intel TBB is in the engine
description: "Intel Threading Building Blocks is integrated, and work starts on a concurrent, templated scene graph that several threads can read at once."
date: 2011-02-02 08:22
tags: [engine, performance, cpp]
---
Intel Threading Building Blocks is now built into the engine. It's a good library with a lot of features.

I've started on a concurrent scene graph. The scene graph (sectors and portals) is now a template, so it can hold different types of objects, and several threads (or tasks) can read it at the same time. Some engine modules also keep their own copy of the scene graph so they only deal with what they need: the renderer holds one with the visible objects, and physics holds one with just the physical objects, which keeps the simulation cheaper.
