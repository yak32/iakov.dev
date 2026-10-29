---
title: A month of refactoring
description: "I split the Glow engine into separate DLL modules behind abstract interfaces and added a thread pool for jobs."
date: 2010-07-07 06:26
tags: [engine]
---
I spent a month refactoring the engine. It had grown so big that I could no longer keep all of it in my head.

So I split it into small pieces: physics, sound, networking, core, AI, UI and archive. I prepared a solid interface for accessing the engine's features, which is the part that people using the engine will see. Every module now lives in its own DLL and sits behind an abstract interface, so the modules are cleanly isolated from each other.

I also added a thread pool (boost::threadpool) that runs jobs from the modules. With that in place the engine should scale easily as CPUs get more cores.
