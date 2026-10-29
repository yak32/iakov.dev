---
title: Starting the web player
description: "First day of work on a browser web player for the Glow engine, built as an ATL ActiveX control."
date: 2010-02-02 10:47
tags: [engine, web]
---
Today I started on a web player for the Glow engine, and there are results already. I created an ActiveX control based on ATL, attached the engine to it, and the whole thing runs in the ActiveX Test Container without problems.

ActiveX means it only works in Internet Explorer for now. Firefox and Chrome will need their own testing later. A player in a browser also can't count on finding its data on the local disk, so the engine will have to learn to load files from the internet as well.
