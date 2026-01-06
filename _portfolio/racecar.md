---
title: "1/10th Scale Autonomous Racecar Updates"
date: 25-08-20
collection: portfolio
tags: [ROS2, CAD, Python, Embedded]
excerpt: |
  **Overview**
  - **System:** 1/10th-scale autonomous racecar hardware integration and sensor packaging update
  - **Role:** Mechanical design lead for sensor mounting, chassis integration, and serviceability improvements
  - **Tools:** CAD, 3D printing, ROS2-compatible sensors, rapid prototyping
  - **Outcome:** Improved sensor placement, durability, and serviceability while transitioning the vehicle from a research robot to an autonomous racecar form factor 

header:
  teaser: 1_10th_racecar/01_Jack_Robot_v6.jpg
---

## Overview
- **System:** 1/10th-scale autonomous racecar hardware integration and sensor packaging update
- **Role:** Mechanical design lead for sensor mounting, chassis integration, and serviceability improvements
- **Tools:** CAD, 3D printing, ROS2-compatible sensors, rapid prototyping
- **Outcome:** Improved sensor placement, durability, and serviceability while transitioning the vehicle from a research robot to an autonomous racecar form factor


## Problem & Constraints
- Utilize current sensor package on vehicle
- Integrate secondary Livox Mid-360 lidar into front area of vehicle
- Maintain top lidar and GPS antenna position
- Change appearance from robot to autonomous vehicle
- Maintain strength and endurance from impacts
- Improve serviceability  

## Build, Test, Iterate
This work focused on repackaging sensors and compute hardware to transition the vehicle from a research-oriented robotic platform into an autonomous racecar that could accept standard RC car bodies. Design changes prioritized compact packaging, durability, and serviceability while preserving sensor performance and enabling realistic racecar aesthetics.

## My Contributions
I led the mechanical redesign and hardware repackaging effort to transition the platform from a research-oriented robotic vehicle into an autonomous racecar capable of accepting standard RC car bodies.

My contributions included:
- Served as the primary CAD designer for sensor mounts, compute packaging, and chassis integration
- Repackaged perception and compute hardware to reduce external protrusions and improve form factor
- Enabled compatibility with off-the-shelf RC car bodies while preserving sensor fields of view
- Designed mounts to improve durability and serviceability under racing conditions
- Supported system integration and testing to validate mechanical robustness and repeatability

## Key Results
- Successfully transitioned the platform from a research-oriented robotic vehicle to an autonomous racecar capable of accepting standard RC car bodies
- Improved packaging and reduced external protrusions, enabling realistic vehicle aesthetics and improved protection of sensors and compute hardware
- Maintained sensor performance and field-of-view while integrating components within a constrained chassis envelope
- Improved durability and serviceability, reducing setup and repair time between testing sessions
- Enabled future aerodynamic and body-fit experimentation by standardizing mounting locations and form factor

<div style="margin-bottom: 0px; font-size: 1.2em;">
  Initial Starting Point:
</div>
<div style="display: flex; align-items: center; gap: 10px;">
  <figure style="flex:1; text-align:center;">
    <img src="/images/1_10th_racecar/20250814_111441.jpg" alt="Original" style="width:100%;height:250px; object-fit:cover;">
    <figcaption>Original hardware location</figcaption>
  </figure>
  <figure style="flex:1; text-align:left;">
    <img src="/images/1_10th_racecar/00_Jack_Robot_modified_hole_size_v4.jpg" alt="Modified" style="width:100%;height:250px; object-fit:cover;">
    <figcaption>Initial modified CAD design</figcaption>
  </figure>
</div>


<div style="margin-bottom: 0px; font-size: 1.2em;">
Chassis Tear Down and Initial Plan:
</div>
<div style="display: flex; align-items: center; gap: 10px;">
  <figure style="flex:1; text-align:center;">
    <img src="/images/1_10th_racecar/20250818_193222.jpg" alt="Original" style="width:100%;height:250px; object-fit:cover;">
    <figcaption>Front lidar mount iterations</figcaption>
  </figure>
  <figure style="flex:1; text-align:center;">
    <img src="/images/1_10th_racecar/20250814_183841.jpg" alt="Modified" style="width:100%;height:250px; object-fit:cover;">
    <figcaption>Front lidar mounting position</figcaption>
  </figure>
</div>

<div style="margin-bottom: 0px; font-size: 1.2em;">
Installation of Front Lidar:
</div>
<div style="display: flex; align-items: center; gap: 10px;">
  <figure style="flex:1; text-align:center;">
    <img src="/images/1_10th_racecar/20250814_115533.jpg" alt="Original" style="width:100%;height:250px; object-fit:cover;">
    <figcaption>Initial body shell, with previous design cut outs</figcaption>
  </figure>
  <figure style="flex:1; text-align:center;">
    <img src="/images/1_10th_racecar/20250815_121627.jpg" alt="Modified" style="width:100%;height:250px; object-fit:cover;">
    <figcaption>Cut template allows repeatable lidar install</figcaption>
  </figure>
    <figure style="flex:1; text-align:center;">
    <img src="/images/1_10th_racecar/20250815_124622.jpg" alt="Modified" style="width:100%;height:250px; object-fit:cover;">
    <figcaption>Front lidar and camera mounted</figcaption>
  </figure>
</div>

<div style="margin-bottom: 0px; font-size: 1.2em;">
Installation of Body Shell and Completed Design:
</div>
<div style="display: flex; align-items: center; gap: 10px;">
  <figure style="flex:1; text-align:center;">
    <img src="/images/1_10th_racecar/20250818_193410.jpg" alt="Original" style="width:100%;height:250px; object-fit:cover;">
    <figcaption>Final mounts 3D printed</figcaption>
  </figure>
    <figure style="flex:1; text-align:center;">
    <img src="/images/1_10th_racecar/20250818_193522.jpg" alt="Modified" style="width:100%;height:250px; object-fit:cover;">
    <figcaption>New mounts test fit before body shell modified </figcaption>
  </figure>
    <figure style="flex:1; text-align:center;">
    <img src="/images/1_10th_racecar/01_Jack_Robot_v6.jpg" alt="Modified" style="width:100%;height:250px; object-fit:cover;">
    <figcaption>Final CAD design with all componets place </figcaption>
  </figure>
</div>

## Summary of Work
- Considered initial design constraints,and was presented the current state of development. Weaknesses of the current design and strengths.
- Realized that initial CAD model did not meet design requirements.
- Tested idea of moving front lidar infront of front suspension system
- Developed cut template for modifying body shell, so that new shells could be easily updated
- Updated component mounts to centeralize in order to minimize risk of damage in side collision 