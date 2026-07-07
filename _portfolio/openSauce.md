---
title: "OpenSauce 2025"
date: 2025-07-19
collection: portfolio
tags: [ROS2, CAD, Python, Embedded]

excerpt: |
  **Overview**
  - **System:** Low-cost autonomous RC racecar developed for live demonstration at OpenSauce 2025
  - **Role:** Primary system integrator responsible for CAD design, hardware integration, autonomy setup, and on-site demonstration
  - **Tools:** ROS2, Python, CAD, Raspberry Pi 5, global shutter camera, embedded motor control
  - **Outcome:** Delivered a reliable autonomous racecar demonstration that continuously operated for attendees throughout OpenSauce 2025

header:
  teaser: openSauce/AWS_Chassis_Electrical_Mounting_Plate.jpg

featured: true
order: 3

card_category: "Public Demonstration"

card_image: /images/openSauce/AWS_Chassis_Electrical_Mounting_Plate.jpg

card_summary: >
  Designed, built, and demonstrated a live autonomous RC racecar demonstration at OpenSauce 2025.

card_tags:
  - Robotics
  - ROS2
  - Embedded
  - Public Demo
---

## Overview
- **System:** Low-cost autonomous RC racecar developed for live demonstration at OpenSauce 2025
- **Role:** Primary system integrator responsible for CAD design, hardware integration, autonomy setup, and on-site demo execution
- **Tools:** ROS2, Python, CAD, Raspberry Pi 5, global shutter camera, embedded motor control
- **Outcome:** Delivered a reliable, repeatable autonomous racecar demo that operated live on the show floor and engaged attendees in hands-on autonomy concepts

## Problem & Constraints
- Develop a sub-$500 autonomous racecar platform
- Utilize Raspberry Pi 5 and a global shutter camera
- Fit within a 16 ft × 16 ft demo area and be transportable by air
- Maintain high serviceability to minimize demo downtime
- Visually demonstrate how an AI model was implemented and trained


## Build, Test, Iterate
This project followed an iterative build–test–refine workflow to ensure the system was reliable, serviceable, and repeatable for a live public demonstration environment. Design decisions prioritized robustness, rapid troubleshooting, and consistent autonomous behavior over maximum performance.

## My Contributions
I served as the primary integrator for the OpenSauce 2025 autonomous racecar demo, responsible for bringing together hardware, software, and mechanical design into a reliable live demonstration system.

My contributions included:
- Designed and maintained the overall system architecture for the autonomous demo
- Served as the primary CAD designer for the chassis layout, sensor mounts, and hardware packaging
- Integrated perception, control, and actuation into a single ROS2-based autonomy stack
- Implemented the primary vehicle control and autonomy logic used during the live demo
- Led system-level debugging, validation, and iteration to ensure consistent operation on the show floor
- Executed on-site setup, troubleshooting, and live operation during the OpenSauce event

## Key Results
- Successfully delivered a fully autonomous RC racecar demo operating live on the OpenSauce 2025 show floor
- Demonstrated repeatable autonomous driving behavior within a constrained 16 ft × 16 ft demo area
- Achieved reliable perception and control using a Raspberry Pi 5 and global shutter camera under variable lighting conditions
- Maintained high system uptime through rapid on-site troubleshooting and serviceable hardware design
- Effectively communicated autonomy concepts to attendees through visible sensing, control, and behavior execution

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
