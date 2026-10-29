---
title: Iron Cube in the browser with Emscripten
subtitle: Iron Cube on the web
description: "I ported my Iron Cube demo to the web with Emscripten in a couple of days, and it runs in modern desktop and mobile browsers."
date: 2019-10-10 00:21
tags: [iron-cube, rendering, web]
youtube: 2Y9w1yKdskM
---
I ported my demo game Iron Cube to the web in a couple of days with Emscripten. Emscripten compiles C++ to code that runs in the browser, so the same engine code that runs on Windows and Android now runs in a web page. The video above shows the result.

You can play the demo here: [https://glow3d.com/blog/demos/iron_cube.html](https://glow3d.com/blog/demos/iron_cube.html). It should work in any modern browser, mobile browsers included.

Iron Cube is my multiplayer tank game in a fully destructible voxel world. The engine already renders with OpenGL and uses SDL2 as its platform layer, and Emscripten supports both.
