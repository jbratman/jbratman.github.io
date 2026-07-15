---
layout: project-case-study
title: "ECE/MAE 148 Autonomous Vehicle"
subtitle: "A perception-driven robotic vehicle for person tracking and visual identification"
date: 2024-12-06
collection: portfolio
permalink: /final_project/

project_type: "Robotics · Autonomous Systems"
hero_image: /images/148_final_project/complete_car.JPG
hero_summary: >-
  Integrated perception, decision logic, vehicle control, mechanical packaging,
  and human-facing feedback into a real-time autonomous ground vehicle.

intro_title: "A team autonomy project built around real-time perception and state-based behavior"
intro: >-
  The vehicle detected and followed a person, evaluated ArUco identification
  markers, and changed behavior based on valid or invalid visual cues. My role
  centered on system architecture, control logic, mechanical layout, and integration.

role: "System Integration and Autonomy Lead"
timeline: "Fall 2024"
team: "ECE/MAE 148 Team 7"
organization: "UC San Diego"
status: "Completed"

tools:
  - ROS2
  - Python
  - C++
  - OAK-D Lite
  - DepthAI
  - Arduino

skills:
  - System Architecture
  - Perception Integration
  - State Machines
  - Mechanical Packaging

process:
  - title: "Behavior Definition"
    detail: "Defined detection, tracking, identification, and response states."
  - title: "Architecture"
    detail: "Separated perception, decision, control, feedback, and actuation interfaces."
  - title: "Mechanical Layout"
    detail: "Packaged sensors, compute, electronics, and mounting hardware."
  - title: "Integration"
    detail: "Connected person detection and ArUco outputs to vehicle behaviors."
  - title: "Debugging"
    detail: "Resolved timing, interface, and real-time control issues."
  - title: "Demonstration"
    detail: "Validated person following, marker response, and status feedback."

results:
  - value: "≈6 m"
    label: "Person-detection and tracking range"
  - value: "RGB + Depth"
    label: "Perception inputs"
  - value: "4X4_50"
    label: "ArUco marker dictionary"
  - value: "State Based"
    label: "Autonomy behavior architecture"
  - value: "LCD"
    label: "Human-readable status feedback"
  - value: "Functional"
    label: "Integrated final demonstration"

featured: true
order: 5
card_title: "ECE/MAE 148 Autonomous Vehicle"
card_category: "Autonomous Systems"
card_image: /images/148_final_project/complete_car.JPG
card_summary: >-
  Integrated an autonomous vehicle using ROS2, perception, and embedded systems.
card_tags:
  - ROS2
  - Robotics
  - Integration
  - Controls

previous_project:
  title: "1/10th-Scale Autonomous Racecar"
  url: /racecar/
next_project:
  title: "Aero-Structural Analysis"
  url: /aerodynamic_analysis/
---

## The Challenge

The vehicle needed to patrol, detect a person, follow that person, evaluate a visual identification marker, and execute different motion responses based on whether the marker was valid.

The system operated under:

- limited onboard compute
- perception noise
- sensor latency
- real-time control requirements
- independently developed team subsystems
- physical packaging constraints

The project required perception, autonomy, controls, embedded feedback, and mechanical hardware to operate as one integrated system.

## System Behavior

The OAK-D Lite camera provided RGB and depth data for person detection and tracking.

When an ArUco marker was presented:

- a valid marker triggered a green status indication
- the vehicle stopped
- the vehicle reversed
- the vehicle executed a U-turn
- the vehicle resumed autonomous search behavior

An invalid marker triggered a red status indication and the vehicle continued following the person.

<div class="engineering-decision">
  <p class="engineering-decision__label">Engineering Decision</p>
  <p><strong>Use explicit state-based behavior rather than tightly coupled conditional control.</strong></p>
  <p>This made perception outputs, motion commands, and behavior transitions easier to debug independently.</p>
</div>

## System Architecture

The architecture separated:

- person detection
- depth-based tracking
- ArUco marker detection
- behavior state
- vehicle motion control
- LCD feedback
- mechanical and electrical hardware

This allowed team members to develop perception components independently while maintaining defined interfaces for integration.

## Mechanical Integration

I served as the primary CAD designer and packaged:

- OAK-D Lite camera
- compute hardware
- control electronics
- Arduino and LCD hardware
- structural mounts
- vehicle interfaces

Mechanical layout had to preserve camera visibility, protect electronics, and remain accessible for debugging.

## Integration and Debugging

I coordinated the interfaces between perception, autonomy, and actuation code.

System-level testing focused on:

- perception timing
- behavior transitions
- steering and throttle response
- valid versus invalid marker handling
- communication between software and embedded feedback
- consistency across repeated demonstrations

## My Contributions

- designed the high-level system architecture
- implemented vehicle control and drive logic
- developed state-based autonomy behavior
- integrated person detection and ArUco detection
- served as primary CAD designer
- packaged sensors and compute hardware
- coordinated subsystem interfaces
- led system debugging and final integration
- supported planning and technical decisions

## Results

The final system demonstrated:

- real-time person detection and tracking
- tracking distances up to approximately 6 meters
- marker detection using the `DICT_4X4_50` dictionary
- state-based motion responses
- dynamic steering and speed adjustment
- LCD status feedback
- successful integrated final behavior

## Stretch Goals

GPS waypoint navigation and enhanced obstacle avoidance were considered as future extensions. They were not fully implemented because of project scope, integration complexity, and schedule constraints.

## Lessons Learned

The project reinforced the importance of clearly defined subsystem interfaces. Integration became much easier when perception, decision logic, motion control, and feedback were treated as separate modules with explicit inputs and outputs.
