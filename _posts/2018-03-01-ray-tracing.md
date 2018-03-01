---
layout: post
title: "Ray Tracing"
description: A simple ray tracing engine based on Compute Shader.
image: '/assets/img/rt/1.jpg'
category: 'tech practice'
tag:
- unity3d
- gpgpu
twitter_text:  A simple ray tracing engine based on Compute Shader - Ray Tracing made by Lind Chen. 
introduction: It's a simple Ray Tracing Renderer made with Unity3d. Due to compute shader and signed distance function, it can run at realtime.
---

Code : *[Github](https://github.com/cozlind/Ray-Tracing)*

Date : *Spring 2018*

Ray tracing is a basic rendering technique used for global illumination, which can highly improve the visual realism. It usually has better rendering quality but greater computational cost than scanline rendering methods like [Satry Renderer](/satry-renderer/).

I made this demo referring to [1].

![](/assets/img/rt/3.png)

The algorithm starts with the camera. Casting the ray from every pixel of eye plane, then set the color and reflect the ray if it cast on the shape. After a few iterations, stop reflecting.

The shape construction is based on [signed distance function](http://iquilezles.org/www/articles/raymarchingdf/raymarchingdf.htm), which can define a primitive in a very simple way. Besides, the most code is in compute shader, so it's amazingly 70fps. I tried to render more general polygon model such as a sphere, but it's really slow with so many triangles needing intersection and light calculation.

![](/assets/img/rt/2.jpg)



I use the [Schlick's approximation](https://en.wikipedia.org/wiki/Schlick's_approximation) to get the fresnel factor to render the reflective surface. 

it's the scene without spotlight.

![](/assets/img/rt/3.jpg)

Here are some document and source code links :

[1] UnityComputeShaderTest [`Github`](https://github.com/Arlorean/UnityComputeShaderTest)

[2] [Samllpt - 99 lines Global Illumination](http://www.kevinbeason.com/smallpt/)

[3] [Raytracing Topics & Techniques](http://www.flipcode.com/archives/Raytracing_Topics_Techniques-Part_1_Introduction.shtml) 

[4] unity-raytracer [`Github`](https://github.com/SIZMW/unity-raytracer) 

[5] ray-tracing [`Github`](https://github.com/adamjoyce/ray-tracing) 





