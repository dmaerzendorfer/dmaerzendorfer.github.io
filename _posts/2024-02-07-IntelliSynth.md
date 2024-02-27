---
layout: post
title: "IntelliSynth"
date: 2024-02-07
excerpt: "My Bachelors Thesis."
tags: [bachelor, midi, piano, raspi, ai, musicautobot, python]
project: true
feature: #assets/img/intellisynth/experimentalSetup.png
comments: false
---

IntelliSynth was the Bachelors Thesis of my ITS Bachelor at the University of Applied Science in Salzburg.

IntelliSynth is a interactive Musician powered by AI. This means a human is able to play and compose music together with an AI.

The concept is the following: 
* a human is sitting at a piano and playing a few notes
* after a while the AI (that has been recording the notes) takes over and continues the music
* after a while the human takes over again
* rinse and repeat

<figure>
	<a href="{{site.url}}/assets/img/intellisynth/interactiveMusician.png"><img src="{{site.url}}/assets/img/intellisynth/interactiveMusician.png"></a>
	<figcaption style ="text-align:center"><a href="{{site.url}}/assets/img/intellisynth/interactiveMusician.png" title="How the interactive Musician works.">How the interactive Musician works.</a>.</figcaption>
</figure>

## Technical Details

The core components of the IntelliSynth are a **e-piano** a **linux PC with IntelliSynth and musicautobot** and a **Raspberry Pi Zynthian**. IntelliSynth itself is written in python.

The <a href="https://musicautobot.com/">musicautobot</a> is an already trained transformer AI model for musical MIDI data. It is able to continue music if feed in a MIDI syntax.   
The <a href="https://zynthian.org/">Zynthian</a> is a Synthesizer that runs on a Raspberry Pi. It is able to synthesise any MIDI-Data to piano sounds.

<figure>
	<a href="{{site.url}}/assets/img/intellisynth/conceptDrawing.png"><img src="{{site.url}}/assets/img/intellisynth/conceptDrawing.png"></a>
	<a href="{{site.url}}/assets/img/intellisynth/experimentalSetup.png"><img src="{{site.url}}/assets/img/intellisynth/experimentalSetup.png"></a>
	<figcaption style ="text-align:center">
	<a href="{{site.url}}/assets/img/intellisynth/conceptDrawing.png" title="The IntelliSynth Setup.">The IntelliSynth Setup.</a>.</figcaption>
</figure>


## Creation Story

In my Bachelor course it is customary to have two Bachelor Theses. The first one is created in a team of two and the second one is created alone.

IntelliSynth was the topic for both my Theses. The first Thesis was created in collaboration with Florian Hinterberger and consisted of creating the first prototype of the setup.

The division of labour here was that I covered the implementation of the usage of the already existing musicautobot model and the output over the Zynthian whilst florian was handling the MIDI interface and file format.

At the end of the first Thesis we noticed a flaw in it: The prediction of the musicautobot is not in real-time. Whilst the model is creating a prediction, one has to wait for it to finish. This hurts the process of creating music together.

<figure>
	<a href="{{site.url}}/assets/img/intellisynth/konzept1.png"><img src="{{site.url}}/assets/img/intellisynth/konzept1.png"></a>
	<figcaption style ="text-align:center"><a href="{{site.url}}/assets/img/intellisynth/konzept1.png" title="The problem with the prediction.">The problem with the prediction.</a>.</figcaption>
</figure>

The topic of my second Thesis was to get rid of this waiting time.  
This was achieved with the help of semaphores and a pipe. The prediction now starts in its own process whilst the user is still playing. The users last few inputs are no longer used for the prediction and are just a buffer-time for the prediction to kick in. The user does not notice anything about the prediction time.

<figure>
	<a href="{{site.url}}/assets/img/intellisynth/solutionKonzept.png"><img src="{{site.url}}/assets/img/intellisynth/solutionKonzept.png"></a>
	<figcaption style ="text-align:center"><a href="{{site.url}}/assets/img/intellisynth/solutionKonzept.png" title="The realtime optimisation.">The realtime optimisation.</a>.</figcaption>
</figure>

### Repo
<a href="https://github.com/dmaerzendorfer/IntelliSynth">https://github.com/dmaerzendorfer/IntelliSynth</a>

