---
layout: project-case-study
title: "OpenSauce 2025 Autonomous Demo"
subtitle: "A low-cost autonomous RC racecar built for continuous public demonstration"
date: 2025-07-19
collection: portfolio
permalink: /openSauce/

project_type: "Robotics · Public Demonstration"
hero_image: /images/openSauce/AWS_Chassis_Electrical_Mounting_Plate.jpg
hero_summary: >-
  Designed, integrated, and operated a sub-$500 autonomous RC racecar capable
  of repeatable lane following inside a transportable 16 ft × 16 ft exhibit.

intro_title: "A complete autonomy stack packaged for reliability, portability, and public engagement"
intro: >-
  The project combined an RC chassis, Raspberry Pi 5, global-shutter camera,
  motor control, custom CAD, training data, and neural-network steering into a
  live demonstration that needed to operate repeatedly in a crowded event environment.

role: "Primary System Integrator"
timeline: "Spring–Summer 2025"
team: "Triton AI demonstration team"
organization: "Triton AI · OpenSauce 2025"
status: "Completed"

tools:
  - Raspberry Pi 5
  - Python
  - CAD
  - DonkeyCar
  - Global-Shutter Camera
  - Embedded Motor Control

skills:
  - Robotics Integration
  - Embedded Systems
  - Mechanical Packaging
  - Public Demonstration

process_heading: "From demonstration constraints to live autonomous operation"

process:
  - title: "Constraints"
    detail: "Set cost, footprint, transport, uptime, and audience requirements."
  - title: "Platform Selection"
    detail: "Selected an RC chassis that met size and hardware needs."
  - title: "CAD Packaging"
    detail: "Mapped chassis interfaces and created modular electronics and camera mounts."
  - title: "Autonomy Setup"
    detail: "Integrated sensing, actuation, data collection, training, and inference."
  - title: "Iteration"
    detail: "Refined speed, steering, robustness, and service access."
  - title: "Live Demo"
    detail: "Transported, deployed, troubleshot, and operated the system at OpenSauce."

results_heading: "Validated through repeated public operation"

results:
  - value: "<$500"
    label: "Target hardware cost"
  - value: "16 × 16 ft"
    label: "Demonstration footprint"
  - value: "Pi 5"
    label: "Onboard perception and inference compute"
  - value: "Live Demo"
    label: "Continuous attendee-facing operation"
  - value: "Repeatable"
    label: "Autonomous lane-following behavior"
  - value: "Portable"
    label: "System transported by air to the event"

featured: true
order: 3
card_title: "OpenSauce 2025 Autonomous Demo"
card_category: "Public Demonstration"
card_image: /images/openSauce/AWS_Chassis_Electrical_Mounting_Plate.jpg
card_summary: >-
  Designed, built, and demonstrated a live autonomous RC racecar at OpenSauce 2025.
card_tags:
  - Robotics
  - Embedded
  - CAD
  - Public Demo

previous_project:
  title: "Autonomous Go-Kart"
  url: /Autonomous_Go-Kart/
next_project:
  title: "1/10th-Scale Autonomous Racecar"
  url: /racecar/
---

## The Challenge

The goal was to create an autonomous-driving demonstration that visitors could understand while watching it operate. Unlike a single test run, the system needed to complete repeated laps in a crowded public environment while remaining inexpensive, portable, and quick to service.

The core requirements included:

- total hardware cost below approximately $500
- Raspberry Pi 5 compute
- global-shutter camera perception
- operation inside a 16 ft × 16 ft area
- air-travel-compatible packaging
- fast access for troubleshooting
- clear demonstration of data collection, model training, and autonomous control

A public demonstration introduced constraints beyond basic lane following. Variable lighting affected perception, repeated operating cycles placed greater demands on reliability, and limited repair time made service access essential. The complete system also needed to survive air travel and be understandable enough to explain while it was running.

> **Engineering implication:** A successful public demonstration depended on uptime and repeatability, not a single fast lap. Packaging, fault recovery, conservative operating limits, and rapid service access were therefore treated as system-level performance requirements.

## System Architecture

The vehicle combined perception, onboard inference, and embedded actuation into a compact autonomy stack. A global-shutter camera captured the track, the Raspberry Pi 5 ran the lane-following model, and the resulting steering and throttle commands were passed through the control hardware to the existing RC drivetrain.

<div class="system-flow" aria-label="Autonomous vehicle system architecture">

  <div class="system-flow__step">
    <span class="system-flow__number">01</span>
    <strong>Perception</strong>
    <span>Global-shutter camera captures the track.</span>
  </div>

  <div class="system-flow__arrow" aria-hidden="true">→</div>

  <div class="system-flow__step">
    <span class="system-flow__number">02</span>
    <strong>Inference</strong>
    <span>Raspberry Pi 5 runs the lane-following model.</span>
  </div>

  <div class="system-flow__arrow" aria-hidden="true">→</div>

  <div class="system-flow__step">
    <span class="system-flow__number">03</span>
    <strong>Commands</strong>
    <span>The model generates steering and throttle targets.</span>
  </div>

  <div class="system-flow__arrow" aria-hidden="true">→</div>

  <div class="system-flow__step">
    <span class="system-flow__number">04</span>
    <strong>Control</strong>
    <span>PWM hardware translates commands into outputs.</span>
  </div>

  <div class="system-flow__arrow" aria-hidden="true">→</div>

  <div class="system-flow__step">
    <span class="system-flow__number">05</span>
    <strong>Actuation</strong>
    <span>Steering servo and ESC control the RC chassis.</span>
  </div>

</div>

<div class="engineering-decision">
  <p class="engineering-decision__label">System-Level Implication</p>
  <p>
    Changes to any stage of the pipeline affected the others: camera placement
    influenced model performance, steering calibration affected control response,
    and packaging determined how quickly the system could be serviced during the
    event.
  </p>
</div>

## Platform and Packaging

An existing RC chassis was selected because it met the dimensional requirements and already included the core drivetrain components. This reduced cost and allowed development effort to remain focused on autonomy, packaging, and reliability. Electrical changes included converting the ESC connector to XT60 and relocating the ESC to accommodate a larger battery.

<figure class="project-figure project-figure--wide">
  <img
    src="{{ '/images/openSauce/20250709_140232.jpg' | relative_url }}"
    alt="Original RC chassis selected for the Open Sauce autonomous demonstration"
    loading="lazy">
  <figcaption>
    Base RC chassis selected to meet the demonstration footprint, cost, and drivetrain requirements.
  </figcaption>
</figure>

I translated the chassis hard points into CAD and developed a modular mounting architecture for:

- Raspberry Pi 5
- camera
- PWM servo and motor controller
- power hardware
- wiring and connectors

<figure class="project-figure project-figure--wide">
  <img
    src="{{ '/images/openSauce/AWS_Chassis_Electrical_Mounting_Plate_v20.png' | relative_url }}"
    alt="CAD model of the modular electronics and sensor mounting system"
    loading="lazy">
  <figcaption>
    CAD packaging architecture for the Raspberry Pi, camera, control electronics, and serviceable wiring interfaces.
  </figcaption>
</figure>

<div class="engineering-decision">
  <p class="engineering-decision__label">Engineering Decision</p>
  <p><strong>Prioritize modular service access over minimum packaging volume.</strong></p>
  <p>The event environment rewarded rapid diagnosis and component replacement more than marginal reductions in size or mass.</p>
</div>

## Autonomy Integration

The system used a global-shutter camera for image capture and onboard inference for steering control. Training data was collected on the demonstration track and used to develop and refine lane-following models for the event environment.

My integration work connected:

- image capture
- training-data collection
- model training and deployment
- steering and throttle control
- embedded motor-control hardware
- mechanical mounts and cable routing

This work connected the software pipeline to the physical vehicle. Camera placement affected the training data, steering calibration affected model response, and throttle limits determined whether the vehicle could recover from prediction errors within the confined track. The vehicle was therefore tuned progressively from slow validation laps to faster repeatable operation.

## Testing for Repeatability

The project followed a repeated build-test-refine cycle.

Early testing focused on:

- camera position and field of view
- steering calibration
- throttle limits
- model consistency
- lighting sensitivity
- component temperature
- service access

Later testing emphasized repeatability and recovery from faults rather than maximum lap speed. Initial laps used conservative throttle limits to verify camera placement, steering direction, inference, and track recognition before increasing vehicle speed.

### Initial Validation

<div class="video-wrapper">
  <iframe
    src="https://www.youtube.com/embed/h1-yFdrnhTQ"
    title="Initial slow autonomous validation lap"
    allow="encrypted-media; gyroscope; picture-in-picture"
    allowfullscreen>
  </iframe>
</div>

The initial validation configuration prioritized controllability and provided a baseline for refining steering calibration, throttle limits, camera position, and training data.

> **Test lesson:** A public demo is a reliability problem first and a performance problem second.

## On-Site Demonstration

I prepared the vehicle for air transport and was responsible for system setup, troubleshooting, live operation, and technical explanation during the event.

The modular packaging allowed the compute, power, and control hardware to be accessed quickly when adjustments were needed. Keeping the camera, compute, and control architecture visible also made it easier to explain how training data was translated into steering behavior while the vehicle operated.

### Final Demonstration Configuration

<div class="video-wrapper">
  <iframe
    src="https://www.youtube.com/embed/Mi3047i9aY0"
    title="Final faster autonomous demonstration lap"
    allow="encrypted-media; gyroscope; picture-in-picture"
    allowfullscreen>
  </iframe>
</div>

After progressive testing and calibration, the final configuration completed faster, repeatable autonomous laps within the constrained demonstration area.

## Engineering Outcomes

The completed vehicle operated autonomously on the Open Sauce show floor and demonstrated repeatable lane-following behavior within the 16 ft × 16 ft track area. The platform remained below the target hardware budget, survived air transport, and supported repeated attendee-facing operation under changing show-floor conditions.

The modular mechanical and electrical architecture provided rapid access for troubleshooting, while progressive speed testing created a controlled path from initial validation to reliable autonomous laps. The finished system demonstrated that a useful autonomy exhibit could be built from accessible hardware without sacrificing serviceability or public engagement.

## Engineering Perspective

This project reinforced that deploying autonomy requires more than achieving correct model output. Camera placement, electrical packaging, steering calibration, thermal behavior, transport constraints, service access, and operating procedures all affected whether the system could perform reliably in front of an audience.

It also demonstrated the value of designing around the real mission. Maximum speed was less important than repeatable operation, quick recovery, and a system architecture that visitors could understand. Treating those needs as engineering requirements shaped the final platform and made the live demonstration successful.
