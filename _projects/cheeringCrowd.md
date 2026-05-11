---
layout: page
title: CheeringCrowd
description: A simple crowd that cheeres and is trigger via a button on your phone.
img: assets/img/cheeringCrowd/crowdCheer.png
importance: 1
category: installation
related_publications: false
images:
 slider: true
toc:
 sidebar: left
related_posts: false
highlight: true
---

## Intro

<a href="https://maerzy.itch.io/cheeringcrowd">CheeringCrowd</a> is a small installation piece that was created for my master studies in Hagenberg. It features a crowd of characters than can be triggered via a button to cheer.

The tech setup is based on a Unity Application that uses ZXing to create a QR-Code to a Netlify web-app. On this web-app there is a button which writes into a realtime Firelink DB, which is in turn read by Unity to trigger an animation. The scope of this project is quite small but I am really happy that the QR-Code to Website on Phone works so smoothly. I might utilise this tech again in some future works :)

---

<iframe width="560" height="315" src="https://www.youtube.com/embed/GborzfqDqzo?si=lvbG4H1kRRn4cavU" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>
<div class="caption">
    Cheering
</div>

---

## Team
- Philipp Wenisch: Modelling
- Kareem Al-Khalily: Animating
- David Märzendorfer: Coding & Audio

---

## Gallery

<swiper-container keyboard="true" navigation="true" pagination="true" pagination-clickable="true" pagination-dynamic-bullets="true" rewind="true">
  <swiper-slide>{% include figure.liquid loading="eager" path="assets/img/cheeringCrowd/crowdCheer.png" class="img-fluid rounded z-depth-1" zoomable=true %}</swiper-slide>
  <swiper-slide>{% include figure.liquid loading="eager" path="assets/img/cheeringCrowd/qrCode.png" class="img-fluid rounded z-depth-1" zoomable=true %}</swiper-slide>
  </swiper-container>
<div class="caption">
    Pictures of the crowd :3
</div>
<div class="row mt-3">
    <div class="col-sm mt-3 mt-md-0">
       {% include figure.liquid loading="eager" path="assets/img/cheeringCrowd/PhoneView.png" class="img-fluid rounded z-depth-1" zoomable=true %}
    </div>
</div>
<div class="caption">
    The web interface is quite barebone and simple
</div>

