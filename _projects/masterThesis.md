---
layout: page
title: Master-Thesis
description: My Master Thesis.
img: assets/img/masterThesis/drorama.png
importance: 1
category: university
related_publications: false
images:
  slider: true
toc:
  sidebar: left
related_posts: false
---

## Intro

This is a post on my master thesis with the lovely and short name: *"Navigation and Manipulation of Multiple Live Viewpoints for Virtual Reality Head-mounted Displays in a Museum Setting"*. It was part of my MMT master studies at the University of Applied Science in Salzburg. 

The thesis and it's source can be found on my <a href="https://github.com/dmaerzendorfer/masterThesis">Github</a>. 

## What it is about

So basically what this thesis does is compare two distinct methods of placing and manipulating multiple live viewpoints in VR. The two methods are a *restricted yet automate* approach based on a **HoverCam** and a more *free* approach based on a **DroneCam**. 

<div class="row mt-3">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid path="assets/img/masterThesis/droneControls.png" class="img-fluid rounded z-depth-1" zoomable=true %}
    </div>
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid path="assets/img/masterThesis/oceControls.png" class="img-fluid rounded z-depth-1" zoomable=true %}
    </div>
</div>
<div class="caption">
    The two examined approaches.
</div>

During the process of writing the thesis another approach was briefly tested. This was a **OrbitCam** this was however scrapped and replaced with the **HoverCam**.
<div class="row mt-3">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid path="assets/img/masterThesis/OrbitCam.png" class="img-fluid rounded z-depth-1" zoomable=true %}
    </div>
</div>
<div class="caption">
    The Orbit Camera.
</div>

Every Viewpoint-Camera was always connected to a freely placeable and adjustable View-Panel which displays the cameras stream. In addition to that, the selected camera is highlighted with a coloured outline.

<div class="row mt-3">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid path="assets/img/masterThesis/ViewPanel.png" class="img-fluid rounded z-depth-1" zoomable=true %}
    </div>
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid path="assets/img/masterThesis/outlines.png" class="img-fluid rounded z-depth-1" zoomable=true %}
    </div>
</div>
<div class="caption">
    The View-Panel and an example for the outlines.
</div>

The two approaches where compared in a within subject study and assessed with a handful of quantitative questionnaires. The task for the participants was to find three hidden objects in a distant life-sized diorama whilst utilising the systems.

<swiper-container keyboard="true" navigation="true" pagination="true" pagination-clickable="true" pagination-dynamic-bullets="true" rewind="true">
  <swiper-slide>{% include figure.liquid loading="eager" path="assets/img/masterThesis/drorama.png" class="img-fluid rounded z-depth-1" zoomable=true %}</swiper-slide>
  <swiper-slide>{% include figure.liquid loading="eager" path="assets/img/masterThesis/examplePoi.png" class="img-fluid rounded z-depth-1" zoomable=true %}</swiper-slide>
  </swiper-container>
<div class="caption">
    The diorama of the study as well as a hidden object in it.
</div>

The result of study was the the **DroneCam** was favoured for the exploration of the scene however the **HoverCam** was preferred for viewing objects in detail.

## Technical Details

For the thesis I have worked with a Meta Quest 2 in Unity utilising the XR Interaction Toolkit. 


For further detail and sources check out the <a href="https://dmaerzendorfer.github.io/assets/pdf/MasterThesis_ViewPointManipulation_dmaerzendorfer.pdf" target="_blank">thesis</a> itself ;) 

