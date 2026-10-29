---
title: First steps with SSAO
description: "Screen-space ambient occlusion in the Glow engine, plus a video of the new water."
date: 2011-12-08 17:14
tags: [engine, lighting, water]
---
![Screen-space ambient occlusion in the Glow engine](/assets/img/2011/glow_ssao_stage2-ad2785.jpg)

Today's result is screen-space ambient occlusion. For each pixel it searches the surrounding pixels to work out how occluded that pixel is, then blurs the result and blends it with the screen.

A video with the water:

<iframe src="https://player.vimeo.com/video/33439317?portrait=0" frameborder="0" width="640" height="424"></iframe>

A few effects are still left to implement, such as light scattering (god rays). After that I can finally start work on the game.
