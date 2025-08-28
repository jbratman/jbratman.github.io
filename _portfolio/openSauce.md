---
title: "OpenSauce 2025"
date: 2025-07-19
collection: portfolio
tags: [ROS2, CAD, Python, Embedded]
header:
  teaser: openSauce/AWS_Chassis_Electrical_Mounting_Plate.jpg
---

## Overview
Built an autonomous racecar demo for OpenSauce so attendees could experience self-driving racing tech.

## Design Constraints
- Develop a sub 500$ autonomous racecar
- Utilize Raspberry Pi 5 and Global Shutter Pi camera
- Needs to be compact enough to fit in 16'x 16' area and travel via plane
- Easily Servicable as to minimize downtime for demo 
- Be able to show how the AI model was being implemented

## Development

### Initial Starting Point
<p class="section-sub">
  Chassis was determined to meet the size requirements. This chassis also had all the components needed to run, with minor modifications: changing the ESC connector to an XT60 and relocating the ESC to allow for a bigger battery.
</p>

<div class="row">
  <figure class="col">
    <img src="/images/openSauce/20250709_140232.jpg" alt="Original">
    <figcaption>Chassis that was found to meet requirements</figcaption>
  </figure>
</div>

### CAD Development
<p class="section-sub">
  With the chassis determined, the next goal was to take the hard mounting points of the aluminum frame and translate them into CAD in order to have a base for the modular mounting system for the Raspberry Pi 5, camera mount, and PWM servo motor driver.
</p>

<div class="row">
  <figure class="col">
    <img src="/images/openSauce/AWS_Chassis_Electrical_Mounting_Plate_v20.png" alt="CAD">
    <figcaption>CAD design with mounting solutions</figcaption>
  </figure>
</div>

### CAD Development (Assembly)
<p class="section-sub">
  The car was then fully assembled and used to demo for attendees.
</p>

<div class="row">
  <figure class="col"><img src="/images/openSauce/mini_white1.jpg" alt=""></figure>
  <figure class="col"><img src="/images/openSauce/mini_white2.jpg" alt=""></figure>
  <figure class="col"><img src="/images/openSauce/mini_white3.jpg" alt=""></figure>
</div>

## Demo at Show

### Initial Slow Autonomous Lap
<div class="video-wrapper">
  <iframe
    src="https://www.youtube.com/embed/h1-yFdrnhTQ?autoplay=1&mute=1&loop=1&playlist=h1-yFdrnhTQ"
    title="Initial slow autonomous lap"
    frameborder="0"
    allow="autoplay; encrypted-media; gyroscope; picture-in-picture"
    allowfullscreen>
  </iframe>
</div>

### Final Fast Autonomous Lap
<div class="video-wrapper">
  <iframe
    src="https://www.youtube.com/embed/Mi3047i9aY0?autoplay=1&mute=1&loop=1&playlist=Mi3047i9aY0"
    title="Final fast autonomous lap"
    frameborder="0"
    allow="autoplay; encrypted-media; gyroscope; picture-in-picture"
    allowfullscreen>
  </iframe>
</div>

## Summary of Work
- Developed a low cost entery level autonomous racecar, utilizing used chassis, Rasberry Pi 5, Global Shutter Pi cam, and PMW servo motor driver.
- Successfully built a working AI model to drive around track enough to take attendee's data and build on top, in order to showcase how they trained the AI to drive. 
- Maintained cost contraints, retained serviceability, and durability with CAD design.
- Conformed to small form factor restrictions. 
