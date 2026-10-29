---
title: Glow engine feature presentation
description: "A slide presentation listing the features of the Glow engine, published on Google Docs."
date: 2010-07-22 07:15
tags: [engine]
---
I made a presentation of the Glow engine's features. You can view it [on Google Docs](https://docs.google.com/present/edit?id=0ATZm93qPBDO8ZGZyYmRxdDJfNTlmc3RqOTVjdw&hl=en).

The engine has changed a lot this year. In February and March it got the ActiveX web player and streaming from zip files, HTTP and FTP. This month I finished a long refactoring that split it into modules (physics, sound, networking, core, AI, UI, archive), each in its own DLL behind an abstract interface, with a thread pool running their jobs. After all that it seemed a good moment to write down what the engine can do.
