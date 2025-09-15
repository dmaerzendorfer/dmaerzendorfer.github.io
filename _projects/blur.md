---
layout: page
title: Blur SRP
description: I tinkered around with scriptable render features.
img: /assets/img/blur/blurHero.png
importance: 1
category: graphics
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

So the result of this project is a **Blur Scriptable Render Pass & Postprocess** in Unity 6. But more than that it is actually a learning experience since this is actually not what I set out to create in the first place. So let me tell you a bit more about how I ended up with this result.

---

## Result
Here is the result first though:

<img-comparison-slider>
  {% include figure.liquid path="assets/img/blur/clearCube.png" class="img-fluid rounded z-depth-1" slot="first" %}
  {% include figure.liquid path="assets/img/blur/blurCube.png" class="img-fluid rounded z-depth-1" slot="second" %}
</img-comparison-slider>

**Repository:**   
<a href="https://github.com/dmaerzendorfer/sdfClouds">https://github.com/dmaerzendorfer/sdfClouds</a>


---

## Initial Goal: SDF Clouds

In the beginning I actually set out to create some **raymarched Signed Distance Field(SDF) clouds**. I saw this beautiful <a href="https://blog.maximeheckel.com/posts/real-time-cloudscapes-with-volumetric-raymarching/">post</a> by Maxime Heckel. He created some really nice clouds with React Three Fiber. I wanted to try out SDFs for a while already and was inspired by this post. I thought I would just follow that blog an port it to Unity and learn something in the process.

**Well, I did learn things. But it didn't go as smoothly...**

At first I was hoping to create them in ShaderGraph, but that was quickly changed since I ran into an issue that I have already forgotten about. I then changed to HLSL and kept on working on it.
I got about halfway through the project but somehow the lighting of my clouds was off. I was still rather new to HLSL and it's ins and outs, and could not find out what was going wrong for the love of me. So I decided to scrap the clouds and do something else.

<div class="row mt-3">
    <div class="col-sm mt-3 mt-md-0">
        {% include video.liquid path="assets/video/blur/cloud.mp4" class="img-fluid rounded z-depth-1" controls=true autoplay=true %}
    </div>
</div>
<div class="caption">
    A nice spherical SDF cloud, that sadly is not shaded that nicely...
</div>

---

## Next Idea: Oil Painting Post-processing

So instead I wanted to create a oil painting post-processing effect inspired by this <a href="https://www.youtube.com/watch?v=Md8l_GK9Sfg">talk</a>.
So prior to starting I did lots of research, and quickly noticed that talk was way too high end for my goals. So instead I decided to go with a **anisotropic kuwahara filter** instead. This was mainly based on one of <a href="https://www.youtube.com/watch?v=LDhN-JK3U9g">acerola's videos</a>.

Acerola used the **OnRenderImage** method for the post-process, so I wanted to be fancy and create a **Scriptable Render Feature** to do it instead.
Since I did not know much about scriptable render passes I started out with creating a simple **blur post-process** (yep, that is the one). After that one worked, I went ahead and tried to move on with the kuwahara filter.

**At least that was the plan. But my kuwahara filter failed...**

So I ran into a few issues. For the anisotropic version I need to generate a eigenvector texture which is later down the line used in the shader. And that is the problem. I did not manage to make that happen. Since many tutorials on render passes are outdated and my code was more like a wet towel of a try, it was quite messy. And in addition to that, ChatGPT kept on giving me halucination answers.

So I decided to end it at that, however I do have a possible solution on how to make it work. Basically I have to split it into two render passes and pass the texture between them, <a href="https://docs.unity3d.com/6000.0/Documentation/Manual/urp/render-graph-pass-textures-between-passes.html">this</a> documentation example ought to show me how. Though, I wont try it now.

I do get the feeling I did bite off more than I can chew here. I should first do something easier(like a blur post-process).

---

## Summary

Overall I dreamt a bit too big. I wanted to create SDF clouds, and then a kuwahara post-process when it did not work out. During that I failed often and ran into many walls. In the end stuff did not work and I realised my error of trying to hard to soon. But in luckily in the process I learnt alot about:
- HLSL
- Scriptable Render Passes
- Raymarching
- Blitting

Who does not like some nice walls to run into in order to learn things. I, for my part at least, sure as heck love those walls and the David-sized dents I put into them :)
