---
title: Recording and replaying games in Iron Cube
description: "How I added movie recording and playback to Iron Cube by saving the server's network snapshots, which also gives slow motion for trailers."
date: 2013-12-02 05:13
tags: [game, iron-cube, engine]
youtube: Wg4ERZKFAF8
---
I've been reading books and articles about marketing mobile and indie games, and I find it more interesting than I expected. One of the most important things for marketing a game is a good trailer, so I decided to add movie recording and playback to Iron Cube and the Glow engine.

It looked like a complicated task, but the solution turned out to be simple. To record a game you save everything the client receives from the server. Later you load that file in the editor and emulate the server's network traffic, and the original game plays out again. The recording comes out compressed for free: networking in the Glow engine is snapshot-based, so only changed data travels between server and client. The movie below takes less than 1 MB.

This opens up some fun options. For example, you can slow playback down and get Matrix-style slow motion. There is no interpolation between frames yet, so it can look a bit laggy.
