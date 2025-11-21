---
layout: page
title: Blender Skeleton Rig
description: I rigged and animated a Skeleton for University.
img: /assets/img/skellyRig/skellyHero.png
importance: 1
category: blender
related_publications: false
images:
 slider: true
 compare: true
toc:
 sidebar: left
related_posts: false
highlight: false
---

## Intro

This is an assignment I did during my MA Masters. Here I rigged and animated a Skeleton Model in Blender using Rigify!

---

## Result
Here is a playblast of the created animations:


<div class="row mt-3">
    <div class="col-sm mt-3 mt-md-0">
        {% include video.liquid path="assets/video/skellyRig/playblast_SkellyBro.mp4" class="img-fluid rounded z-depth-1" controls=true autoplay=true%}
    </div>
</div>
<div class="caption">
    Three animations were created with the rig. The idle is from Mixamo, the rest I created myself.
</div>

---

## Some more Info

So the course was called **"Animation for Games"** and in class we were working with **Maya**, but already during those lessons I noticed I liked Blender more. So I worked with Blender for my final assignment. The requirements were to rig a character and create three animations for it. It was a free choice whether to use mixamo animations or animate them ourselves and whether we want to model our own character or not.

I decided to not model the character myself and instead focus more on the rigging part. For that I used Rigify, I also retargetet one animation (the idle one) from Mixamo to my custom rig, in order to learn how to do it. For that I used Rokoko. The two remaining animations I created myself. 

The task for the class was also to make sure the model and animation cleanly imports in Unity. I did have some trouble with that, especially since I was a bit extra and created the 'turning into bones' animation. That animation did not import into Unity very well. The reason for that is, that I was unaware on how to cleanly rig such an endeavour, and once I did know how, I did not have enough time to redo it :/
But nonetheless, I learnt a lot during this assignment! :)
