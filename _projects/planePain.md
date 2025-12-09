---
layout: page
title: PlanePain
description: A six player local game about painful planes!
img: assets/img/planePain/hero.png
importance: 1
category: game
related_publications: false
images:
 slider: true
toc:
 sidebar: left
related_posts: false
highlight: true
---

## Intro

<a href="https://maerzy.itch.io/planepain">PlanePain</a> is a local versus game for up to six players! It was created as an assignment during my Advanced Game Design course in my master studies. An inspiration for the project was <a href="https://achtungkurve.com/">Achtung die Kurve</a>. 

---

<iframe width="560" height="315" src="https://www.youtube.com/embed/xMMr_efsZIE?si=57xrUSmKyEgBcECQ" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>
<div class="caption">
    Gameplay of PlanePain
</div>

In the game each player controls a paper plane with two keyboard buttons they choose in the menu. The controls and game loop are simple:
- planes constantly fly forward
- planes can be steered left and right
- planes can shoot darts to the left and right (with a cooldown)
- if a plane is hit by a dart it turns into a copy of the shooter of the dart!
- clones behave just like the shooter, meaning they steer the same and also shoot at the same time
- last plane remaining wins!

The settings in the menu give players the option to customise various things such as shoot cooldown, screen wrapping, initial player clones and more! 

---

## Team
- Philipp Wenisch: Art
- David Märzendorfer: Game Design, Coding & Audio

---

## Gallery

<div class="row mt-3">
    <div class="col-sm mt-3 mt-md-0">
        {% include video.liquid path="assets/video/planePain/settingsClip.mp4" class="img-fluid rounded z-depth-1" controls=true %}
    </div>
</div>
<div class="caption">
    The settings allow for some fastly different gameplay, such as stationary machine gun planes!
</div>

<div class="row mt-3">
    <div class="col-sm mt-3 mt-md-0">
        {% include video.liquid path="assets/video/planePain/gamePlayClip.mp4" class="img-fluid rounded z-depth-1" controls=true %}
    </div>
</div>
<div class="caption">
    Player fly around and shoot each other.
</div>



<swiper-container keyboard="true" navigation="true" pagination="true" pagination-clickable="true" pagination-dynamic-bullets="true" rewind="true">
  <swiper-slide>{% include figure.liquid loading="eager" path="assets/img/planePain/gameplay.png" class="img-fluid rounded z-depth-1" zoomable=true %}</swiper-slide>
  <swiper-slide>{% include figure.liquid loading="eager" path="assets/img/planePain/playerSelect.png" class="img-fluid rounded z-depth-1" zoomable=true %}</swiper-slide>
  <swiper-slide>{% include figure.liquid loading="eager" path="assets/img/planePain/spawn.png" class="img-fluid rounded z-depth-1" zoomable=true %}</swiper-slide>
  <swiper-slide>{% include figure.liquid loading="eager" path="assets/img/planePain/titleScreen.png" class="img-fluid rounded z-depth-1" zoomable=true %}</swiper-slide>
 
  </swiper-container>
<div class="caption">
    Pictures of the game :3
</div>

