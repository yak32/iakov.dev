---
title: First horde tests
description: "First tests of steering behaviours for a horde of bots: Recast navigation plus neighbour, wall and dynamic obstacle avoidance."
date: 2009-12-24 10:36
tags: [engine, ai]
youtube: uH4lo1gW2K8
---
I spent the day implementing steering behaviours for a horde.

The first video uses Recast navigation, plus avoiding the nearest neighbour (with prediction, in the OpenSteer style), plus avoiding nearby walls.

The second one uses Recast navigation and the same nearest-neighbour avoidance, but here the bots avoid walls only after they collide with them, and they also avoid dynamic obstacles.

{% include youtube.html id="_gStLaNyJ24" %}

The navigation mesh takes time to update (usually it's updated at 0.5-second intervals), so sometimes bots walk through an obstacle. For moving obstacles I may need to use the same steering behaviour as for avoiding other bots.

Does it look natural to you, or does it need more work?
