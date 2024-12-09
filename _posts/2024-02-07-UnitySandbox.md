---
layout: post
title: Unity Sandbox
date: 2024-02-07 12:00:00
description: A collection of bits and bobs that I have created in Unity
tags: Unity Sandbox
categories: Unity
thumbnail: https://www.miracle-recreation.com/content/uploads/pim/1140/1140.jpg
images:
  slider: true
toc:
  sidebar: left
related_posts: false
---

## Intro

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

---

## Repo

<a href="https://github.com/dmaerzendorfer/UnitySandbox">https://github.com/dmaerzendorfer/UnitySandbox</a>

---

## Gallery

<swiper-container keyboard="true" navigation="true" pagination="true" pagination-clickable="true" pagination-dynamic-bullets="true" rewind="true">
  <swiper-slide>{% include figure.liquid loading="eager" path="assets/img/unitySandbox/fakeLiquid.png" class="img-fluid rounded z-depth-1" %}</swiper-slide>
  <swiper-slide>{% include figure.liquid loading="eager" path="assets/img/unitySandbox/healthBars.png" class="img-fluid rounded z-depth-1" %}</swiper-slide>
  <swiper-slide>{% include figure.liquid loading="eager" path="assets/img/unitySandbox/lobbySystem.png" class="img-fluid rounded z-depth-1" %}</swiper-slide>
  <swiper-slide>{% include figure.liquid loading="eager" path="assets/img/unitySandbox/smileyGif.gif" class="img-fluid rounded z-depth-1" %}</swiper-slide>
  <swiper-slide>{% include figure.liquid loading="eager" path="assets/img/unitySandbox/BreathingWizardLady.gif" class="img-fluid rounded z-depth-1" %}</swiper-slide>
  <swiper-slide>{% include figure.liquid loading="eager" path="assets/img/unitySandbox/ShatterDemo.gif" class="img-fluid rounded z-depth-1" %}</swiper-slide>
  <swiper-slide>{% include figure.liquid loading="eager" path="assets/img/unitySandbox/ColourShifter.gif" class="img-fluid rounded z-depth-1" %}</swiper-slide>
  <swiper-slide>{% include figure.liquid loading="eager" path="assets/img/unitySandbox/vanishBoy.gif" class="img-fluid rounded z-depth-1" %}</swiper-slide>
  <swiper-slide>{% include figure.liquid loading="eager" path="assets/img/unitySandbox/spline.gif" class="img-fluid rounded z-depth-1" %}</swiper-slide>
</swiper-container>