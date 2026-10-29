---
title: Moving to Intel Threading Building Blocks
description: "Why the Glow engine's task system is switching from the experimental boost::thread_pool to Intel Threading Building Blocks."
date: 2011-01-31 05:22
tags: [engine]
---
I'm getting deeper into concurrency and multithreading, and I've decided to use [Intel Threading Building Blocks](https://github.com/uxlfoundation/oneTBB) instead of the experimental [boost::thread_pool](http://threadpool.sourceforge.net/).

All computation in the Glow engine is organised into tasks, so in theory it should scale well as the number of hardware threads (CPU cores) goes up. Until now I ran those tasks on boost::thread_pool. Coming back to the concurrency code, I realised that approach can't scale, because the pool relies heavily on spin-based mutexes.

Later I'll run tests to measure how both methods scale and post the results here.
