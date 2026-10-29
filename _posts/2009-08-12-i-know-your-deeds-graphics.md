---
title: Graphics tech in I Know Your Deeds
description: "A tech video of the graphics in I Know Your Deeds: grass, trees, deferred shading, dynamic sky and a landscape painted in Photoshop."
date: 2009-08-12 09:23
tags: [engine, game, rendering, lighting]
youtube: vhlBdYBUnqE
---
I'm going to upload a few tech videos from I Know Your Deeds, the demo I made for Intel Level Up. This one is about graphics.

It shows grass, trees, deferred shading, a dynamic sky with clouds, and a landscape with three materials blended by a weight map. I modelled the landscape in Photoshop with the Clouds filter, then edited it by hand to make room for the houses.

Grass is drawn from a grass density map, one per landscape. I placed the trees in Photoshop as well. There is a separate bitmap for foliage: paint a red dot on it, for example, and a tree appears at that spot in the level.

Shadows use ordinary shadow mapping. I don't use perspective shadow maps.
