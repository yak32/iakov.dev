---
title: Replacing std::vector with a stack array
description: "Removing dynamic allocation from the Glow engine's update loop with a container that mixes boost::array and std::vector."
date: 2010-12-30 10:28
tags: [engine, performance, cpp]
---
I am working on memory management for the engine at the moment. A lot is done already, and I will write about it in detail later. This post is about arrays.

Dynamic allocation is a bad thing, especially in optimised applications. You get fragmentation, locks, and time spent searching for a free block. The general advice is to avoid any kind of dynamic allocation in the update loop, so I decided to remove it everywhere and move all dynamic data to the stack.

<!--more-->

The source had a lot of std::vectors and std::strings: around 700 uses of std::string, and about the same for vector. First I changed the vectors into C arrays, but those are inconvenient to use. Then I found boost::array, but it isn't dynamic.

So I made a mix of boost::array and std::vector. It is based on the boost::array source, with the ability to grow dynamically through one extra variable, m_size. It is useful and looks optimal.

Update: maybe not so optimal for complex objects with non-trivial constructors, or for big objects. For pointers and simple types it is optimal.
