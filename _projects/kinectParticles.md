---
layout: page
title: Kinect-Particles
description: An installation featuring a kinect and particles.
img: assets/img/kinectParticles/hero.png
importance: 1
category: installation
related_publications: false
images:
 slider: true
toc:
 sidebar: left
related_posts: false
highlight: false
---

## Intro
We created a small interactive installation in one of my master classes. However, it sadly was not exhibited since the event it was ment to displayed at was canceled. Though I still want to document at least a little bit here.

The project is a floor projection of a particle simulation, whenever people move over the floor the particles would react. We implemented everything in TouchDesigner. During the conceptual phase we at first tried to solve this via block tracking and an infrared camera. Here we ran into some issues, but we were using a kinect for the infrared so we decided to use the kinect's depthtexture instead. That solved our issues. The simulation is based on a <a href="https://www.patreon.com/posts/pop-fluid-solver-143585157?utm_medium=clipboard_copy&utm_source=copyLink&utm_campaign=postshare_creator&utm_content=join_link">patreon solution</a> that one of our professors provided.

---
## Gallery
Sadly I only have dev footage to show for, but have a look anyway ;)

<iframe width="560" height="315" src="https://www.youtube.com/embed/tGDt6zFUDHo?si=7U5F3Y5ETyIbjh1h" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>
<div class="caption">
    The early iterations of the particle simulations were tested with just mouse inputs.
</div>

<iframe width="560" height="315" src="https://www.youtube.com/embed/EBhIldpIVRc?si=uuHa_g3eF11kpyBA" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>
<div class="caption">
    At the start the blobtracking was running on infrared video footage, but this turned out to noisy and we had trouble mapping the tracking data to the particle space.
</div>

<iframe width="560" height="315" src="https://www.youtube.com/embed/DtYDKtBHYeQ?si=P8UOK1L3iBrBR3hW" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>
<div class="caption">
    In the end I had a setup working with depthtexture and blobtracking. The blobs location is used to move the particles to the right. For a real installation only the particles would be shown.
</div>

---

## Team
- Sarah Lindinger: Particle Simulation
- Kareem Al-Khalily: Particle Simulation
- David Märzendorfer: Blobtracking & Touchdesigner orchestration


