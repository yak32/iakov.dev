---
title: Deferred reflections
description: "How the Glow engine does planar reflections with deferred lighting, using the deferred reflections idea from Metro 2033."
date: 2011-12-26 02:04
tags: [engine, rendering, lighting]
image: /assets/img/2011/12/glow_deferred_reflections.jpg
---
I spent a long time thinking about how to do planar reflections in an engine with deferred lighting. Rendering the lit scene, shadows included, into a separate render target is very expensive, because it doubles all the calculations. Then I came across the idea of deferred reflections in an article about the rendering technology in Metro 2033.

The idea is simple. You render the reflection into the G-buffer with non-reflected attributes, and in the next step you light the scene and the reflected scene together. There are some subtleties, but in general it's easy to implement. I had some trouble with unlit objects, like the sky and the glass here. Preserving the depth buffer while rendering the scene into the G-buffers solves that.
