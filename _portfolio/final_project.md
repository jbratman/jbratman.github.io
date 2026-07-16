---
layout: project-case-study
title: "ECE/MAE 148 Autonomous Vehicle"
subtitle: "A perception-driven robotic vehicle for person tracking and visual identification"
date: 2024-12-06
collection: portfolio
permalink: /final_project/

project_type: "Robotics · Autonomous Systems"
hero_image: /images/148_final_project/complete_car.JPG
hero_mobile_position: "center 42%"
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
  - Jetson Nano
  - OAK-D Lite
  - DepthAI
  - Arduino

skills:
  - System Architecture
  - Perception Integration
  - State Machines
  - Mechanical Packaging

process_heading: "From behavior requirements to an integrated autonomous vehicle"

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

results_heading: "Validated through system integration and demonstration"

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

The vehicle used explicit states to separate search, person following, marker evaluation, and response behaviors. This made transitions observable and allowed perception and motion logic to be tested independently.

<div class="system-flow" aria-label="Autonomous vehicle behavior sequence">
  <div class="system-flow__step">
    <span class="system-flow__number">01</span>
    <strong>Search</strong>
    <span>Patrol the operating area while waiting for a person detection.</span>
  </div>
  <div class="system-flow__arrow" aria-hidden="true">→</div>
  <div class="system-flow__step">
    <span class="system-flow__number">02</span>
    <strong>Detect</strong>
    <span>Identify a person and estimate their relative position using RGB and depth.</span>
  </div>
  <div class="system-flow__arrow" aria-hidden="true">→</div>
  <div class="system-flow__step">
    <span class="system-flow__number">03</span>
    <strong>Follow</strong>
    <span>Adjust steering and speed to track the detected person.</span>
  </div>
  <div class="system-flow__arrow" aria-hidden="true">→</div>
  <div class="system-flow__step">
    <span class="system-flow__number">04</span>
    <strong>Evaluate</strong>
    <span>Read the presented ArUco marker and select the next behavior.</span>
  </div>
  <div class="system-flow__arrow" aria-hidden="true">→</div>
  <div class="system-flow__step">
    <span class="system-flow__number">05</span>
    <strong>Respond</strong>
    <span>Execute the valid-marker maneuver or continue following after rejection.</span>
  </div>
</div>

The OAK-D Lite camera provided RGB and stereo-depth data for person detection, spatial tracking, and marker recognition.

When an ArUco marker was presented:

- a valid marker triggered a green status indication, stopped the vehicle, initiated a reverse and U-turn maneuver, and returned the system to autonomous search
- an invalid marker triggered a red status indication and the vehicle continued following the person
- the waiting state was displayed in blue before a marker decision was available

<div class="video-wrapper">
  <iframe
    src="https://www.youtube.com/embed/hA4WmpDeQwc?mute=1"
    title="LCD and ArUco marker verification test"
    allow="encrypted-media; gyroscope; picture-in-picture"
    allowfullscreen>
  </iframe>
</div>

*ArUco verification test showing the human-readable LCD feedback used for waiting, valid, and invalid marker states.*

<div class="engineering-decision">
  <p class="engineering-decision__label">Engineering Decision</p>
  <p><strong>Use explicit state-based behavior rather than tightly coupled conditional control.</strong></p>
  <p>This made perception outputs, motion commands, and behavior transitions easier to debug independently.</p>
</div>

## System Architecture

The software architecture separated perception, behavior selection, vehicle control, and embedded feedback through defined ROS2 and serial interfaces.

<div class="system-flow" aria-label="Autonomous vehicle system architecture">
  <div class="system-flow__step">
    <span class="system-flow__number">01</span>
    <strong>Perception</strong>
    <span>OAK-D RGB, stereo depth, MobileNet-SSD, and ArUco recognition.</span>
  </div>
  <div class="system-flow__arrow" aria-hidden="true">→</div>
  <div class="system-flow__step">
    <span class="system-flow__number">02</span>
    <strong>ROS2 Data</strong>
    <span>Person and marker information published through defined topics.</span>
  </div>
  <div class="system-flow__arrow" aria-hidden="true">→</div>
  <div class="system-flow__step">
    <span class="system-flow__number">03</span>
    <strong>Behavior</strong>
    <span>State logic selected search, follow, and marker-response modes.</span>
  </div>
  <div class="system-flow__arrow" aria-hidden="true">→</div>
  <div class="system-flow__step">
    <span class="system-flow__number">04</span>
    <strong>Control</strong>
    <span>Velocity commands adjusted vehicle steering and throttle.</span>
  </div>
  <div class="system-flow__arrow" aria-hidden="true">→</div>
  <div class="system-flow__step">
    <span class="system-flow__number">05</span>
    <strong>Feedback</strong>
    <span>Serial commands drove the Arduino-controlled LCD state.</span>
  </div>
</div>

The primary ROS2 interfaces included `/person_detection`, `/aruco_markers`, and `/cmd_vel`. The Arduino received `waiting`, `yes`, and `no` serial messages to update the LCD independently from the vehicle motion controller.

> **System-level implication:** Defined interfaces allowed perception, decision logic, vehicle control, and feedback to be developed separately while still providing observable signals for integration and debugging.

## Perception and Tracking

The DepthAI pipeline combined the OAK-D color camera, mono cameras, stereo-depth processing, and MobileNet-SSD spatial detection. This allowed the vehicle to identify a person, estimate their three-dimensional position, and adjust steering and speed using both image location and depth.

During testing, the integrated system detected and tracked people at distances up to approximately six meters. ArUco markers from the `DICT_4X4_50` dictionary provided the visual identification input used by the behavior state machine.

## Mechanical Integration

As the primary CAD designer, I developed the mounting system for:

- OAK-D Lite camera
- Jetson Nano and DC-DC converter
- combined camera and lidar hardware
- Arduino and LCD hardware
- main structural plate and vehicle interfaces

Mechanical layout had to preserve camera visibility, protect electronics, and remain accessible for debugging.

<div class="project-gallery__grid">
  <figure class="project-gallery__item">
    <img src="{{ '/images/148_final_project/IMG1-main_mounting_plate.png' | relative_url }}" alt="Main mounting plate CAD model">
    <figcaption><strong>Main Mounting Plate</strong><span>Primary structural interface for the vehicle hardware.</span></figcaption>
  </figure>
  <figure class="project-gallery__item">
    <img src="{{ '/images/148_final_project/Jetson_Mount.png' | relative_url }}" alt="Jetson Nano and power electronics mount">
    <figcaption><strong>Compute and Power Mount</strong><span>Packaged the Jetson Nano and power-conversion hardware.</span></figcaption>
  </figure>
  <figure class="project-gallery__item project-gallery__item--contain">
    <img src="{{ '/images/148_final_project/IMG2-combined_lidar_camera_mount.png' | relative_url }}" alt="Combined camera and lidar mount CAD model">
    <figcaption><strong>Combined Sensor Mount</strong><span>Maintained the relative position of the forward perception hardware.</span></figcaption>
  </figure>
  <figure class="project-gallery__item project-gallery__item--contain">
    <img src="{{ '/images/148_final_project/IMG4-LCD_mount.png' | relative_url }}" alt="LCD status display mount CAD model">
    <figcaption><strong>LCD Mount</strong><span>Positioned the human-facing status display for visibility and service access.</span></figcaption>
  </figure>
</div>

## Electrical and Feedback Integration

The Jetson Nano handled the primary perception and autonomy workload, while the Arduino Nano provided a dedicated interface for the LCD status display. Separating feedback from the primary motion-control path made system state visible without coupling display behavior directly into the vehicle controller.

<div class="project-gallery__grid">
  <figure class="project-gallery__item project-gallery__item--contain">
    <img src="{{ '/images/148_final_project/wiring_diagram.png' | relative_url }}" alt="Electrical wiring diagram for the autonomous vehicle">
    <figcaption><strong>System Wiring</strong><span>Electrical interfaces between compute, embedded feedback, sensing, and vehicle hardware.</span></figcaption>
  </figure>
  <figure class="project-gallery__item project-gallery__item--contain">
    <img src="{{ '/images/148_final_project/arduino.png' | relative_url }}" alt="Arduino Nano and LCD wiring">
    <figcaption><strong>Embedded Feedback</strong><span>Arduino-controlled interface used to display marker-verification status.</span></figcaption>
  </figure>
</div>

## Integration and Debugging

I coordinated the interfaces between perception, autonomy, actuation, and embedded-feedback code. Because the subsystems were developed by different team members, system-level debugging depended on verifying both the data passed between modules and the timing of each transition.

System-level testing focused on:

- perception timing
- behavior transitions
- steering and throttle response
- valid versus invalid marker handling
- communication between software and embedded feedback
- consistency across repeated demonstrations

### Initial Integrated Behavior Test

<div class="video-wrapper">
  <iframe
    src="https://www.youtube.com/embed/1Sczadr2QxU?mute=1"
    title="Initial person detection and search behavior test"
    allow="encrypted-media; gyroscope; picture-in-picture"
    allowfullscreen>
  </iframe>
</div>

*Initial integrated test showing person detection, vehicle response, and the transition back to searching for another person.*

## Final Validation

The final demonstration connected the full perception-to-actuation pipeline: person detection, depth-based following, marker evaluation, state transitions, vehicle motion, and LCD feedback.

<div class="video-wrapper">
  <iframe
    src="https://www.youtube.com/embed/NoUrJJRty2U?mute=1"
    title="Final person detection and redetection demonstration"
    allow="encrypted-media; gyroscope; picture-in-picture"
    allowfullscreen>
  </iframe>
</div>

*Final integrated demonstration showing person detection, autonomous response, and successful redetection behavior on the completed vehicle.*

## Engineering Outcomes

The completed vehicle demonstrated real-time person detection and depth-based following at distances up to approximately six meters. ArUco markers triggered state-dependent motion responses and corresponding LCD feedback, allowing the complete autonomy pipeline to be demonstrated as an integrated system.

Separating perception, decision logic, vehicle control, and feedback into defined interfaces allowed independently developed team components to be tested individually and then combined into the final behavior.

## Engineering Perspective

This project reinforced that reliable autonomy depends on clearly defined subsystem interfaces. Integration became significantly easier when perception, decision logic, vehicle control, and feedback were treated as separate modules with explicit inputs, outputs, and expected timing.

It also demonstrated the value of explicit state-based behavior. Observable states made transitions easier to test, allowed failures to be isolated more quickly, and provided a clearer framework for coordinating independently developed team components.

GPS waypoint navigation and enhanced obstacle avoidance were deferred so the team could prioritize robust person following, marker recognition, and state-based response within the project schedule.

## Project Documentation

The complete team repository contains the source code, CAD documentation, electrical integration details, and additional project media.

[View the ECE/MAE 148 Team 7 project repository on GitHub](https://github.com/UCSD-ECEMAE-148/fall-2024-final-project-team-7)
