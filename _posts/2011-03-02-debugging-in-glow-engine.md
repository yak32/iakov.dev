---
title: Debug views in the Glow engine
description: "The Glow engine editor gets debug modes for wireframe, normals, depth, lights, physics, AI triggers and navigation meshes."
date: 2011-03-02 11:06
tags: [engine]
---
When you're building a game level you need to see debugging information about the level and its models. I used to place every object, lights included, in 3ds Max, and it was slow going: tweak the lighting in 3ds Max, switch to the engine, check the lighting, and round again.

The Glow engine now has several debug modes: wireframe, world-space normals, pixel depth, lights, physics, AI (triggers) and navigation meshes. You can turn on several at once, except normals, depth and diffuse colour, which can't be combined. To pick a mode, press the "layers" button and select it.

A room from the "Deadly Light" demo, lit by 6 lights:

[![Room from the Deadly Light demo lit by six lights](/assets/img/2011/editor_room-624730.jpg)](/assets/img/2011/editor_room-76ad04.jpg)

The same room in wireframe mode:

[![The same room in wireframe debug mode](/assets/img/2011/editor_wireframe-12d89b.jpg)](/assets/img/2011/editor_wireframe-a8301b.jpg)

Normals mode:

[![World-space normals debug view](/assets/img/2011/editor_normals-087acb.jpg)](/assets/img/2011/editor_normals-1eb876.jpg)

The lights debugger:

[![Lights debug view showing the room's light sources](/assets/img/2011/editor_lights-c6eb97.jpg)](/assets/img/2011/editor_lights-10ab6b.jpg)

Physics:

[![Physics debug view](/assets/img/2011/editor_physics-b91bd7.jpg)](/assets/img/2011/editor_physics-351a57.jpg)

Depth:

[![Depth debug view](/assets/img/2011/editor_depth-0e2f38.jpg)](/assets/img/2011/editor_depth-74f51a.jpg)
