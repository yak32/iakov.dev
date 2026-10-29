---
title: Mercury in stage 2 of the Intel challenge
subtitle: Intel Perceptual Computing Challenge, stage 2
description: "An improved Mercury for stage 2 of the Intel Perceptual Computing Challenge: new gestures, an OpenGL renderer, saving and smoother brushes."
date: 2013-11-12 05:49
tags: [voxel, contest, rendering]
youtube: EzSByIMRiJk
---
I took part in stage 2 of the Intel Perceptual Computing Challenge with an improved version of my first prototype, the one that [won first prize](/2013/03/first-prize-winner-of-intel-perceptual-computing-challenge/) in stage 1. Intel has improved the SDK since June, and it is more robust now. Last time the camera reached me one day before the deadline, so I didn't have time to implement gesture support properly.

<!--more-->

This demo adds several new gestures. A "zoom" gesture, where you move your open hands, changes the brush size. The "circle" gesture, which the SDK provides, undoes the last operation. Swiping up, down, left or right starts "potter" mode.

I also switched the renderer from DirectX to OpenGL and made the lighting simpler (forward) to speed up rendering. You can now save and load a model, and the brush moves more smoothly and reliably.

It has turned into something like a paint editor for voxel models.
