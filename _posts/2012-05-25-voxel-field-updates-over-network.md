---
title: Voxel field updates over the network
description: "Tarta now edits the voxel field on the server and sends changed chunks to clients over UDP, compressed with RLE."
date: 2012-05-25 00:09
tags: [game, voxel, multiplayer]
image: /assets/img/2012/05/tarta_net_hole2.jpg
---
Today I got voxel field updates working in multiplayer. The server is the one that changes the voxel field, and then it sends the result to the clients. The screenshot is the first one I took of it working: a hole in the ground that was dug on the server and showed up on the client.

Updates go out one chunk at a time. A chunk is 32x32x64 voxels, and I compress it with RLE before sending. The transport is UDP, the same as the rest of the client-server communication in the game.
