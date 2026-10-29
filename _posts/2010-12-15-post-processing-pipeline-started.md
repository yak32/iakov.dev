---
title: Post-processing pipeline started
description: "A post-processing pipeline for the Glow engine, starting with camera motion blur built from the geometry buffer."
date: 2010-12-15 16:08
tags: [engine]
---
I spent last week on post-processing, and the engine now has a pipeline for it. The first effect is motion blur done as a post-process and built from the geometry buffer, as described in [GPU Gems 3](https://developer.nvidia.com/gpugems/gpugems3/part-iv-image-effects/chapter-27-motion-blur-post-processing-effect). It can be safely disabled. My collection of papers is finally paying off.

This motion blur comes from camera movement only. Per-object motion blur will follow later, with per-pixel velocities stored in the geometry buffer.

Motion blur in action, with a 15-sample kernel:

[![Editor view of the scene with strong camera motion blur](/assets/img/2010/editor_motion_blur-5d736d.jpg)](/assets/img/2010/editor_motion_blur-d45d31.jpg)

The original scene:

[![The same building in the editor without motion blur](/assets/img/2010/editor6-3eec69.jpg)](/assets/img/2010/editor6-715713.jpg)

Several more post-processing effects are scheduled: a glow pass that blurs the bright parts of the scene, analytical anti-aliasing, depth of field and others. I have also started on mirrors and deferred reflections.
