---
layout: post
title: "Satry Renderer"
description: A Software rasterizing renderer based on CPU.

image: '/assets/img/satry/1.jpg'
category: 'tech practice'
tag:
- rasterization
- rendering
- c++
twitter_text: A Software rasterizing renderer based on CPU - Satry Renderer made by Lind Chen. 
introduction: Satry Renderer is my bachelor graduate project, which contains the basic function of the fixed rendering pipeline, such as vertex transform, texture mapping, software rasterization, normal mapping, environment mapping, alpha blending, etc. 
---

Code : *[Github](https://github.com/cozlind/SatryRenderer)*


Date : *Spring 2016*

<iframe width="100%" height="372vh" src="https://www.youtube.com/embed/wT75H7Lri30" frameborder="0" allow="autoplay; encrypted-media" allowfullscreen></iframe>I spent about two month on this project, one month in searching for various documents, tutorials, one month in coding. Computer graphics is my interest all the time, but it wasn't in the syllabus of my direction. So I took a lot of time to decide what project to attain, which also can help me get a deep understanding of CG. So I choose this software rasterizing renderer instead of general hardware rasterizing with OpenGL or DirectX etc. 

![](/assets/img/satry/2.jpg)

I accomplished an `.obj` model loader which can help me input the standard `.obj` model even with normal texture. Then Satry set four different kinds of light sources to make it looks real. 

![](/assets/img/satry/4.jpg)

This strange model I make is to test the backface culling and alpha blending.

![](/assets/img/satry/3.jpg)

It also supports wireframe, polygon and smooth display modes.

![](/assets/img/satry/8.jpg)

And some shader function like normal mapping, environment mapping.

![](/assets/img/satry/6.jpg)