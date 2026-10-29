---
title: Taking my game from 40 to 160 fps
description: "How a forgotten debug line, grass instancing and a slow NPC sensor system were holding my IGF game back, and what I've fixed so far."
date: 2009-11-25 10:17
tags: [engine, performance, contest]
---
In testing, my game ran at an average of 40 fps on a GeForce 9600 with an Intel quad-core CPU. That's the version I sent to the IGF.

A few days ago I noticed that every shadow in the level was being drawn every frame. I searched the source and found a line I had commented out for debugging. Putting it back doubled the speed, to about 80 fps. Then I switched off the grass and the NPC sensor system, which searches for enemies five times a second, and the frame rate went up to 400.

<!--more-->

So the first thing I did was implement proper instancing for the grass. I also dropped support for all graphics cards without Shader Model 3. The next step is a faster sensor system for the NPCs.

The average is now 160 fps, and there are still plenty of ways to improve it.
