---
layout: post
title: "GPU Marching Cubes"
description: A marching cubes demo based on GPU.
image: '/assets/img/gpumc/1.gif'
category: 'tech practice'
tag:
- marching cubes
- gpu
- directx 11
twitter_text: A marching cubes demo based on GPU made by Lind Chen. 
introduction: A marching cubes demo based on GPU. 
---

Code : *[Github](https://github.com/cozlind/ComplexTerrainGPU)*

Date : *Spring 2017*

As mentioned before ([Voxel Terrain](/voxel-terrain)), Marching Cubes is one of the isosurface extraction algorithm, which was first published in the 1987 Siggraph proceedings by Lorensen and Cline. The application of this algorithm are mainly concerned with medical visualizations such as CT and MRI scan data, and special effects or 3D modeling with what is usually called [metaballs](https://en.wikipedia.org/wiki/Metaballs). The two-dimensional method is called the marching squares algorithm. [Anstroneer](https://astroneer.space/) also use this method to acoomplish their stylized terrain.

![](/assets/img/gpumc/2.jpg)

The procedural generation part is mainly based on Perlin Noise, which is saved and read from a 3d texture. The difference between this demo and [Voxel Terrain](/voxel-terrain) is that this one is written in `.fx` shader file so that it's much faster than the former one.

![](/assets/img/gpumc/3.jpg)

For accomplishing this, I practised my directx programming for more than 1 month. By following the [GPU Gems 3 Chapter 1](https://developer.nvidia.com/gpugems/GPUGems3/gpugems3_ch01.html), it finally worked.