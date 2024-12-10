---
layout: page
title: IntelliSynth
description: My Bachelor Thesis.
img: assets/img/intellisynth/experimentalSetup.png
importance: 1
# category: work
related_publications: false
images:
  slider: true
toc:
  sidebar: left
related_posts: false
---

## Intro

IntelliSynth was the bachelors thesis of my ITS Bachelor at the University of Applied Science in Salzburg.

IntelliSynth is a interactive Musician powered by AI. This means a human is able to play and compose music together with an AI.

The concept is the following: 
* a human is sitting at a piano and playing a few notes
* after a while the AI (that has been recording the notes) takes over and continues the music
* after a while the human takes over again
* rinse and repeat

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/intellisynth/interactiveMusician.png" title="example image" class="img-fluid rounded z-depth-1" zoomable=true %}
    </div>
</div>
<div class="caption">
    How the interactive Musician works.
</div>

---

## Technical Details

The core components of the IntelliSynth are a **e-piano** a **linux PC with IntelliSynth and musicautobot** and a **Raspberry Pi Zynthian**. IntelliSynth itself is written in python.

The <a href="https://musicautobot.com/">musicautobot</a> is an already trained transformer AI model for musical MIDI data. It is able to continue music if feed in a MIDI syntax.   
The <a href="https://zynthian.org/">Zynthian</a> is a Synthesizer that runs on a Raspberry Pi. It is able to synthesise any MIDI-Data to piano sounds.

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/intellisynth/conceptDrawing.png" title="example image" class="img-fluid rounded z-depth-1" zoomable=true %}
        {% include figure.liquid loading="eager" path="assets/img/intellisynth/experimentalSetup.png" title="example image" class="img-fluid rounded z-depth-1" zoomable=true %}
    </div>
</div>
<div class="caption">
    The IntelliSynth Setup.
</div>

---

## Creation Story

In my bachelor course it is customary to have two bachelor theses. The first one is written in a team of two and the second one is written alone.

IntelliSynth was the topic for both my Theses. The first thesis was written in collaboration with Florian Hinterberger and consisted of creating the first prototype of the setup.

The division of labour here was that I covered the implementation of the usage of the already existing musicautobot model and the output over the Zynthian whilst florian was handling the MIDI interface and file format.

At the end of the first Thesis we noticed a flaw in it: The prediction of the musicautobot is not in real-time. Whilst the model is creating a prediction, one has to wait for it to finish. This hurts the process of creating music together.

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/intellisynth/konzept1.png" title="example image" class="img-fluid rounded z-depth-1" zoomable=true %}
    </div>
</div>
<div class="caption">
    The problem with the prediction.
</div>


The topic of my second thesis was to get rid of this waiting time.  
This was achieved with the help of semaphores and a pipe. The prediction now starts in its own process whilst the user is still playing. The users last few inputs are no longer used for the prediction and are just a buffer-time for the prediction to kick in. The user does not notice anything about the prediction time.

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/intellisynth/solutionKonzept.png" title="example image" class="img-fluid rounded z-depth-1" zoomable=true %}
    </div>
</div>
<div class="caption">The realtime optimisation.
</div>

---

## Repo
<a href="https://github.com/dmaerzendorfer/IntelliSynth">https://github.com/dmaerzendorfer/IntelliSynth</a>

