---
title: A pool allocator for small objects
description: "Small objects in my engine now get their memory from a pool allocator, which makes small allocations three times faster."
date: 2009-12-01 09:47
tags: [engine, performance, cpp]
---
![Little Zombie Susie screenshot](/assets/img/2009/littlezombiesusie2-009771.jpg)

The standard C++ allocator usually keeps free memory chunks in a linked list, so finding a free chunk isn't fast, and small objects suffer the most. I decided to speed up allocation with a dedicated pool allocator. Every small object in the engine now derives from a base class that takes its memory from the pool and gives it back there.

Memory allocation for small objects is now three times faster.

The idea comes from Andrei Alexandrescu's [Modern C++ Design](http://www.amazon.com/exec/obidos/ASIN/0201704315/modecdesi-20). His small-object allocator is explained in detail [here](http://books.google.com/books?id=aJ1av7UFBPwC&pg=PA78&lpg=PA78&dq=Andrei+Alexandrescu+pool+allocator&source=bl&ots=YQfM1pOh7_&sig=reCULuBCidrVZX9rJNgwdH-fiRE&hl=en&ei=ds8VS4vtD5CTkAWZgZWABw&sa=X&oi=book_result&ct=result&resnum=1&ved=0CAgQ6AEwAA#v=onepage&q=&f=false).
