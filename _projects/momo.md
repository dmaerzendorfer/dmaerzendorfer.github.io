---
layout: page
title: Momo
description: An interative game for a theatre play.
img: https://mezzanintheater.at/wp-content/uploads/2023/05/Momo-%C2%A9-Clemens-Nestroy_57.jpg
importance: 1
category: game
related_publications: false
images:
 slider: true
toc:
 sidebar: left
related_posts: false
---

## Intro

Momo was a student project for the Mezzanin Theater in Graz Austria. It consisted out of an interactive lobby setup for the Mezannin Theater's production of Momo (a childrens book by Michael Ende, I love that story btw).

Details to the theatre play can be found <a href="https://mezzanintheater.at/auffuehrungen/momo/">here</a>.

The project included a handtracking mini-game and a fotobox. The project was implemented by five students (including me) of the University of Applied Science in Salzburg.

## Photobox

The photobox was powered by a Raspberry Pi with a webcam. A Python script was running a OpenGL facial detection to trigger the camera shutter. The taken pictures of theatre guests were later exported to a USB for usage in the play itself. 

My contribution on this part was bugfixing and getting things to run on the Raspberry.
<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/momo/fotoBox1.jpg" title="example image" class="img-fluid rounded z-depth-1" zoomable=true %}
        {% include figure.liquid loading="eager" path="assets/img/momo/fotoBox2.jpg" title="example image" class="img-fluid rounded z-depth-1" zoomable=true %}
    </div>
</div>
<div class="caption">
    The Photobox :)
</div>

## Hand-Tracking Mini-Game

The Hand-Tracking Mini-Game is a game in which the players hands are tracked and water is spraying from their virtual hands' palms. The Players have to aim the water to destroy Grey-Men and reach a Highscore. With increasing score phrases from the book are shown on the screen.

The Handtracking is handled by the <a href="https://developers.google.com/mediapipe">Google Mediapipe</a>. The python code for this runs in Unity and the resulting data points are visualised in a Scene.

The water simulation is handled by the <a href="https://assetstore.unity.com/packages/tools/physics/zibra-liquid-266451">Zibra Liquid Package</a>.

The sounddesign was handled with fmod.
<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/momo/hands1.png" title="example image" class="img-fluid rounded z-depth-1" zoomable=true %}
        {% include figure.liquid loading="eager" path="assets/img/momo/hands2.png" title="example image" class="img-fluid rounded z-depth-1" zoomable=true %}
    </div>
</div>
<div class="caption">
    The Handtracking in Unity :)
</div>

My contribution in this was the implementation of the hand tracking with mediapipe.   
As well as the scoring system, the configuration system for book quotes that can be unlocked via scores, the highscore saving system and the integration of fmod.

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/momo/momo_setup.JPG" title="example image" class="img-fluid rounded z-depth-1" zoomable=true %}
        {% include figure.liquid loading="eager" path="assets/img/momo/momoFinalRelease.png" title="example image" class="img-fluid rounded z-depth-1" zoomable=true %}
    </div>
</div>
<div class="caption">
    The Handtracking in in Action :)
</div>
