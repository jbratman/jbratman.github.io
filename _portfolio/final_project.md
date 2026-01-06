---
title: "ECE/MAE 148 Final Project (Team 7)"
date: 2024-12-06
collection: portfolio
tags: [Autonomy, Robotics, Controls, Perception, Systems]
excerpt: |
  **Overview**
  - **System:** Team-based autonomous systems project developed for ECEMAE 148
  - **Role:** Team member contributing to system integration, implementation, and testing
  - **Tools:** ROS2, Python, C++, Git, embedded sensors and compute hardware
  - **Outcome:** Demonstrated a functional autonomous system with documented architecture, testing results, and final presentation

header:
  teaser: 148_final_project/complete_car.JPG
---

## Overview
- **System:** Team-based autonomous systems project developed for ECEMAE 148
- **Role:** Team member contributing to system integration, implementation, and testing
- **Tools:** ROS2, Python, C++, Git, embedded sensors and compute hardware
- **Outcome:** Demonstrated a functional autonomous system with documented architecture, testing results, and final presentation

## Problem Statement
The objective of this project was to design and demonstrate an autonomous robotic system capable of detecting, tracking, and interacting with humans using onboard perception and decision logic. The system needed to reliably identify people, respond to visual identification cues, and execute distinct behaviors based on validated versus invalid inputs, all in real time.

The project emphasized perception-driven autonomy, sensor fusion, and state-based decision making under real-world constraints such as limited compute, sensor noise, and system latency.

## Project Goals & Scope

The primary objective of the project was to develop an autonomous robotic vehicle capable of patrolling a defined area, detecting a person, and interacting based on visual identification cues. Upon recognizing a valid ArUco marker, the system was designed to disengage from the individual and resume autonomous search behavior.

In addition to the core functionality, several stretch goals were identified to extend system capability beyond the minimum requirements:
- **GPS-based navigation:** Enabling the vehicle to follow predefined routes with waypoint-level precision
- **Enhanced object avoidance:** Integrating additional sensing (camera or LiDAR) to improve navigation safety in dynamic environments

These stretch goals were explored at a conceptual level but were not fully implemented due to time, integration complexity, and project scope constraints.

## System Overview

This project utilized the DepthAI Toolbox within a robotic vehicle framework to detect and follow a person until a visual identification cue was presented using an ArUco marker.

The system continuously tracked a detected individual using RGB and depth data. When an ArUco marker was presented, the system evaluated its validity and executed a corresponding response:
- **Valid marker:** Green indicator displayed, vehicle halted, reversed, and executed a U-turn before resuming search behavior.
- **Invalid marker:** Red indicator displayed, vehicle continued following the individual until a valid marker was detected.

Visual feedback was provided via an Arduino-controlled LCD to clearly communicate system state and detection status.

## My Contributions

While this was a team-based project, I was primarily responsible for overall system integration, autonomy behavior design, and mechanical layout, serving as the main point of integration across software and hardware subsystems.

My contributions included:
- Designed the high-level system architecture and state-based autonomy logic
- Implemented the primary vehicle control and drive logic, including behavior transitions and motion responses
- Integrated perception outputs (person detection and ArUco marker detection) into a unified decision-making pipeline
- Served as the primary CAD designer, responsible for mechanical layout, sensor mounting, and hardware packaging
- Coordinated subsystem interfaces between perception, autonomy, and actuation code developed by team members
- Led system-level debugging, testing, and integration to ensure reliable real-time operation
- Contributed to project planning, task breakdown, and technical decision-making throughout development

This role required balancing system-level behavior, real-time constraints, and mechanical integration challenges while enabling team members to develop and validate individual perception components independently.

## Key Results

- Successfully detected ArUco markers from the `DICT_4X4_50` dictionary using an OAK-D Lite camera and the DepthAI Toolbox
- Implemented real-time person detection and tracking up to approximately 6 meters using RGB and depth data
- Enabled dynamic vehicle control by adjusting speed and steering in response to human motion
- Implemented state-based behavior transitions in response to valid and invalid identification markers
- Integrated visual status feedback via an LCD interface to indicate system state and detection outcomes

