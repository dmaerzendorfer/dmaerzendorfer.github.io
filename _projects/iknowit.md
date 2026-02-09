---
layout: page
title: i know it
description: A faux water simulation I did in university.
img: /assets/img/iknowIt/hero.png
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

During my master studies at the FH Hagenberg we created an animation in Blender in our first semester. This project called 'i know it' is based on a poem by Lea (one of my team mates). It features two people in a room that slowly fills with more water. The people are 2D and are created with blenders grease pencil. The Environment and water are 3D. My part in this was creating everything related to the water.

**Team:**
- Lea Obermair: Management, 2D Animation, Audio, Compositing
- Keving Killinger: 3D Environment
- Julian Stögmüller: 2D Animation
- David Märzendorfer: Water Shaders/Animation and Simulation

---

## Result
<iframe width="560" height="315" src="https://www.youtube.com/embed/XCSgj8ea9Gk?si=2JcYq1Ec_CI5HY4C" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>
<div class="caption">
    Only the first half of the animation is done so far.
</div>

---

## Technical Detail

The implementation of the water is one main shader with a layered voronoi texture that flows and distorts naturally. Besides this the water utilises blenders dynamic paint system in order to create outlines around objects that intersect with the water plane.
For shots with water droplets, the drops were animated via a deform rig by hand. Other shots also utilised particle systems that spawn said drops (which in turn are dynamic paint brushes), yet other shots utilised fluid simulations or lattices in order to be deformed.

The tech for the water was inspired by an <a href="https://www.instagram.com/p/Ctj4mgTKEv_/"> instagram post</a>.

---

## Gallery

The implementation was a process, here are some visuals of the development:

<div class="row mt-3">
    <div class="col-sm mt-3 mt-md-0">
        {% include video.liquid path="assets/video/iknowit/dropTestDev.mp4" class="img-fluid rounded z-depth-1" controls=true %}
    </div>
    <div class="col-sm mt-3 mt-md-0">
        {% include video.liquid path="assets/video/iknowit/earlyWaterTestDev.mp4" class="img-fluid rounded z-depth-1" controls=true %}
    </div>
</div>
<div class="caption">
    Early on wave modifiers and a geo node proximity approach for the objection intersection were used.
</div>


<div class="row mt-3">
    <div class="col-sm mt-3 mt-md-0">
        {% include video.liquid path="assets/video/iknowit/earlyToonDev.mp4" class="img-fluid rounded z-depth-1" controls=true %}
    </div>
    <div class="col-sm mt-3 mt-md-0">
        {% include video.liquid path="assets/video/iknowit/toonWaterDev.mp4" class="img-fluid rounded z-depth-1" controls=true %}
    </div>
</div>
<div class="caption">
    A few glances at the early toon tests.
</div>

<div class="row mt-3">
     <div class="col-sm mt-3 mt-md-0">
        {% include video.liquid path="assets/video/iknowit/fluidSimDev.mp4" class="img-fluid rounded z-depth-1" controls=true %}
    </div>
    <div class="col-sm mt-3 mt-md-0">
        {% include video.liquid path="assets/video/iknowit/fluidSimSplashDev.mp4" class="img-fluid rounded z-depth-1" controls=true %}
    </div>
</div>
<div class="caption">
    A some visuals on the early fluid simulation tests.
</div>

<div class="row mt-3">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid path="assets/img/iknowit/RealistCyclesWater.png" class="img-fluid rounded z-depth-1" zoomable=true %}
    </div>
</div>
<div class="caption">
    A more realistic water has also been tried at one point
</div>


---

## Learnings
I learnt a lot about Blender in general and on how to work as a team on a shared project and animation. I got the opportunity to dive further into shaders, animation and modifiers in Blender. 