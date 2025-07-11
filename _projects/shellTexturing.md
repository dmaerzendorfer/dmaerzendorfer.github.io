---
layout: page
title: Shell Texturing
description: I tried out Shell Texturing :)
img: /assets/img/shell/snowLeopardBunny.png
importance: 1
category: graphics
related_publications: false
images:
 slider: true
toc:
 sidebar: left
related_posts: false
highlight: true
---

## Intro

Once again trying out new stuff, this time around **Shell Texturing**! So basically Shell Texturing is a way to fake fur in video games but it does have a few problems (like overdraw and it not working from every angle however we do not care about those right now).   

Basically I saw this <a href="https://www.youtube.com/watch?v=9dr-tRQzij4">video</a> of Acerola and thought I want to try this!
In general this video as well as the blog by <a href="https://tips.hecomi.com/entry/2021/06/27/185835">hecomi</a> and the video by <a href="https://www.youtube.com/watch?v=YghAbgCN8XA">NMG</a> helped me a lot with this. 

**Repository:**   
<a href="https://github.com/dmaerzendorfer/ShellTexturing">https://github.com/dmaerzendorfer/ShellTexturing</a>

---

### What I learnt
- how Shell Texturing works, duh
- how to write HLSL shaders for Unity URP
- how to make shell texturing work with geometry shaders
- lots of hands on knowledge on graphics topics such as shader stages, blending, shader passes, wavefronts, etc. 
- lighting and ShadowCaster Passes!

## What problems I faced
- making my shader work, lol
- take for example the geometry shader, needed two tries and two different tutorials to make it work
- also was thinking to port it into unity's ShaderGraph but thats a big nono with geometry shaders as I found out
- I wanted to add some emission to my fur, however I did not manage to make it look good, so i scrapped it

---

## Gallery

<div class="row mt-3">
    <div class="col-sm mt-3 mt-md-0">
        {% include video.liquid path="assets/video/shell/bouncyBall.mp4" class="img-fluid rounded z-depth-1" controls=true %}
    </div>
    <div class="col-sm mt-3 mt-md-0">
        {% include video.liquid path="assets/video/shell/WindBall.mp4" class="img-fluid rounded z-depth-1" controls=true %}
    </div>
</div>
<div class="caption">
    Since I followed hecomi's solution, my shader also allows for wind-physics (you can also see the problems of shell texturing really well here). I tried to also make a bouncy ball with it, tho it did not come out that well.
</div>

<div class="row mt-3">
    <div class="col-sm mt-3 mt-md-0">
         {% include figure.liquid loading="eager" path="assets/img/shell/giraffeFurBall.png" title="giraffeBall" class="img-fluid rounded z-depth-1" zoomable=true %}
    </div>
    <div class="col-sm mt-3 mt-md-0">
         {% include figure.liquid loading="eager" path="assets/img/shell/snowLeopardBunny.png" title="snowLeopardBunny" class="img-fluid rounded z-depth-1" zoomable=true %}
    </div>
</div>
<div class="caption">
    The shader supports different patterns and one can use any noise texture in order to define how the strands of the fur look like.
</div>

<div class="row mt-3">
    <div class="col-sm mt-3 mt-md-0">
         {% include figure.liquid loading="eager" path="assets/img/shell/weirdlyBlendedFur.png" title="blendFur" class="img-fluid rounded z-depth-1" zoomable=true %}
    </div>
</div>
<div class="caption">
    Whilst working on the shader I also toyed around with the blend options and I managed to get this weird pattern. Not quite sure why that happens but I shall keep note of it if I ever need some buggy looking textures!
</div>
