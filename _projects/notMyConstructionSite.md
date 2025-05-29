---
layout: page
title: Nicht meine Baustelle
description: An art installation.
img: assets/img/nmcs/NMCS_hero.jpeg
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

**Nicht meine Baustelle** (german for "Not my construction site") is an art installation and the masters project of:

- Annika Braun
- Anja Gutschmidt
- Alina Traun
- Sebastian Scholtze

The project is an interactive exhibit trying to get people more involved in politics. The exhibit is structured into seven stations that try to highlight some aspects on why people might not want to be invovled. Overall the exhibit itself is themed like a proper construction site you can find in your local city.

Two of the stations involve some technical doodads. Thats where I come in.
Together with Alexander Gewald and Nico Weiser (two of my master degree colleagues) we helped them to make these station reality. 

**My role** in this was **technical consultant** in the planning phase, **management** of the technical team as well as **implementing** the solution.

The two stations in question are:

### The Dixi Loo
This station tries to allow people to let out whatever bothers them. It is installed in a dixie loo and asks the participant to get into the loo, close the door, open the loo lid, leave a voice message, close the lid and then receive the message of his/her predecessors.

The technical implementation of this station involves a **Raspberry PI 3B+** that is connected to a **microphone** as well as a **bluetooth speaker** and has four buttons connected to its GPIO pins. The **four buttons** are:
- a button for checking if the door is closed
- a button for checking if the lid is open or closed
- a button for skipping through audio recordings
- a button for reseting the recording process

The raspi is hidden inside the loo and is powered via a generic powerbank. The recordings are saved on a external USB-Stick for easy curation. The system includes some extra audio instructions for the user on when the recording starts and on when the message has been saved. The programm itself on the raspi is written in python. The raspi also automatically connects to its trusted bluetooth speaker due to an extra script that runs whenever a terminal is opnend and the python-script with the loo logic runs automatically once the Raspian OS desktop is loaded.


### The Pylons
This station tries to bring some attention to the fact that some people might be afraid of showing their opinions in public. For this a small podium was built with some questions of which the participants takes one and two answer pylons. The depending on whether the participant lifts the yes or the no pylon a booing or a cheering sound is played.

Once again this station is powered by a **Raspberry PI 3B+**, a **bluetooth speaker**, some **buttons** and a **powerbank**.

The buttons are installed as preasure plates under the pylons and are hooked up to the raspis GPIO pins. Just as with the loo station the buttons have been solder by yours truly to some cables for convenient usage. Similiarly to the loo this raspi automatically boots into the pylon python script on startup.

### Troubles we faced

The most anyoying part of this project was getting the raspi to **consistently autostart** into the python scripts. We have tried many different approaches such as chrontabs (which ultimately did not work for this case since we had to make sure both bluetooth and the audio setup where available to the OS). In the end this was **solved via** **custom .desktop files** that run a **launcher shell script** once the desktop is loaded which in turn opens a terminal window **that runs** the **python script**.

---
### Awards
The installation was also awared by the <a href="https://creativclub.at/">CCA</a> and <a href="https://www.adc.de/">ADC</a> in 2025. It won 
- 3x Gold ADC Talent Award
- 1x Bronze CCA Venus Award
- 3x Shortlist CCA Venus Award

- ADC CC Stuttgart Winner

---

## Gallery

<div class="row mt-3">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid path="assets/img/nmcs/toiletView.jpg" class="img-fluid rounded z-depth-1" zoomable=true %}
    </div>
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid path="assets/img/nmcs/nmcs_station3.jpeg" class="img-fluid rounded z-depth-1" zoomable=true %}
    </div>
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid path="assets/img/nmcs/nmcs_station4.jpeg" class="img-fluid rounded z-depth-1" zoomable=true %}
    </div>
</div>

<swiper-container keyboard="true" navigation="true" pagination="true" pagination-clickable="true" pagination-dynamic-bullets="true" rewind="true">
  <swiper-slide>{% include figure.liquid loading="eager" path="assets/img/nmcs/nmcs_display.jpeg" class="img-fluid rounded z-depth-1" zoomable=true %}</swiper-slide>
  <swiper-slide>{% include figure.liquid loading="eager" path="assets/img/nmcs/nmcs_flyer.jpeg" class="img-fluid rounded z-depth-1" zoomable=true %}</swiper-slide>
  <swiper-slide>{% include figure.liquid loading="eager" path="assets/img/nmcs/nmcs_station1.jpeg" class="img-fluid rounded z-depth-1" zoomable=true %}</swiper-slide>
  <swiper-slide>{% include figure.liquid loading="eager" path="assets/img/nmcs/nmcs_station2.jpeg" class="img-fluid rounded z-depth-1" zoomable=true %}</swiper-slide>
  <swiper-slide>{% include figure.liquid loading="eager" path="assets/img/nmcs/raspi_cablesalad.jpeg" class="img-fluid rounded z-depth-1" zoomable=true %}</swiper-slide>
  <swiper-slide>{% include figure.liquid loading="eager" path="assets/img/nmcs/raspi.jpeg" class="img-fluid rounded z-depth-1" zoomable=true %}</swiper-slide>
  <swiper-slide>{% include figure.liquid loading="eager" path="assets/img/nmcs/toilet.jpeg" class="img-fluid rounded z-depth-1" zoomable=true %}</swiper-slide>
  <swiper-slide>{% include figure.liquid loading="eager" path="assets/img/nmcs/toiletSetup.jpeg" class="img-fluid rounded z-depth-1" zoomable=true %}</swiper-slide>
  <swiper-slide>{% include figure.liquid loading="eager" path="assets/img/nmcs/pylons.jpeg" class="img-fluid rounded z-depth-1" zoomable=true %}</swiper-slide>
 
  </swiper-container>
<div class="caption">
    Gallery Images
</div>
