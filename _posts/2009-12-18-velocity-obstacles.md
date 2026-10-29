---
title: Velocity obstacles finally make sense
description: "I finally understand the velocity obstacle method for avoiding moving obstacles, which is what I need for hordes of zombies."
date: 2009-12-18 08:57
tags: [engine, ai]
---
I finally understand what a [Velocity Obstacle](http://www.cs.rpi.edu/~sakella/rmp03/presentations/Motion_Planning_in_Dynamic_Environments_using_Velocity_Obstacles.pdf) is. It's ridiculously simple. Printing out the source article and reading it on paper helped a lot.

For each moving obstacle you work out the set of velocities that would make you collide with it at some point, if both of you keep moving as you are. Then you pick a velocity outside all of those sets.

Which means there will be hordes of zombies.
