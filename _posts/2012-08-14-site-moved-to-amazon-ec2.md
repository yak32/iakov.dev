---
title: Moving the site to Amazon EC2
description: "I moved the blog and site from Hostgator to a free t1.micro instance on Amazon EC2 and set up the whole server by hand."
date: 2012-08-14 15:42
tags: [personal]
image: /assets/img/2012/08/AroundApp.png
---
I moved the blog and the site to Amazon Elastic Compute Cloud, and it took me several days. Until now I paid Hostgator around 10 USD a month for hosting. Amazon has a free option, a t1.micro instance that costs nothing for the first year, and I wanted to try Amazon's services and play with a virtual machine anyway, so I switched.

<!--more-->

What you get is a bare virtual machine with no extra services, which means you install everything yourself. In return it scales easily, and you pay only for what you use.

I chose Linux for the machine and then installed MySQL, the Apache server, an FTP server and WordPress. Two links that helped me: [WordPress installation](http://coenraets.org/blog/2012/01/setting-up-wordpress-on-amazon-ec2-in-5-minutes/) and [FTP](http://www.synergycode.com/knowledgebase/blog/item/ftp-server-on-amazon-ec2).

I hope this post still reaches my readers through RSS.
