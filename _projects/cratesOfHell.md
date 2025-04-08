---
layout: page
title: Crates of Hell
description: My first solo game jam.
img: /assets/img/cratesOfHell/fire.png
importance: 1
category: game
related_publications: false
images:
 slider: true
toc:
 sidebar: left
related_posts: false
highlight: false
---

## Intro

This time around I decided I want to give soloing a game jam a try. Just to see what comes of it. For the jam I chose a 72h one, namely the <a href="https://ldjam.com/events/ludum-dare/57">57th Ludum Dare</a>!

The topic of the jam was:

<h1 style="text-align:center"><b>Depths</b></h1>

And oh boy, I hade no idea what to make of it. Turns out brainstorming is way harder alone but in the end I created:
<div class="row mt-3">
    <div class="col-sm mt-3 mt-md-0">
         {% include figure.liquid loading="eager" path="assets/img/cratesOfHell/TitleBanner.png" title="cratesOfHell" class="img-fluid rounded z-depth-1" zoomable=true %}
    </div>
</div>
<div class="caption">
    Crates of Hell simulates the depths of hell by dooming you to endlessly organise creates whilst your supervisor talks to you.
</div>

The game can be found on <a href="https://maerzy.itch.io/crates-of-hell">itch</a> and the source code on my <a href="https://github.com/dmaerzendorfer/ludumDare25">github</a>.

---

## Technical Details
Since I knew I was going at it alone I decided on a minimalistic artstyle beforehand.
Since modelling would take too long it needed to be 2D. So before the jam I was prepping a bit and created a plain menu scene, a scene manager, an audio manager as well as a pixelation post-processing setup. 
For the sprites I decided to use simple vector art that I created in <a href="https://www.figma.com">Figma</a>. For Audio I got a simple beat from <a href="https://www.bandlab.com">BandLab</a>. For the SFX I mostly used some free samples of a drumkit.
The engine I used was <a href="https://www.unity.com">Unity 6</a> and for my IDE I used <a href="https://www.jetbrains.com/rider/">Rider</a>.

## The Process

### Day One
On day one I started out with brainstorming on what to do. My original idea was to create a game about dreams! In that game you would have been in different dream worlds. In order to get to the next one you would need to solve small tasks and puzzles. For example one NPC lost is wrench and you needed to find it. Once the NPC was happy you could control him (and his wrench) to solve another puzzle etc.

So, I started out with creating top-down pawns you could move around and maybe pickup some things with:
<div class="row mt-3">
    <div class="col-sm mt-3 mt-md-0">
        {% include video.liquid path="assets/video/cratesOfHell/day1.mp4" class="img-fluid rounded z-depth-1" controls=true %}
    </div>
</div>
<div class="caption">
    This was at middle of day one: One could select pawns and move them around. Later on I also added obstacles in the form of <i>crates</i> and a hammer you could pick up. At this point I already noticed I wont have enough time create that game. I needed to change something.
</div>

### Day Two
I was really stumped, since I did not know in what direction I wanted to take this. Especially since I did not know how to incorporate the theme of **Depths**. Whilst I was still working on the Hammers animation I told myself: screw it, let's just follow the fun. So I made the hammer massive, made it smack around crates and juiced everything up. Thats how I ended up with:

<div class="row mt-3">
    <div class="col-sm mt-3 mt-md-0">
        {% include video.liquid path="assets/video/cratesOfHell/day2.mp4" class="img-fluid rounded z-depth-1" controls=true %}
    </div>
</div>
<div class="caption">
    Day two was over, I pivoted towards the theme of <i>Depths of Hell</i> and had a somewhat polished product. But it was lacking one important thing: an actual gameloop.
</div>

### Day Three
This day I focused on creating a gameloop. I really did not want to go the easy (and boring) route of adding enemies that swarm the player and you need to smack away. Instead I made the game about organising crates by smacking them into a delivery zone. A snarky and rude supervisor is giving you comments during each delivery.

<div class="row mt-3">
    <div class="col-sm mt-3 mt-md-0">
        {% include video.liquid path="assets/video/cratesOfHell/day3.mp4" class="img-fluid rounded z-depth-1" controls=true %}
    </div>
</div>
<div class="caption">
    I wrote about 100 lines for the supervisor. At some point I had to stop, though in game he keeps on going (and repeating itself) forever. Since after all, there is no escape from (organising crates in) hell.
</div>

So whilst the process itself was a struggle I am happy with the result in the end. There are stil a few things I am not too happy about (like the pixelation effect is not clean enough...). But for a first time solo jam experience it is quite nice.

## Gallery
<div class="row mt-3">
    <div class="col-sm mt-3 mt-md-0">
         {% include figure.liquid loading="eager" path="assets/img/cratesOfHell/menuScreen.png" title="menuScreen" class="img-fluid rounded z-depth-1" zoomable=true %}
    </div>
    <div class="col-sm mt-3 mt-md-0">
         {% include figure.liquid loading="eager" path="assets/img/cratesOfHell/ingame.png" title="ingame" class="img-fluid rounded z-depth-1" zoomable=true %}
    </div>
</div>