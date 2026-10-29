---
title: A short way to build a quaternion from a direction
description: "Replacing a long asin/acos quaternion function with four lines that rotate (0,0,1) onto any unit vector."
date: 2010-08-05 06:53
tags: [engine]
---
A long time ago I wrote a function that creates a quaternion for the rotation from (0,0,1) to any unit vector. It was very long, with asin, acos, several conditions and so on.

Today I came back to it, and after some thought it shrank to the code below. The w component is 1 plus the dot product of the two vectors, which with (0,0,1) is just 1 + dir.z. The x and y components come from their cross product, whose z part is always zero here, and normalising at the end gives the correct half-angle rotation. `dir` must be a unit vector.

```cpp
void Quaternion::from_direction(const vec3 dir){
	x = dir.y;
	y = -dir.x;  z = 0;
	w = 1 + dir.z; // simplified dot product with 0,0,1
	normalize();
}
```
