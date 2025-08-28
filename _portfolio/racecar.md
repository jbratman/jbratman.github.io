---
title: "1/10th Scale Autonomous Racecar Updates"
date: 2025-08-20
collection: portfolio
tags: [ROS2, CAD, Python, Embedded]
header:
  teaser: 1_10th_racecar/01_Jack_Robot_v6.jpg
---

## Overview
This project focused on developing modular sensor mounts and integration of body shell for a 1/10th-scale autonomous racecar.  
The system was designed to be adaptable across vehicle setups while reducing downtime during testing.

## Features
- Designed modular CAD + 3D-printed sensor mounts
- Improved serviceability and reduced downtime during races

## Design Constraints
- Utilize current sensor package on vehicle
- Integrate secondary Livox Mid-360 lidar into front area of vehicle
- Maintain top lidar and GPS antenna position
- Change appearance from robot to autonomous vehicle
- Maintain strength and endurance from impacts
- Improve serviceability  

## Development
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