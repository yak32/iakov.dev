---
title: Normal texture trick
description: "A normal map trick that lets the same shaders read DXT1 and DXT5 bump textures, so the editor can skip DXT5 compression."
date: 2010-12-01 12:58
tags: [engine, rendering, editor]
---
I found an interesting trick for reading normals from textures, described on the [NVIDIA Texture Tools wiki](https://github.com/castano/nvidia-texture-tools/wiki/NormalMapCompression). In short, it lets the same shaders use both DXT1 and DXT5 bump textures.

This matters for the editor, because the DXT5 version of a bump texture is only produced at the last stage, when the game is packaged. During testing inside the editor objects will look a little different, since DXT1 is not good for normals. I think that is acceptable.
