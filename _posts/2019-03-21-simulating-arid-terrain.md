---
layout: post
title: "Simulating Arid Terrain With Aeolian Erosion"
description: A unified framework to create 6 kinds of typical arid landform with wind erosion.
image: '/assets/img/satwae/1.jpg'
category: 'master thesis'
tag:
- unity3d
- simulation
- gpgpu
twitter_text: A unified framework to create 6 kinds of typical arid landform with wind erosion - Simulating Arid Terrain With Aeolian Erosion made by Lind Chen. 
introduction:  We address the problem of generating physically based arid terrain efficiently by presenting a unified framework for creating six kinds of typical arid terrain with wind erosion.
---

Paper : *[PDF](/assets/pdf/Simulating Arid Terrain With Aeolian Erosion.pdf)*

Date : *Summer 2018 - Spring 2019*

Authors : Zuo Chen, Yufan Zhou, Junichi Hoshino

Abstract : We address the problem of generating physically based arid terrain efficiently by presenting a unified framework for creating six kinds of typical arid terrain with aeolian erosion. Previous research mainly focuses on hydraulic erosion or some specific landforms by using ad hoc modeling techniques. Based on the physics of blown sand, the essential idea of our method is the following. We divided the whole simulation into three stages: Erosion, Movement and transportation/deposition. First, we combine the wind drag force with erosion model to realize aeolian erosion. Second, we add the wind parameters, buoyancy equation, thermal diffusion to position based fluids, allowing a saltation motion of sand flow. Besides, we handle the creep motion by moving the surplus solid particles to the neighbors if there are too many sand particles accumulate in one place. Finally, we simulate sand flow as open channel flow, associated with sediment transport between particles. Moreover, we propose a boundary filter to maintain the sediment concentration so that the sand flow particles could be reused and retain the process erosion all the time. The results include the final polygon mesh simulated from the volume model. Our implementation is based on GPU and simulates in an interactive framerate for scenes with up to 50,000 voxels.

The entire procedure is showed in this video below, please check it to build an intuitive impression.
<iframe width="100%" height="372vh" src="https://www.youtube.com/embed/WnHBYLmMpIw" frameborder="0" allowfullscreen></iframe>

At the very first, we summarize 6 kinds of typical landforms which show up regularly in arid environment based on geomorphology.

![](/assets/img/satwae/2.jpg)

Then we model them in [MagicaVoxel](https://ephtracy.github.io/) as voxel-based model according to their structure of strata. Voxel is a very intuitive way to separate the layer resistance and easy for users to understand and edit it.

![](/assets/img/satwae/3.jpg)

The core simulation can be divided into two parts happening at the same time. One is the wind particles simulation implemented based on Position-Based Fluid (PBF) method, the other is erosion process involving the interaction between voxel and particles. We can adjust a lot of parameters such as wind direction, wind frequency, wind force, wind force distribution in vertical perspective, eroded rate, buoyancy, sediment diffusion rate, etc. 

Finally we generate the polygon mesh from eroded voxel model using Marching Cubes method. Considering rendering isn't what this research focuses,  we just import the model without extra editing to Unreal Engine and assign them with textures and put them with a terrain plane, then we acquire this final scene.

<iframe width="100%" height="372vh" src="https://www.youtube.com/embed/-J3FovkvftU" frameborder="0" allowfullscreen></iframe>

