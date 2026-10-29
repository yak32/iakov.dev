---
title: 6000 animated entities in the Glow engine
subtitle: A performance test of the Glow engine
description: "A Glow engine performance test with 6000 animated entities in one frame and no special optimisation such as instancing."
date: 2012-12-06 02:53
tags: [engine, performance]
youtube: NSS2AC4OMFY
---
The video above is a stress test of the Glow engine with 6000 animated entities in one frame.

There is no special optimisation in this scene. I haven't used instancing, the usual way to draw thousands of copies of the same thing cheaply, so every entity goes through the normal rendering path. It can go faster than this.
