---
title: Simple steering behaviour for bots
description: "Bots in my engine now use simple steering with velocity and acceleration instead of following the path directly."
date: 2009-12-15 08:23
tags: [engine, ai]
youtube: Pw7GRTxxnYA
---
Yesterday I added simple steering behaviour for the bots. Their movement looks more realistic than the old direct path following. A bot now has a velocity and an acceleration, and it tries to move along the current line of its path.

There's still work left. The bot's position is no longer exactly on the safe path, so I have to deal with walls. Moving obstacles need handling too.
