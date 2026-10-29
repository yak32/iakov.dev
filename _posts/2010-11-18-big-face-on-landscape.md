---
title: Big face on the landscape
description: "A random photo used as landscape texture while testing the Glow editor, plus FBX import, heightmap tracing and drag-and-drop assignment."
date: 2010-11-18 16:45
tags: [personal]
---
[![A landscape in the editor textured with a giant photo of a face](/assets/img/2010/editor_face-58edac.jpg)](/assets/img/2010/editor_face-a18d6a.jpg)

While testing new editor features I set the landscape texture to a random photo. Walking across a gigantic face is a strange experience.

The new features:

* Import of 3D models from FBX files through the Autodesk FBX SDK.
* Ray tracing against landscapes uses the heightmap, which is faster than tracing the actual geometry.
* Materials, scripts and audio files can be assigned to objects by dragging them from Explorer or the Assets window.
* Scripts can be edited in Notepad, assigned to an object and removed.
* A depth pass now runs before the geometry buffer pass in deferred shading.
* A current insertion position for cut, copy and paste.
