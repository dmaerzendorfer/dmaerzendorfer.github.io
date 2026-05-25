---
layout: page
title: FlowingSand
description: An interactive installation for the AEC Deepspace.
img: assets/img/flowingSand/hero.png
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

<a href="https://github.com/dmaerzendorfer/DeepspaceFlowingSand">FlowingSand</a> is an interactive installation that was created during my studies in Hagenberg. It was designed for the Deepspace, a 8k 16x9m wall/floor projection space with integrated motion tracking, of the <a href="https://ars.electronica.art/news/en/">AEC</a> in Linz.

FlowingSand was coded in Processing and uses Open Sound Control (OSC) to connect to a Reaper-Session to influence an interactive soundtrack.
It features a Flow-Field that influces particles that avoid any people that stand in their way. The Flow-Field and Particles support four different behaviours to mix up the experience eG Particles with trails, a more erradic Flow-Field etc.

The Processing application was optimised to maximise the framerate: the particles are omitted if they are too dense to reduce overdraw and particles are pre-rendered into a texture to save on draw-calls.

---
## Team
- Sarah Lindinger: Audio
- David Märzendorfer: Coding

--- 
## Gallery

<swiper-container keyboard="true" navigation="true" pagination="true" pagination-clickable="true" pagination-dynamic-bullets="true" rewind="true">
  <swiper-slide
  style=""
  ><iframe width="560" height="315" src="https://www.youtube.com/embed/pCYgdCk4LtI?si=51QIjXufeismy1UY" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>
  </swiper-slide>
  <swiper-slide><iframe width="560" height="315" src="https://www.youtube.com/embed/ueWrIRjIjcc?si=56zidIrk5NhM25l-" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>
  </swiper-slide>
  <swiper-slide><iframe width="560" height="315" src="https://www.youtube.com/embed/fM7LzW3zdSQ?si=IU78OGljI4wGtmSa" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>
  </swiper-slide>
  </swiper-container>
<div class="caption">
    Videos of the Installation
</div>
