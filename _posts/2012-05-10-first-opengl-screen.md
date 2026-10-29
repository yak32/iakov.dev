---
title: First OpenGL screenshot
description: "The first screenshot of Tarta on the Glow engine's new OpenGL renderer, after a quick port to GCC and Linux."
date: 2012-05-10 02:25
tags: [engine]
image: /assets/img/2012/05/opengl_first_screen1.jpg
---
This is the first screenshot of the Tarta game running on the OpenGL renderer. There's nothing special in it, but it matters to me: the scheme for cross-platform development that I chose a long time ago finally works.

Two weeks ago I tried compiling under GCC on Linux and had it done in 2-3 days without any serious problems.

The engine now supports DirectX and, in a basic form, OpenGL. Later OpenGL will let me run the Glow engine on iOS and Android, as well as Linux and macOS.

On top of that, with the open-source hlsl2glsl library I'll be able to use all the complex HLSL shaders from the DirectX renderer automatically.
