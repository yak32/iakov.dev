---
title: Path tracing voxels, day 1
subtitle: Actually day 2
description: "Adding a path tracer to my voxel engine after Ray Tracing in One Weekend: voxel ray casting, importance-sampled sunlight and going from 0.4M to 5M rays per second."
date: 2019-10-16 12:13
tags: [voxel, rendering, lighting, performance]
image: /assets/img/2019/raytracing_blog.png
---
### Ray Tracing in One Weekend

I was reading the excellent [Ray Tracing in One Weekend](https://www.realtimerendering.com/raytracing/Ray%20Tracing%20in%20a%20Weekend.pdf) and decided to try it in my voxel engine and editor. The book builds its scenes out of spheres, but I wanted to use voxels.

### How it works

A ray goes from the camera through each pixel on the screen. You find where it hits the scene and then work out where the ray goes next. On a diffuse surface the ray scatters in a random direction, a metal surface reflects it, and glass either reflects or refracts it. [The book](https://www.realtimerendering.com/raytracing/Ray%20Tracing%20in%20a%20Weekend.pdf) explains this better than I can here.

<!--more-->

### Ray casting

Ray tracing is only as fast as your ray casting. There are many ways to speed it up, such as bounding volume hierarchies. Luckily the engine already had a world trace function that I used for surface editing, although it was slow.

So the first thing I wrote was a version of [Bresenham's line algorithm](https://en.wikipedia.org/wiki/Bresenham%27s_line_algorithm) for tracing, similar to what Wolfenstein 3D does but extended to 3D. [Here](https://lodev.org/cgtutor/raycasting.html) is a good explanation of the ray casting in Wolfenstein. You step from voxel to voxel until you reach the first solid one, and that's your intersection. The voxel field is split into 32x32x32 clusters, so the tracer can skip empty clusters entirely, and it uses the same stepping technique to move between clusters. The inner loop, for both clusters and voxels, has only 2 conditions and 2 floating point additions.

### Shading and lighting

Then I moved on to the actual rendering and reimplemented the shading from the book in 300 lines of code. Ray tracing is a powerful technique. A few lines of code get you a picture quite close to reality.

For sunlight and shadows I used importance sampling, following the idea from [Ray Tracing: The Rest of Your Life](https://www.realtimerendering.com/raytracing/Ray%20Tracing_%20the%20Rest%20of%20Your%20Life.pdf).

One of the first images, using a free voxel scene by [Mike Judge](https://github.com/mikelovesrobots/mmmm):

[![One of the first path-traced images of a voxel scene](/assets/img/2019/raytracing_day1_thumb.png)](/assets/img/2019/raytracing_day1.png)

### Optimisations

The first version was slow: 0.4M rays per second, and several minutes to render a 720p picture at 100 samples per pixel. I applied the obvious fixes:

* Multithreading. Several threads render the image and add their colours into one shared floating point buffer, so a first rough picture shows up quickly.
* Removing profiling and debugging code. trace() is called millions of times, so taking out everything that touched a mutex helped a lot.
* A better random number generator, from [this article](https://aras-p.info/blog/2018/03/28/Daily-Pathtracer-Part-2-Fix-Stupid/) by Aras.

The random number generator and the multithreaded rendering were painful at first. I spent a couple of hours trying to understand why a picture rendered with 100 samples per pixel looked this bad:

[![Noisy render caused by unseeded random numbers in worker threads](/assets/img/2019/raycasting_1_thumb.png)](/assets/img/2019/raycasting_1_thumb.png)

The answer was interesting. The C++ random number generator computes each number from the previous one, and you have to call srand() to seed it in each thread. The random numbers push each sample's ray in a random direction. Without srand() the rays went in the same direction every time, so every pass produced an identical image.

### Conclusion

With a couple of tricks I got the ray tracer from 0.4M rays per second to around 5M. Going further could be tricky. One option is [Intel Open Image Denoise](https://openimagedenoise.github.io/): you render with fewer samples per pixel and run the denoiser on top.
