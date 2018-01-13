---
layout: post
title: "Lowpoly Terrain"
description: A procedural terrain generation demo based on perlin noise.

image: '/assets/img/noiseterrain/1.jpg'
category: 'tech practice'
tag:
- procedural generation
- LOD
- noise
- unity3d
twitter_text: A procedural terrain generation demo based on perlin noise. - Lowpoly Terrain made by Lind Chen. 
introduction: A procedural terrain generation demo based on perlin noise. With LOD technique and mesh collider user can move on this unlimited large terrain.
---

Code : *[Github](https://github.com/cozlind/Noise2DTerrain)*

Date : *Fall 2016*

<iframe width="100%" height="372vh" src="https://www.youtube.com/embed/m0TUJfMGYkg" frameborder="0" allow="autoplay; encrypted-media" allowfullscreen></iframe>
This project is created following Sebastian Lague's [Procedural Landmass Generation Tutorial](https://www.youtube.com/watch?v=wbpMiKiSKm8&feature=youtu.be&list=PLFt_AvWsXl0eBW2EiBtl_sxmDtSgZBxB3). I had learned a lot from video tutorials of him, and really appreciate this guy. 

![](/assets/img/noiseterrain/2.jpg)

The procedural generation technique is mainly based on Perlin Noise, which is kind of general way to express self similarity. The parameters offered in inspector panel can used to change the size, density, height of the mountain.

![](/assets/img/noiseterrain/4.jpg)

This demo also divide the terrain into different color area according to height, so it seems so beautiful with a lowpoly look.

![](/assets/img/noiseterrain/3.jpg)

The terrain is actually seperated to different blocks. It not only helps on the development of LOD, also be able to support mesh collider without break the poly number limitation. 

![](/assets/img/noiseterrain/6.jpg)

The most troublesome part , I suppose, is to fix gaps among blocks of different detail levels, because the vertex of reduced block cannot really match the higher detail one. Then the normals also need to recalculate by myself.