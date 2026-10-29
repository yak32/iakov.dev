---
title: Cutting texture loading from 4 minutes to 4 seconds
description: "How DDS textures, a loading thread and distance-based streaming took my level loading time from about 4 minutes to 3-4 seconds."
date: 2009-11-30 05:24
tags: [engine]
---
![Outdoor level in my engine](/assets/img/2009/screen-1de4df.jpg)

My previous demo took about 4 minutes to load. It had a lot of big textures, usually 1024x1024, and most of them were TGA files.

To fix this I switched to DDS with the mipmaps packed into the file, and moved texture loading to a separate thread. The engine now loads only the textures that are close by, within about 50 metres (an engine parameter). As you move, textures that end up outside that radius are unloaded. At a distance the engine uses a small version of each texture instead of the full one, usually 64x64.

The current outdoor level has about 800,000 triangles and now loads in 3-4 seconds. There's no limit on the number of textures in a level, and all the loading happens in a separate thread, which matters on today's multi-core CPUs.
