---
title: Colour transformations as a post-process
description: "The Glow engine gets a single-pass colour transformation post-process for contrast, brightness, black and white and RGB shifts."
date: 2011-04-04 08:40
tags: [engine, rendering]
---
I've added colour transformations to the Glow engine as a post-process.

Right now it supports contrast, brightness, black and white, and red, green and blue shifts. Saturation will come later. All the transformations run in one pass, so adding contrast on top of brightness, for example, doesn't make it twice as slow.

The transformations are scene properties, so scripts can change them.

The original image:

![Original image before colour transformations](/assets/img/2011/cc_step1-fe367a.jpg)

Brightness adjusted:

![The same image with brightness adjusted](/assets/img/2011/cc_step2-830846.jpg)

Blue and green shifted for a Matrix look, with brightness adjusted:

![Blue and green shifted to give a Matrix film look](/assets/img/2011/cc_step3-09cd2c.jpg)

Black and white:

![The image in black and white](/assets/img/2011/cc_step4-c90f6e.jpg)
