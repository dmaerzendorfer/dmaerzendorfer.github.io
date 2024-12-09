---
layout: post
title: A little Devblog on Prototyping
date: 2024-03-05 12:00:00
description: The story of how the main mechanic in one of my university projects was created
tags: Unity Prototypes
categories: Unity
thumbnail: assets/img/devblog01/heroBanner.jpg
images:
  slider: true
toc:
  sidebar: left
related_posts: false
---


## What is this post about?

This post is less technical and more of a little story on how the main mechanic for one of my university projects was found. The project in question is <a href ="https://portfolio.fh-salzburg.ac.at/projects/2024-the-wuzeling">The Wuseling</a>. Wuseling is a four player local  2.5D brawler about bearded mages that battle it out in an arena.

The game was written in Unity and my part in this project was mainly Gameplay-Programming and a bit of Game Design. At the start of the project we had to find our main mechanic so we created a few prototypes, which I often ended up programming.

## Storytime! So what was our process?

In hindsight we actually somewhat followed the double/triple diamond design model.

### The Diamond Model

I first got into contact with this when I was reading <a href="https://www.amazon.com/Design-Everyday-Things-Revised-Expanded-ebook/dp/B00E257T6C">The Design of Everyday Things</a> by Don Norman (highly recommend that book by the way). 

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/devblog01/doubleDiamond.png" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    The double diamond design model
</div>

Basically the design model describes the process of designing solutions for problems. Firstly one needs to define the problem itself. For this, one broadens their view to find possible causes for the problem to then converge back to find a concrete definition for the problem. Afterwards the same is done for finding a solution. Many possible solutions are found to converge back to a concrete solution again.

Besides the double diamond model there also exists the triple diamonds model:

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/devblog01/tripleDiamond.png" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    The triple diamond design model
</div>


This graphic is by Karl T. Ulrich, who also has a lovely explanation on the triple diamond model <a href="https://ktulrich.com/the-triple-diamond-model-of-design/#:~:text=The%20triple%20diamond%20model%20focuses,establishing%20a%20product%20architecture%2C%20or">here</a>.
But in short, it is quite similar to the double diamond model. It however adds another diamond in the middle, which focuses on understanding the needs of the customer/user.

**As a little sidenote:** personally I always tend to call it the tennis-ball-snake model, as it looks like a snake that has swallowed a few tennis balls.   
Just now I was once again wondering why my google search for "tennis-ball-snake design model" didn't get me any good results ^^'


### Human-Centered Design Process

Don Norman also describes the Human-Centered Design Process. This is an iterative approach on constantly improve a design/prototype. I think the following grafic describes it nicely.

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/devblog01/HumanCenteredDesign.png" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    The Human-Centered Design Process
</div>


This is also often called the *spiral method* (even though it is depicted as a circle here). So basically one makes observations on the intended target population, generate ideas, produce prototypes and tests them. This can be repeated until satisfied.

## Back to Wuseling!
Enough about the theory behind it! Let's see how we applied this to our project. Basically we did not follow this concrete design process, we just did things our way. That however ended up with certain similarities. Let's wander through our process with some nice pictures!

### Definition of what we want
At the beginning we started with establishing the approximate range within which our mechanic should operate. To do this, we sketched out some rough guidelines:
- it should be physics based
- it should be somewhat chaotic (it was a bit tough to find the correct balance of chaos)
- it should include some pulling or pushing of players

### Prototype Ideas: Lots of them!
With this we started to write down some possible ideas that fit the theme. Let's just look at some sketches so I don't have to explain every single one:

<div class="row mt-3">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/devblog01/hook.jpg" class="img-fluid rounded z-depth-1" zoomable=true %}
    </div>
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/devblog01/charge.jpg" class="img-fluid rounded z-depth-1" zoomable=true %}
    </div>
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/devblog01/cthulhu.jpg" class="img-fluid rounded z-depth-1" zoomable=true %}
    </div>
</div>
<div class="row mt-3">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/devblog01/dinghy.jpg" class="img-fluid rounded z-depth-1" zoomable=true %}
    </div>
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/devblog01/icey.jpg" class="img-fluid rounded z-depth-1" zoomable=true %}
    </div>
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/devblog01/jetpacks.jpg" class="img-fluid rounded z-depth-1" zoomable=true %}
    </div>
</div>
<div class="row mt-3">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/devblog01/magnet.jpg" class="img-fluid rounded z-depth-1" zoomable=true %}
    </div>
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/devblog01/needle.jpg" class="img-fluid rounded z-depth-1" zoomable=true %}
    </div>
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/devblog01/spear.jpg" class="img-fluid rounded z-depth-1" zoomable=true %}
    </div>
</div>
<div class="row mt-3">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/devblog01/spin.jpg" class="img-fluid rounded z-depth-1" zoomable=true %}
    </div>
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/devblog01/rubberLink.jpg" class="img-fluid rounded z-depth-1" zoomable=true %}
    </div>
</div>
<div class="caption">Mechanic Sketches</div>

After we decided on our favourites we actually made quick and dirty prototypes on the mechanics and decided on the one we liked most:

<swiper-container keyboard="true" navigation="true" pagination="true" pagination-clickable="true" pagination-dynamic-bullets="true" rewind="true">
  <swiper-slide>{% include figure.liquid loading="eager" path="assets/img/devblog01/Jetpacks.gif" class="img-fluid rounded z-depth-1" zoomable=true %}</swiper-slide>
  <swiper-slide>{% include figure.liquid loading="eager" path="assets/img/devblog01/MagnetsGoYeet.gif" class="img-fluid rounded z-depth-1" zoomable=true %}</swiper-slide>
  <swiper-slide>{% include figure.liquid loading="eager" path="assets/img/devblog01/bombsGoBoom.gif" class="img-fluid rounded z-depth-1" zoomable=true %}</swiper-slide>
  <swiper-slide>{% include figure.liquid loading="eager" path="assets/img/devblog01/ChargeShot.gif" class="img-fluid rounded z-depth-1" zoomable=true %}</swiper-slide>
</swiper-container>
<div class="caption">Dirty Prototypes</div>

<h2 style="text-align:center">The winner was <b>Rubber-Links</b>!</h2>
We decided on focusing on the *Rubber-Links* mechanic. Basically players can shoot two ends of a rubber band and activate the rubber band in order to pull any connected things together. This also allows players to only shoot one end of the Link and activate the rubber band whilst it is still connected to oneself to dash forward! In combination with environmental elements such as boom-barrels this mechanic was promising.

With this we started into further iterations and improvements of the mechanics:

<!-- gallery on the development process -->
<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/devblog01/firstGamePrototype.gif" title="example image" class="img-fluid rounded z-depth-1" zoomable=true %}
    </div>
</div>
<div class="caption">
    The first iteration of the prototype added some more rope physics (and placeholder tanks)
</div>

Over time the mechanic was further improved by adding some aim assist, less wobbly ropes as well as better player models.
<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/devblog01/linkShot.gif" title="linkShot" class="img-fluid rounded z-depth-1" %}
        {% include figure.liquid loading="eager" path="assets/img/devblog01/dash.gif" title="dash" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    Homing Rubber-Links and Dashing
</div>

### Conclusion on our Prototyping Process

We somewhat applied the "tennis-ball-snake" model. We first started with defining what we wanted. Then wrote down some possible mechanics, narrowed it down to our favourites. Then we created some small and dirty prototypes of these to actually tested them. Then we decided on a favourite again. Then we scrapped the dirty prototype code (yay to dirty prototyping!). Finally we coded it clean again and started the spiral model of constantly improving on the mechanic.

I have to say however, in this specific example we never found a satisfying end for the mechanic. The cycle continued on and on. In the end Wuseling was scrapped due to many reasons which I won't go into detail here. Though I think if we would have kept on it, at some point we would have ended up with the perfect mechanic that just 100% clicks :)



That's it,  
Thanks for reading,  
Cheers, David :)