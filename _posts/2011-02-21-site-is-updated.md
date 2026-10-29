---
title: Updated glow3d.com
description: "glow3d.com now matches the current state of the Glow engine after the recent concurrency work."
date: 2011-02-21 07:20
tags: [personal]
---
I've updated www.glow3d.com so it reflects the recent changes to the engine.

Most of those changes are about concurrency. The Glow engine now runs its tasks on Intel Threading Building Blocks instead of boost::thread_pool, and the scene graph of sectors and portals is a template that several threads can read at once. The renderer and physics each keep their own copy of it. None of that was on the site yet, so it needed a refresh.
