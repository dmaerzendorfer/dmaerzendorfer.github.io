---
layout: post
title: "Unity Sandbox"
date: 2024-02-07
excerpt: "A collection of bits and bobs that I have created in Unity"
tags: [unity, sandbox]
# project: false
feature: https://www.miracle-recreation.com/content/uploads/pim/1140/1140.jpg
tiled_bg: false   # Set this true if you want to tile your background image, otherwise it will be covered
comments: false
---

At some point I was bored and I wanted to learn and try out some things. Thats when this sandbox was created. 

My UnitySandbox is just a repo with a Unity Project in which I implement and try random things. The original thought was also to have some useful components lying around that could be used in a game jam for example.

A few toys that are currently lying around in the sandbox are:

* A Spline Tool
* A Healthbar Component
* A third person player controller with a hierarchical state machine
	* This also includes a lobby card system for four-player local coop gameplay
* A menu template including options with transition screens and a level-loader
* A generic score system
* A fake liquid shader
* A test implementation of VFX using the Skinned Mesh Renderer's Vertex Positions.
* A system for changing color palettes. In addition I tested out some things with pixelization filters. 
* A simple AudioManager. For the usage in GameJams where it is not worth it to integrate fmod or wwise.
* A little experiment with cutting and shattering meshes during runtime.
* A little 2.5D scene
* A procedural 2d face with googly eyes!
	* I found a nice package which does everything, I mereley fixed some bugs. (https://forum.unity.com/threads/procedural-eyes.454758/)
* A base version of a 2D ragdoll character that I used in my game Foetality.
* A simple AudioManager for Unity-AudioSources, specifically for the usage in GameJams where the requirements are low.
### Repo
<a href="https://github.com/dmaerzendorfer/UnitySandbox">https://github.com/dmaerzendorfer/UnitySandbox</a>

### Gallery
<!-- <video width="560" height="315" controls>
  <source src="{{site.url}}/assets/img/sandbox/DancingVanishBoy.mp4" type="video/mp4">
Your browser does not support the video tag.
</video> -->
![Splines going Round]({{site.url}}/assets/img/sandbox/spline.gif)
![Silly Dance vanish boy]({{site.url}}/assets/img/sandbox/vanishBoy.gif)
![Mage boi changing colors]({{site.url}}/assets/img/sandbox/ColourShifter.gif)
![Sphere getting shattered]({{site.url}}/assets/img/sandbox/ShatterDemo.gif)
![Breathing 2.5D lady in a forest]({{site.url}}/assets/img/sandbox/BreathingWizardLady.gif)
![A procedural face]({{site.url}}/assets/img/sandbox/smileyGif.gif)


{% capture images %}
	{{site.url}}/assets/img/sandbox/fakeLiquid.png
	{{site.url}}/assets/img/sandbox/healthBars.png
	{{site.url}}/assets/img/sandbox/lobbySystem.png
{% endcapture %}
{% include gallery images=images caption="Sandbox Images" cols=2 %}


