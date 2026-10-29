---
title: Debugging Iron Cube with recorded network traffic
subtitle: Debugging by saving network communication
description: "Recording server data on an Android phone and replaying it in the Windows editor helps me track down network bugs in Iron Cube."
date: 2013-12-16 15:16
tags: [game, iron-cube, editor, android, multiplayer]
image: /assets/img/2013/12/ironcube_editor.jpg
---
I'm debugging some network issues in the Android version of Iron Cube. Saving the network data that the client receives from the server, which I added for recording trailers, has turned out to be very useful for this. I can record a game on an Android device and then play it back in the editor on a Windows machine, which makes bugs much easier to find and fix. In the screenshot the editor has a recording, net_record.glw, loaded in the Cinematic panel, next to the pause, stop and playback speed buttons.

There is still one bug in the Android version where bullets don't disappear from the screen. I hope to fix it soon.
