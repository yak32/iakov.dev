---
title: Antialiasing in the Glow engine
description: "The Glow engine gets antialiasing through Directionally Localized Antialiasing, the post-process method used in The Force Unleashed 2."
date: 2011-04-04 07:57
tags: [engine, rendering]
---
The Glow engine finally has antialiasing.

I used the [Directionally Localized Antialiasing algorithm](http://and.intercon.ru/releases/talks/dlaagdc2011/), the one from The Force Unleashed 2. It works in image space as a post-process. A high-pass filter finds the edges, and then they get blurred with a 5x5 kernel, or a 16x16 one for long edges.

It looks good. My screenshots have suffered from jaggies for a long time, and now they don't.

Antialiasing off:

![Scene with antialiasing off, showing jagged edges](/assets/img/2011/aa_off-b5493f.jpg)

Antialiasing on:

![The same scene with antialiasing on](/assets/img/2011/aa_on-74db6d.jpg)
