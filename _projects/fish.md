---
layout: page
title: Fish
description: I modelled a fish and displayed it a bit.
img: /assets/img/fish/tonsOfFish.png
importance: 1
category: modelling
related_publications: false
images:
 slider: true
toc:
 sidebar: left
related_posts: false
highlight: false
---

## Intro

Recently I decided I want to try something more artsy and less cody. So therefore I tried my hand at modelling a fish in Blender and displaying it a bit! 

---

### Blender
For the basic fish model I followed a tutorial by <a href="https://www.youtube.com/watch?v=jn9X9YSqJDc">baeac</a>. For my fish I chose a common carp.

<div class="row mt-3">
    <div class="col-sm mt-3 mt-md-0">
         {% include figure.liquid loading="eager" path="assets/img/fish/fish.png" title="fishyInBlender" class="img-fluid rounded z-depth-1" zoomable=true %}
    </div>
    <div class="col-sm mt-3 mt-md-0">
         {% include figure.liquid loading="eager" path="assets/img/fish/fishyInUnity.png" title="fishyInUnity" class="img-fluid rounded z-depth-1" zoomable=true %}
    </div>
</div>
<div class="caption">
    The modelling part was quite fun, I had to find my way around Blender first tho. I also exported the model to Unity to see what the process is like. During that I also ran into a small issue with backface culling, but that was easily fixed.
</div>

I also animated my fish in Blender to form a gigantic swarm. I guess that's not how they act in real life but who cares for that anyway ¯\\_(ツ)_/¯

<div class="row mt-3">
    <div class="col-sm mt-3 mt-md-0">
        {% include video.liquid path="assets/video/fish/fishSwarm.mp4" class="img-fluid rounded z-depth-1" controls=true %}
    </div>
</div>
<div class="caption">
    The model is used in a particle system which is influenced by a flow to follow a nice curvature.
</div>

---

### TouchDesigner

Besides tinkering about in Blender I also wanted to use my model in TouchDesigner. I don't have much experience with TouchDesigner, but I know what it is capable of, so I wanted to give it a try.

For this I followed some tutorials by <a href="https://www.youtube.com/@DeanCheesman">Dean Cheesman</a>.

<div class="row mt-3">
    <div class="col-sm mt-3 mt-md-0">
        {% include video.liquid path="assets/video/fish/fishSwim.mp4" class="img-fluid rounded z-depth-1" controls=true %}
    </div>
    <div class="col-sm mt-3 mt-md-0">
        {% include video.liquid path="assets/video/fish/fishSwimBlue.mp4" class="img-fluid rounded z-depth-1" controls=true %}
    </div>
</div>
<div class="caption">
    The basic concept for this is to have fish boids that use my model with some image magic on top to make it look nice. Furthermore, a text particle system that is displaced by the fish, is also layered on top. In the beginning, I also wanted to make the fish interactive by somehow utilising camera input but ultimately decided against it since it was already taking long enough to make. 
</div>