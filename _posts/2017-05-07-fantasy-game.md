---
title: A voxel adventure game prototype
subtitle: An untitled game prototype
description: "Video of an isometric, Zelda-like voxel adventure prototype on my Glow3D engine, with art by Sir carma, MagicaVoxel import and NVIDIA HBAO+."
date: 2017-05-07 23:13
tags: [game]
youtube: dsCfWE7WE1c
---
This is a video of the voxel [game prototype](/2017/04/voxel-project/) I built on my **Glow3D** engine a while ago. The idea was something like the original Zelda: an isometric adventure, but made of voxels. The art in the video is by [Sir carma](https://twitter.com/sir_carma?lang=en).

I wrote a parser for the MagicaVoxel file format and made big changes to the code I had written for the [Iron Cube game](/2013/10/iron-cube-on-google-play/). To improve the picture I added NVIDIA HBAO+ and NVIDIA shadows through the [ShadowWorks middleware](https://developer.nvidia.com/shadowworks). HBAO+ is a *screen space ambient occlusion* technique that approximates global illumination, and with it I gave up on writing my own SSAO, at least for a while. The engine already had some shadow support, but at the time it had no efficient cascaded shadow maps, so I went with the NVIDIA libraries instead. They are fast and many modern games use them.

[MagicaVoxel](https://ephtracy.github.io/) is a nice voxel editor and renderer made by [@ephtracy](https://twitter.com/ephtracy?lang=en). He has more or less built a 3ds Max single-handed, only for voxel graphics. The music in the video is [Medieval Introduction](http://www.freesound.org/people/Tristan_Lohengrin/sounds/319781/).
