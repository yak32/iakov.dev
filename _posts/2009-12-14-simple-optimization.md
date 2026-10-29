---
title: Use std::vector::swap instead of assignment
description: "If you don't need the source vector after assigning it, swap it instead and save a memory allocation."
date: 2009-12-14 02:23
tags: [engine, cpp]
---
If your code assigns one std::vector to another and you won't need the source vector afterwards, use the vector's `swap` member function instead. Assignment copies the elements into the destination, which can mean allocating a new buffer. Swap only exchanges the internal buffers of the two vectors, so you save one memory allocation.

```cpp
void SetPath_Dirty(vec3& path) {
	m_path.swap(path);
}
```

After the call, `path` holds whatever `m_path` held before, so the caller shouldn't rely on its contents.
