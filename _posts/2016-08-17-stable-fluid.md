---
layout: post
title: "Stable Fluid"
description: 2d grid based fluid simulation.
image: '/assets/img/ns/3.gif'
category: 'tech practice'
tag:
- fluid
- simulation
- 2d
- unity3d
twitter_text: 2d grid based fluid simulation - Stable Fluid made by Lind Chen. 
introduction: Stable Fluid is a algorithm proposed by Jos Stam to simulate grid based fluid simulation. This is a 2d implementation made with unity3d.
---

Date : *summer 2016*

Stable Fluid is a solver proposed by Jos Stam to simulate grid based fluid simulation. [The paper](http://www.dgp.toronto.edu/people/stam/reality/Research/pdf/ns.pdf) first proposed in Siggraph 99'. This is a 2d implementation made with unity3d. 

![](/assets/img/ns/2.jpg)

It solve the Navier-Stokes Equasion based on grid. 

$$
\displaystyle \rho {\frac {\mathrm {D} \mathbf {v} }{\mathrm {D} t}}=-\nabla p+\nabla \cdot \mathbb {T} +\rho \mathbf {f}
$$

Then arrange the calculation into 4 steps: add force, advection, diffusion and projection.

![](/assets/img/ns/3.jpg)

I try implement this paper during the summer vacation after graduation and spent 1 month trying to figure out the strange fluid mechanics theory. I didn't know the difference between various fluid algorithm that time. Whatever the final result is amazing.

![](/assets/img/ns/1.gif)



