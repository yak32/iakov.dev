---
title: First week of the level editor
description: "A week into the Glow level editor: drag-and-drop meshes, a background asset manager, undo/redo and objects snapped to the landscape."
date: 2010-08-25 05:02
tags: [engine]
youtube: N9XsXwIe9mQ
---
These features went into the Glow engine editor over the last week. Until now all level geometry was built in 3ds Max and imported into the engine. That is an inconvenient way to edit a game level, and an expensive one, so I started on an editor of my own.

After a week it can do this. Meshes can be dragged and dropped in from Explorer (OBJ format for now, more formats later). A simple asset manager runs as a job in a parallel thread, so parsing 3D meshes doesn't block the UI.

Undo and redo work, implemented with boost functors. They currently cover move, rotate, scale, delete, insert and selection. Objects can be linked to the landscape, so buildings and trees always stay on the ground. Rotation and movement work in either local or world coordinates.

Next on the list: building the level, attaching scripts to objects, and assigning materials by dragging them from Windows Explorer.
