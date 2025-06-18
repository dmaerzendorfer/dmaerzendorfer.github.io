---
layout: post
title: Catlike Coding Tutorials
date: 2025-03-09 12:00:00
description: I plan to do all the Catlike Coding Tutorials
tags: Unity Tutorial Shader Graphics
categories: Unity
thumbnail: assets/img/catlikeCoding/icon.png
images:
  slider: true
toc:
  sidebar: left
related_posts: false
---

# Intro
A while I go I decided I want to do **ALL** <a href="https://catlikecoding.com/unity/tutorials/">Catlike Coding</a> Unity tutorials. The reason for that was that I just want to further increase my knowledge of Unity and especially dip a bit further into shaders and graphics programming. If possible I also want to try to apply the things from the tutorial to something new or at least try to alter or complement the tutorials end results somehow.

---

## The Basics Tutorials
For the basic tutorials I learnt some new things about: 
- Surface-Shaders
- GPU Instancing
- Shader-Graph and custom functions in it
- Performance Measuring in Unity
- Compute Shaders
- The Unity Job System

See the <a href="https://catlikecoding.com/unity/tutorials/basics/">original site</a> for the tutorials.

**Repo:** <a href="https://github.com/dmaerzendorfer/CatlikeCodingBasics">https://github.com/dmaerzendorfer/CatlikeCodingBasics</a>

### Gallery
<div class="row mt-3">
    <div class="col-sm mt-3 mt-md-0">
        {% include video.liquid path="assets/video/catlikeCoding/basics/clock.mp4" class="img-fluid rounded z-depth-1" controls=true autoplay=true %}
    </div>
    <div class="col-sm mt-3 mt-md-0">
        {% include video.liquid path="assets/video/catlikeCoding/basics/clock2.mp4" class="img-fluid rounded z-depth-1" controls=true %}
    </div>
</div>
<div class="caption">
    The first part was creating a clock in Unity. Just for fun I also updated it so the clocks hour indicators also rotate.
</div>

<div class="row mt-3">
    <div class="col-sm mt-3 mt-md-0">
        {% include video.liquid path="assets/video/catlikeCoding/basics/graph.mp4" class="img-fluid rounded z-depth-1" controls=true autoplay=true %}
    </div>
    <div class="col-sm mt-3 mt-md-0">
        {% include video.liquid path="assets/video/catlikeCoding/basics/graph2.mp4" class="img-fluid rounded z-depth-1" controls=true %}
    </div>
</div>
<div class="caption">
    For the second part a simple 2D graph was created that I then augmented to also feature a depth with delayed and shifted functions.
</div>

<div class="row mt-3">
    <div class="col-sm mt-3 mt-md-0">
        {% include video.liquid path="assets/video/catlikeCoding/basics/morphingGraph.mp4" class="img-fluid rounded z-depth-1" controls=true %}
    </div>
    <div class="col-sm mt-3 mt-md-0">
        {% include video.liquid path="assets/video/catlikeCoding/basics/computeGraph.mp4" class="img-fluid rounded z-depth-1" controls=true %}
    </div>
</div>
<div class="caption">
    In the third part of the tutorial the graph was updated to display mathematical surfaces and smoothly morph to and from them. After measuring the performance it was also upgraded to run via a compute shader with GPU Instancing.
</div>

<div class="row mt-3">
    <div class="col-sm mt-3 mt-md-0">
        {% include video.liquid path="assets/video/catlikeCoding/basics/fractal.mp4" class="img-fluid rounded z-depth-1" controls=true %}
    </div>
    <div class="col-sm mt-3 mt-md-0">
        {% include video.liquid path="assets/video/catlikeCoding/basics/organicFractal.mp4" class="img-fluid rounded z-depth-1" controls=true %}
    </div>
</div>
<div class="caption">
    Lastly the Unity Job system was used to create a fractal. The fractal also utilises GPU instancing and was later updated to create more organic fractals.
</div>

<div class="row mt-3">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid path="assets/img/catlikeCoding/basics/flower.png" class="img-fluid rounded z-depth-1" zoomable=true %}
    </div>
</div>
<div class="caption">
    For the organic fractals I also brushed up my blender skills and created a simple flower model.
</div>

---

## Pseudorandom Noise Tutorials

For the basic tutorials I learnt some further things about: 
- Hashing functions
- Burst Optimisation and the Unity Job System
- Value and Gradient Noise

See the <a href="https://catlikecoding.com/unity/tutorials/pseudorandom-noise/">original site</a> for the tutorials.

During this tutorial various variations of noise were implemented, these include:
- Value Noise
- Perlin Noise
- Voronoi Noise
- Simplex Noise

Each noise is available in 1D, 2D and 3D. Furthermore each noise includes settings for variance and turbulence as well as tiling.

### Gallery
<div class="row mt-3">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid path="assets/img/catlikeCoding/pseudoRandomNoise/hashWithVerticalOffset.png" class="img-fluid rounded z-depth-1" zoomable=true %}
    </div>
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid path="assets/img/catlikeCoding/pseudoRandomNoise/hashScaledAndRotated.png" class="img-fluid rounded z-depth-1" zoomable=true %}
    </div>
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid path="assets/img/catlikeCoding/pseudoRandomNoise/torusShape.png" class="img-fluid rounded z-depth-1" zoomable=true %}
    </div>
</div>
<div class="caption">
    The first part was creating a hashing function implementation (SmallHash). The hashing was then used to create noise.
</div>

<div class="row mt-3">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid path="assets/img/catlikeCoding/pseudoRandomNoise/3dPerlinNoiseSphere.png" class="img-fluid rounded z-depth-1" zoomable=true %}
    </div>
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid path="assets/img/catlikeCoding/pseudoRandomNoise/3dSphereSimplexValueNoise.png" class="img-fluid rounded z-depth-1" zoomable=true %}
    </div>
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid path="assets/img/catlikeCoding/pseudoRandomNoise/VoronoiWorleyF2MinusF1.png" class="img-fluid rounded z-depth-1" zoomable=true %}
    </div>
</div>
<div class="caption">
    Later on various variations of noise, such as Perlin, Voronoi and Simplex were added. The Voronoi noise also features multiple distance and evaluation functions to, for instance, use the second closest Voronoi point.
</div>

---

## Procedural Meshes Tutorial

<h3 style="text-align:center">WIP</h3>

