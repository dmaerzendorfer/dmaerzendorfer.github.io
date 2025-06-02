---
layout: page
title: Dog
description: I tried out rigging with a Keith Haring Dog.
img: /assets/img/dog/dogRef.png
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

So, I thought I might try out rigging in Blender real quick. The plan was to just make a quick model of a <a href="https://en.wikipedia.org/wiki/Keith_Haring">Keith Haring</a> dog and then rig it. In the end however this *little* project took a bit longer since it is never as easy as one would like. I ended up making some simple VFX, SFX as well as a background tune besides the modelling and rigging, which I then put into a small sample scene in unity. Besides this I looked a bit into LUTs and some grass rendering.


Before I dive into all the steps, here is the result:

<div class="row mt-3">
    <div class="col-sm mt-3 mt-md-0">
        {% include video.liquid path="assets/video/dog/finished.mp4" class="img-fluid rounded z-depth-1" controls=true %}
    </div>
</div>
<div class="caption">
    So in the end I had a dog walking around and when it barks at the magical torus all the colours swap :)
</div>

---

### Modelling and Rigging

The Modeling was quite straight forward, the rigging was a bit rought tho. My first mistake was not using a finished armature and adjusting it to my needs. Instead I created my own armature. The second one was thinking that I wont need a control rig, I only created a deform rig. I thought, I am only making simple animations, I wont need a control rig. Now I can confidently say: true, I did not *need* it. It would have been more convenient and faster however^^ 

I ended up creating three simple animations: Idle, Walk and Bark

<div class="row mt-3">
    <div class="col-sm mt-3 mt-md-0">
        {% include video.liquid path="assets/video/dog/barkAnim.mp4" class="img-fluid rounded z-depth-1" controls=true %}
    </div>
    <div class="col-sm mt-3 mt-md-0">
        {% include video.liquid path="assets/video/dog/walkAnim.mp4" class="img-fluid rounded z-depth-1" controls=true %}
    </div>
    <div class="col-sm mt-3 mt-md-0">
        {% include video.liquid path="assets/video/dog/idleAnim.mp4" class="img-fluid rounded z-depth-1" controls=true %}
    </div>
</div>
<div class="caption">
    For creating the animations I briefly read up on the 12 principles of animation, I tried to get some anticipation, squishing and follow through in there.
</div>

#### Outline
Since the Keith Haring style features nice and bold lines I also wanted to have a nice outline for my model. With some trial and error I ended up with a simple inverse hull outline that I created in Unity. At first I faced trouble with my model since it features too sharp edges for that approach. As a solution I let Unity calculate new normals with a larger smoothing angle. It is still not perfect, but for my usecase I deemed it to suffice. The extra normals however messed up the shading of the model, I wanted to keep it super plain. As a workaround I just used an unlit material, aswell as a invisible material to still let the model cast a shadow.

<div class="row mt-3">
    <div class="col-sm mt-3 mt-md-0">
         {% include figure.liquid loading="eager" path="assets/img/dog/ProblemOfHullShading.png" title="brokenOutline" class="img-fluid rounded z-depth-1" zoomable=true %}
    </div>
    <div class="col-sm mt-3 mt-md-0">
         {% include figure.liquid loading="eager" path="assets/img/dog/solvedOutline.png" title="fixedOutline" class="img-fluid rounded z-depth-1" zoomable=true %}
    </div>
</div>
<div class="caption">
    As you can see: sharp edges lead to visible gaps with the inverse hull outline. The model with extra normals solves this however.
</div>


---
### VFX
You can already see the VFX in the videos further up. They are quite simple, just some motion lines. They are made in Unities ShaderGraph and are triggered by events that I set in the animations.

---
### Audio
For the audio production I used <a href="https://www.image-line.com/">FL Studio</a> as well as the free <a href="https://www.spitfireaudio.com/bbc-symphony-orchestra-discover">BBC Symphony Orchestra Discover</a> virtual instruments.

I started with creating SFX for the bark and footsteps, for that I wanted to keep it simple and just use plain orchestra instruments.

<div class="row mt-3">
    <div class="col-sm mt-3 mt-md-0">
        {% include video.liquid path="assets/video/dog/dogBarkAndVfx.mp4" class="img-fluid rounded z-depth-1" controls=true %}
    </div>
</div>
<div class="caption">
    Just like in Peter and the Wolf, I used horns for the bark. The step sounds are violin plucks however.
</div>

Sadly I do not have very much music theory knowledge, therefore I struggled a bit with the background tune. It was mostly just trying things out until they sounded good. I ended up with a rather nice and curious tune made out of a marimba, percussions and a clarinet. I do like the result, but sadly I do not think it fits with the rest of the demos asthetic. However I also did not have the energy to redo it, so here it stays!

<div class="row mt-3">
    <div class="col-sm mt-3 mt-md-0">
        {% include audio.liquid path="assets/audio/dog/bg.mp3" controls=true %}
    </div>
</div>
<div class="caption">
    This tune just loops in the background. 
</div>

---

### Grass

I built a simple scene with a fence, some green, a sun and a magical torus in Unity with ProBuilder. It felt a bit empty tho. So I looked into adding some grass. I was tempted to go all the way down the rabbit hole and create a compute shader utilising GPU instancing with grass meshes but ultimately decided against it due to the time cost of that. Instead I created a simple grass mesh in blender and used Unities terrain to brush them onto a plane. As it turns out, this also uses GPU Instancing!

<div class="row mt-3">
    <div class="col-sm mt-3 mt-md-0">
         {% include figure.liquid loading="eager" path="assets/img/dog/grass.png" title="grass in blender" class="img-fluid rounded z-depth-1" zoomable=true %}
    </div>
</div>
<div class="caption">
    The grass model I created.
</div>
---

### LUTs

I wanted the bark of the dog to have some kind of effect, so I decided it should be able to swap the demos colour palette! This was inspired by the colour shift in Ape out. I tried this effect out in another demo before, back then I swapped the materials of my gameobjects. This time around I wanted to try something new. So I added a Color Lookup Postprocessing! The LUT textures for that I created using Krita. The result was a bit less controlled, but it was nice to try it out.
