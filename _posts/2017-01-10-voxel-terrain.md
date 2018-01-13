---
layout: post
title: "Voxel Terrain"
description: A procedural voxel terrain generation demo based on marching cubes.
image: '/assets/img/marchingcubes/1.jpg'
category: 'tech practice'
tag:
- procedural generation
- marching cubes
- noise
- unity3d
twitter_text: A procedural terrain generation demo based on marching cubes - Voxel Terrain made by Lind Chen. 
introduction: A procedural terrain generation demo based on perlin noise. The voxel representation is attained with marching cubes.
---

Code : *[Github](https://github.com/cozlind/Marching-Cubes)*

Date : *Winter 2017*

It's a procedural terrain generation demo based on perlin noise. The voxel representation is attained with marching cubes & marching tetrahedron.
<iframe width="100%" height="372vh" src="https://www.youtube.com/embed/uYTlM7gtpBc" frameborder="0" allow="autoplay; encrypted-media" allowfullscreen></iframe>

Marching Cubes is one of the isosurface extraction algorithm, which was first published in the 1987 Siggraph proceedings by Lorensen and Cline. The application of this algorithm are mainly concerned with medical visualizations such as CT and MRI scan data, and special effects or 3D modeling with what is usually called [metaballs](https://en.wikipedia.org/wiki/Metaballs). The two-dimensional method is called the marching squares algorithm. [Anstroneer](https://astroneer.space/) also use this method to acoomplish their stylized terrain.

As for the voxel, the signed distance field data representation and ray tracing or ray matching are usually the most accurate practice in volume rendering. However, although marching cubes is not really a volume algorithm, it's more efficient for real-time application.

![](/assets/img/marchingcubes/2.jpg)

The procedural generation technique is mainly based on Perlin Noise, which is kind of general way to express self similarity. The difference between this demo and [Lowpoly Terrain](/lowpoly-terrain) is that this one can generate overhangs and cave.

![](/assets/img/marchingcubes/3.jpg)

I developed it for about 1 month, and the fps is basically over 60 but not steady because it's  based on CPU. I think it's would be faster on shader.

![](/assets/img/marchingcubes/4.jpg)

I see this demo as the foundamation for my master research. Then I can execute the erosion algorithm on 3d terrain.

![](/assets/img/marchingcubes/5.jpg)

The most troublesome part , I suppose, is to consider all the shapes that could happen inside a voxel cube, and thanks to there are some initial arrays can be download in the Internet. 