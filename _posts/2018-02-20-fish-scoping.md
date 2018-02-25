---
layout: post
title: "Fish Scoping"
description: A 3d fish scoping game for Dementia prevention.
image: '/assets/img/fs/2.jpg'
category: 'game'
tag:
- unity3d
- substance painter
twitter_text:  A 3d fish scoping game for Dementia prevention - Fish Scoping made by Lind Chen. 
introduction: The number of elderly people with Dementia in Japan will exceed 7 million in 2025. It's a fish scoping game designed for Dementia prevention of elderly people, who can use the controller Mayukko to exercise.
---

Date : *Winter 2018*

Role : Designer, Programmer, Artist

In January, 2015, The MHLW (Ministry of Health, Labour and Welfare) of Japan have predicted that the elderly with Dementia will be over 7 million people in 2025. Therefore, I create this fish scoping game with a special controller Mayukko to help the elderly exercise and prevent the Dementia.

Mayukko was a joint study between my lab ECL and  System Instruments Co.,Ltd. The official site is [here](http://www.salon-old.jp/fitness/).

<iframe width="100%" height="372vh" src="https://www.youtube.com/embed/ITpMdU-3JjA" frameborder="0" allowfullscreen></iframe>

The animation of fish was implemented by Sin function based on shader without any bone animations. I created this following the GDC presentation of ABZU.

![](/assets/img/fs/3.gif)

Our team has two people. Zhou is the 3d modeler created the white model of the whole scene with 3ds Max. Then I used Substance Painter to paint the materials and enabled GI. Finally add some post effect in the unity.

![](/assets/img/fs/1.jpg)

The water has a very artistic style, and actually it's made from two different plugins. The one is the default simple water in the Standard Assets, while the other one is called DCG Shaders.

![](/assets/img/fs/4.gif)