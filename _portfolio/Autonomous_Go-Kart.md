---
layout: project-case-study
title: "Autonomous Go-Kart"
subtitle: "Mechanical integration and subsystem development for a student autonomous racing platform"
date: 2025-06-15
collection: portfolio
permalink: /Autonomous_Go-Kart/

project_type: "Autonomous Systems · Mechanical Integration"
hero_image: /images/go_kart/1750071646128.jpg
hero_summary: >-
  Led the mechanical development of an autonomous electric go-kart, improving
  braking response, electrical reliability, battery retention, packaging, and
  serviceability for repeated on-track testing.

intro_title: "Mechanical systems designed around track reliability and rapid iteration"
intro: >-
  The kart combined perception, controls, actuation, power electronics, and
  mechanical hardware within an existing racing chassis. My work focused on
  translating autonomy requirements into durable, serviceable hardware that
  could survive vibration, shock, thermal loading, and active test cycles.

role: "Mechanical Lead"
timeline: "November 2024–August 2025"
team: "Triton AI student engineering team"
organization: "UC San Diego · Triton AI"
status: "Completed"

tools:
  - CAD
  - MATLAB
  - Python
  - Rapid Prototyping
  - Fabrication
  - Track Testing

skills:
  - Mechanical Design
  - Systems Integration
  - Brake Analysis
  - Electrical Packaging

process:
  - title: "Requirements"
    detail: "Defined mounting, thermal, braking, retention, and serviceability needs."
  - title: "Baseline Review"
    detail: "Inspected existing hardware, failures, packaging limits, and test constraints."
  - title: "Analysis"
    detail: "Modeled brake kinematics, force transmission, and subsystem tradeoffs."
  - title: "Design"
    detail: "Developed mounts, enclosures, retention hardware, and packaging layouts."
  - title: "Fabrication"
    detail: "Built and installed revised mechanical hardware for testing."
  - title: "Track Validation"
    detail: "Evaluated durability, serviceability, thermal behavior, and control response."

results:
  - value: "≈1:1"
    label: "Revised actuator-to-brake response"
  - value: ">25%"
    label: "Initial actuator stroke lost before meaningful brake response"
  - value: "Track Tested"
    label: "Subsystems validated under vibration and shock"
  - value: "No Repeat"
    label: "Thermal shutdown recurrence after enclosure redesign"
  - value: "Improved"
    label: "Battery retention and service access"
  - value: "Integrated"
    label: "Mechanical support for autonomy development"

featured: true
order: 2
card_title: "Autonomous Go-Kart"
card_category: "Mechanical Integration"
card_image: /images/go_kart/1750071646128.jpg
card_summary: >-
  Led the mechanical development of Triton AI's autonomous go-kart.
card_tags:
  - Mechanical Design
  - Systems Integration
  - Autonomy

previous_project:
  title: "Payload Delivery Aircraft"
  url: /payload_deliv/
next_project:
  title: "OpenSauce 2025"
  url: /openSauce/
---

## The Challenge

The autonomous go-kart had to support perception, controls, compute, power distribution, and autonomous actuation within an existing racing chassis. The mechanical systems needed to survive vibration, shock, and repeated track use while remaining accessible enough for rapid troubleshooting.

The main constraints included:

- limited mounting locations within the existing chassis
- high vibration and impact loading
- rapid design changes during active testing
- thermal loading from high-current electrical components
- close coupling between sensor placement and autonomy performance
- the need for fast service and repair between track sessions

> **Engineering implication:** Mechanical packaging was part of the autonomy system. A mount, enclosure, or linkage failure could prevent software validation even when the autonomy stack itself was functioning correctly.

## Brake Actuation Analysis

I developed a Python-based analysis tool to characterize the relationship between a linear actuator, crank geometry, master-cylinder stroke, hydraulic pressure, and resulting brake response.

Initial evaluation showed that more than 25% of actuator travel was consumed before meaningful master-cylinder motion began. This compressed braking authority into a narrow region of the actuator stroke and made calibration difficult.

The tool was used to:

- map actuator displacement to master-cylinder travel
- calculate mechanical advantage throughout the stroke
- estimate force transmission and hydraulic response
- compare alternate actuator mounting positions
- identify the geometry causing delayed brake engagement

<div class="engineering-decision">
  <p class="engineering-decision__label">Engineering Decision</p>
  <p><strong>Move the actuator closer to the crank pivot.</strong></p>
  <p>The revised geometry reduced dead travel and produced a response closer to a 1:1 actuator-to-brake relationship, widening the useful control range for the controls team.</p>
</div>

## Battery Retention and Packaging

I evaluated two traction-battery layouts.

The first retained the existing left- and right-side-pod architecture but improved retention and packaging. The second relocated the batteries toward the seat region to centralize mass and reduce lateral center-of-gravity offset.

The centralized layout offered potential handling benefits, but it conflicted with program requirements to preserve a traditional kart appearance and would have required additional fabrication time and funding.

The implemented design retained the side-pod arrangement and added a universal automotive-style hold-down system that improved battery retention under vibration and dynamic loading.

## Electrical Housing Redesign

The existing electronics enclosure had a recurring thermal failure mode. Heat-generating high-current solenoids were packaged inside a single enclosed box, leading to overheating and intermittent shutdowns.

I redesigned the layout to:

- relocate high-heat solenoids outside the primary enclosure
- improve airflow and thermal separation
- maintain debris and contact protection
- improve inspection and debugging access
- preserve compatibility with existing mounting interfaces

> **Validation result:** The revised layout reduced thermal stress on the electrical hardware and prevented recurrence of the prior thermal shutdown behavior during autonomous operation.

## Integration and Track Testing

My mechanical integration work included:

- sensor and compute mounts
- wiring and hardware packaging
- battery retention
- electrical enclosure design
- brake-system geometry
- fabrication and assembly
- serviceability improvements
- track-test support

Hardware was evaluated during repeated on-track sessions. Vibration-related issues, access problems, and packaging conflicts were documented and fed directly into revised designs.

## My Contributions

- led mechanical design and subsystem integration
- developed the brake-analysis tool
- redesigned brake linkage geometry
- evaluated alternate battery layouts
- implemented improved battery retention
- redesigned the electrical enclosure and thermal layout
- designed and fabricated sensor and compute mounts
- supported controls and autonomy teams during test cycles
- participated in track testing and post-test iteration

## Results

The updated hardware provided a more reliable mechanical foundation for autonomous development.

Key outcomes included:

- improved brake control resolution
- improved battery retention under track loading
- reduced thermal stress inside the electrical enclosure
- improved access for debugging and repair
- durable mounting for sensors and compute hardware
- faster iteration during active test sessions

## Lessons Learned

Mechanical integration work on autonomous vehicles must be evaluated at the system level. Packaging decisions affect thermal performance, sensor behavior, serviceability, calibration, and ultimately the amount of useful track time available to the software team.
