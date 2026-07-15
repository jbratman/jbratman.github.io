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

The demonstration needed to make autonomous driving visible and understandable to a public audience while remaining inexpensive, portable, and reliable.

The core requirements were:

- total hardware cost below approximately $500
- Raspberry Pi 5 compute
- global-shutter camera perception
- operation inside a 16 ft × 16 ft area
- air-travel-compatible packaging
- fast access for troubleshooting
- clear demonstration of data collection, model training, and autonomous control

A public demonstration environment introduced additional constraints: variable lighting, repeated operating cycles, limited repair time, and the need to explain the system while it was running.

## Platform and Packaging

An existing RC chassis was selected because it met the dimensional requirements and included the core drivetrain components. Minor electrical changes included converting the ESC connector to XT60 and relocating the ESC to accommodate a larger battery.

I translated the chassis hard points into CAD and developed a modular mounting architecture for:

- Raspberry Pi 5
- camera
- PWM servo and motor controller
- power hardware
- wiring and connectors

<div class="engineering-decision">
  <p class="engineering-decision__label">Engineering Decision</p>
  <p><strong>Prioritize modular service access over minimum packaging volume.</strong></p>
  <p>The event environment rewarded rapid diagnosis and component replacement more than marginal reductions in size or mass.</p>
</div>

## Autonomy Integration

The system used a global-shutter camera for image capture and onboard inference for steering control. Training data was collected on the demonstration track and used to develop lane-following models.

My integration work connected:

- image capture
- training-data collection
- model training and deployment
- steering and throttle control
- embedded motor-control hardware
- mechanical mounts and cable routing

The vehicle was tuned progressively from slow validation laps to faster repeatable operation.

## Build, Test, Iterate

The project followed a repeated build-test-refine cycle.

Early testing focused on:

- camera position and field of view
- steering calibration
- throttle limits
- model consistency
- lighting sensitivity
- component temperature
- service access

Later testing emphasized repeatability and recovery from faults rather than maximum lap speed.

> **Test lesson:** A public demo is a reliability problem first and a performance problem second.

## On-Site Demonstration

I was responsible for system setup, troubleshooting, live operation, and technical explanation during the event.

The design allowed the system to be serviced quickly when adjustments were needed. The visible camera, compute, and control architecture also made it easier to explain how the AI model translated training data into steering behavior.

## My Contributions

- defined the overall system architecture
- served as primary CAD designer
- designed chassis, camera, and electronics mounts
- integrated perception, control, and actuation
- implemented the primary autonomy and control workflow
- led system debugging and validation
- prepared the system for transport
- executed on-site setup and operation
- explained the system to attendees

## Results

The racecar operated autonomously on the OpenSauce show floor and demonstrated repeatable lane-following behavior within the constrained track area.

Key outcomes included:

- complete platform below the target hardware budget
- reliable Raspberry Pi 5 perception and control
- repeatable operation under variable event lighting
- high uptime through serviceable hardware design
- successful transport and deployment
- effective public communication of autonomy concepts

## Initial Chassis

<figure>
  <img src="{{ '/images/openSauce/20250709_140232.jpg' | relative_url }}" alt="Original RC chassis selected for the OpenSauce autonomous demo">
  <figcaption>Base chassis selected to meet the size and drivetrain requirements.</figcaption>
</figure>

## CAD Packaging

<figure>
  <img src="{{ '/images/openSauce/AWS_Chassis_Electrical_Mounting_Plate_v20.png' | relative_url }}" alt="CAD model of the modular electronics and sensor mounting system">
  <figcaption>CAD architecture for the Raspberry Pi, camera, and control hardware.</figcaption>
</figure>

## Demonstration Videos

### Initial Validation Lap

<div class="video-wrapper">
  <iframe
    src="https://www.youtube.com/embed/h1-yFdrnhTQ"
    title="Initial slow autonomous validation lap"
    allow="encrypted-media; gyroscope; picture-in-picture"
    allowfullscreen>
  </iframe>
</div>

### Final Autonomous Lap

<div class="video-wrapper">
  <iframe
    src="https://www.youtube.com/embed/Mi3047i9aY0"
    title="Final faster autonomous demonstration lap"
    allow="encrypted-media; gyroscope; picture-in-picture"
    allowfullscreen>
  </iframe>
</div>
