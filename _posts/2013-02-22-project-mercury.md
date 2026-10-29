---
title: Project Mercury
subtitle: A voxel 3D mesh editor you control with your bare hands
description: "Mercury, my entry for the Intel Perceptual Computing Challenge: a voxel sculpting prototype on the Glow engine controlled by hand gestures."
date: 2013-02-22 09:32
tags: [mercury, prototype]
youtube: y6779QOnh6A
---
I entered the Intel Perceptual Computing Challenge with Project Mercury, a digital sculpting application. You edit a voxel-based 3D mesh with your bare hands.

The prototype runs on the Glow engine and uses the voxel engine I wrote for the [Iron Cube](http://www.moddb.com/games/iron-cube) game. For Mercury I also wrote smooth mesh generation based on Surface Nets, which is a modification of Marching Cubes.

The hand interface uses the [Intel Perceptual Computing SDK](http://software.intel.com/en-us/vcsource/tools/perceptual-computing-sdk) and the [Creative Interactive Gesture Camera Developer Kit](http://click.intel.com/intelsdk/Creative_Interactive_Gesture_Camera_Developer_Kit-P2061.aspx). The camera arrived one day before my deadline, so I had a single day to integrate it into the engine. To my surprise the integration took only a few hours. The SDK ships with a utility library that makes the camera's features easy to use.

The SDK recognises several common gestures, such as victory (V) and thumbs up, and gives you the exact 3D position of every finger. It also tells you where the hand is and whether it is open or closed.

For now Mercury supports only a limited set of gestures and manipulations. I want sculpting in it to feel as easy as sculpting real clay, and the camera is precise enough to get there.
