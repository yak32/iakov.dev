---
title: The Mercury prototype
subtitle: A better video of the Mercury prototype
description: "A cleaner video of Mercury, my hand-controlled voxel sculpting prototype, with more robust fingertip tracking from the Perceptual Computing SDK."
date: 2013-03-05 14:39
tags: [prototype, mercury, voxel]
youtube: ASTTUvziJgE
---
Mercury is my entry for the Intel Perceptual Computing Challenge: a voxel sculpting prototype on the Glow engine that you control with your hands in front of a Creative gesture camera. The first video was a bit chaotic, so here is a new one.

Since then I have also improved the gesture handling. The Perceptual Computing SDK reports positions for individual fingers, and that is what I used at first. Now I take the coordinate of LABEL_HAND_FINGERTIP instead, and it seems more robust.

The camera arrived only a day before the deadline, so the first version had a single day of integration behind it and very little time for tuning the gestures.
