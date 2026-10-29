---
title: Notes on the Metro 2033 tech interview
description: "Reading the Digital Foundry interview on Metro 2033's tech: deferred reflections, and a plan to try exponential shadow maps."
date: 2010-12-13 04:32
tags: [engine, rendering, lighting]
---
This [Digital Foundry interview about the tech of Metro 2033](http://www.eurogamer.net/articles/digitalfoundry-tech-interview-metro-2033) is inspiring reading. Shishkovtsov is a smart guy.

The part I liked most is deferred reflections. It is a very simple way to get reflections out of a deferred renderer: render the reflected attributes (position, normal and so on) into the geometry buffer and shade them as usual.

After reading it I am also thinking about implementing [Exponential Shadow Maps](http://www.thomasannen.com/pub/gi2008esm.pdf).

I first read the interview about half a year ago, and I have rewritten a lot of the engine since then. It got a thread pool, it was split into several separate modules, and more.
