---
title: Streaming data from the internet
description: "The Glow engine now streams data from local files, zip archives and HTTP or FTP, which the web player needs."
date: 2010-03-12 08:29
tags: [engine]
---
The web player needs data from the internet, so I had to implement streaming. It works now, through an extra layer that sits between the engine and wherever the data comes from.

That layer supports several kinds of data source:

1. The usual file system
2. Zip files
3. Files from the internet, over HTTP or FTP

The last piece missing is an installer for the ActiveX control. I haven't decided yet how to install it properly: as a separate MSI installer, or the usual ActiveX way, where the browser downloads and installs it.

![A dark basement room with barrels, rendered by the engine](/assets/img/2010/single-2008-06-30-03-15-17-78-e61ca9.jpg)
