---
layout: project-case-study
title: "Payload Delivery Aircraft"
subtitle: "Col. Pollo J. Rosso — RC aircraft and in-flight payload delivery system"
date: 2025-06-15
collection: portfolio
permalink: /payload_deliv/

project_type: "Aerospace Engineering · Senior Capstone"
hero_image: /images/delivery_plane/DSC_0420.jpg
hero_mobile_position: "70% center"
hero_summary: >-
  Senior aerospace capstone focused on designing and flight-validating a
  competition aircraft with an integrated in-flight payload deployment system.

intro_title: "A complete aircraft developed around an integrated payload mission"
intro: >-
  This project combined aircraft sizing, propulsion analysis, structural
  fabrication, controls integration, mechanism design, and flight testing.
  My primary ownership centered on the payload-delivery architecture,
  four-bar door mechanism, structural integration, and build-test iteration.

role: "Co-Lead Mechanical Design · Payload System · Fabrication · Flight Testing"
timeline: "January–June 2025"
team: "6 aerospace engineering seniors"
organization: "UC San Diego"
status: "Completed"

tools:
  - Fusion 360
  - MATLAB
  - Python
  - 3D Printing
  - Laser Cutting
  - RC Aircraft Systems

skills:
  - Aircraft Design
  - Payload Systems
  - Mechanism Design
  - Flight Test

process_heading: "From requirements to validated flight hardware"

process:
  - title: "Requirements"
    detail: "Defined payload, propulsion, safety, and mission constraints."
  - title: "Sizing"
    detail: "Established wing loading, thrust margin, cruise speed, and geometry."
  - title: "Concept"
    detail: "Selected high-wing architecture and integrated payload-bay layout."
  - title: "Analysis"
    detail: "Modeled propulsion and four-bar linkage motion."
  - title: "Fabrication"
    detail: "Built airframe, payload hardware, and avionics packaging."
  - title: "Flight Test"
    detail: "Validated, diagnosed failures, redesigned, and completed deployment."

results_heading: "Validated through build and flight testing"

results:
  - value: "2.125 kg"
    label: "Gross aircraft weight as flown"
  - value: "20 m/s"
    label: "Target cruise speed"
  - value: "700 cm³"
    label: "Volume payload capacity"
  - value: "24% MAC"
    label: "Loaded center-of-gravity location"
  - value: "≈90°"
    label: "Payload-door travel"
  - value: "Flight Validated"
    label: "Successful in-flight payload deployment"

lead_image:
  image: /images/delivery_plane/IMG_0004.JPG
  alt: "UC San Diego MAE 155B team with the completed payload delivery aircraft"
  caption: "UC San Diego MAE 155B Team MJ5 — Spring 2025"

featured: true
order: 1
card_title: "Payload Delivery Aircraft"
card_category: "Aircraft Design"
card_image: /images/delivery_plane/DSC_0420.jpg
card_summary: >-
  Designed and flight-tested a competition aircraft with a custom four-bar
  payload delivery mechanism.
card_tags:
  - Aircraft Design
  - CAD
  - Flight Testing
  - Mechanisms

project_links:
  - label: "View Final Design Review"
    url: /files/docs/payload_delivery/FDR_MJ5.pdf
    primary: true
  - label: "View Senior Day Poster"
    url: /files/docs/payload_delivery/Team_3_MJ5_Poster_colored_fixedlogo.pdf

documents:
  - type: "Design Review"
    title: "Preliminary Design Review"
    description: "Early sizing, requirements, architecture, and risk assessment."
    pdf: /files/docs/payload_delivery/PDR_MJ5.pdf
    pptx: /files/docs/payload_delivery/PDR_Presentation.pptx
  - type: "Design Review"
    title: "Final Design Review"
    description: "Final configuration, subsystem details, testing, and results."
    pdf: /files/docs/payload_delivery/FDR_MJ5.pdf
    pptx: /files/docs/payload_delivery/FDR_Presentation.pptx
  - type: "Poster"
    title: "Senior Day Poster"
    description: "Condensed project summary presented at UC San Diego Senior Day."
    pdf: /files/docs/payload_delivery/Team_3_MJ5_Poster_colored_fixedlogo.pdf

next_project:
  title: "Autonomous Racecar Updates"
  url: /racecar/
---

## The Challenge

The competition required an electrically powered aircraft that could carry two payload classes, complete the prescribed flight course, and deploy a volume payload while airborne. The aircraft also had to pass an empty-weight validation flight before attempting the scored mission.

The key constraints were:

- Package 1: lead weights with a minimum mass of 0.5 lb
- Package 2: an empty cardboard box with a minimum volume of 500 cm³
- Package 2 had to be deployed in flight
- The aircraft had to use the assigned motor, ESC, battery, and receiver
- The design had to remain safe, manufacturable, and repairable within the capstone schedule

> **Engineering implication:** The payload system could not be treated as a secondary add-on. Its volume, mass, actuation loads, and service access directly affected the fuselage architecture and aircraft center of gravity.

## Aircraft Architecture

A high-wing configuration with approximately three degrees of dihedral was selected to support predictable handling and payload stability. The aircraft used a balsa wing, plywood fuselage, and lightweight empennage structure, with the payload systems positioned near the aircraft center of gravity.

The final aircraft used:

- NACA 4412 wing airfoil
- NACA 0012 empennage airfoil
- approximately 0.23 m² wing area
- approximately 1.15 m wingspan
- approximately 20 m/s cruise speed
- approximately 10–11 m/s stall speed

<div class="engineering-decision">
  <p class="engineering-decision__label">Engineering Decision</p>
  <p><strong>High-wing architecture over a faster, lower-drag configuration.</strong></p>
  <p>The selected layout prioritized predictable low-speed handling, payload stability, fabrication access, and mission completion rather than maximum speed.</p>
</div>

## Sizing and Propulsion

Initial sizing used wing-loading and thrust-to-weight trade studies. The fixed propulsion package included a Cobra C-2217/16 1180 KV motor, 40 A ESC, 3S 1800 mAh LiPo battery, and FrSky X8R receiver.

An APC 9×6E propeller was selected after comparing predicted thrust against the 8×6E alternative. At approximately 9,000 RPM, the 9×6E provided the required cruise thrust with practical margin.

The propulsion analysis supported:

- approximately 3 N cruise thrust requirement
- approximately 10 N available static thrust
- approximately 0.5 thrust-to-weight ratio as flown
- short takeoff distance within the available test environment

## Payload Mechanism

The volume payload was housed in a 3D-printed bomb-bay module integrated into the lower fuselage. The final mechanism used two micro-servos and a four-bar linkage to drive opposing cargo doors through approximately 90 degrees of rotation.

<figure class="project-figure project-figure--wide">
  <img
    src="{{ '/images/delivery_plane/Delivery_Assembly_CAD.jpg' | relative_url }}"
    alt="CAD model of the payload bay, opposing cargo doors, servos, and four-bar linkage"
    loading="lazy">
  <figcaption>
    Payload-bay CAD showing the opposing cargo doors, dual micro-servos, and
    four-bar linkage integrated into the lower fuselage structure.
  </figcaption>
</figure>

<div class="engineering-decision">
  <p class="engineering-decision__label">Engineering Decision</p>
  <p><strong>Use a four-bar linkage with a near-locked closed geometry.</strong></p>
  <p>
    The selected linkage reduced continuous servo holding load, improved
    packaging efficiency, and helped the cargo doors remain secure under
    vibration and aerodynamic loading.
  </p>
</div>

### Linkage Analysis

I developed a MATLAB model to evaluate servo rotation, linkage position, and cargo-door travel before fabrication. This allowed the team to compare geometry options and identify binding or insufficient travel before manufacturing hardware.

<figure class="project-figure project-figure--animation">
  <img
    src="{{ '/images/delivery_plane/fourbar_animation.gif' | relative_url }}"
    alt="MATLAB four-bar linkage simulation showing the payload-door motion"
    loading="lazy">
  <figcaption>
    MATLAB linkage simulation used to evaluate servo input, crank rotation,
    and cargo-door travel before fabrication.
  </figcaption>
</figure>

### Bench-Test Controls

A Python Tkinter interface was used during bench testing to command the deployment servos and repeatedly cycle the mechanism. This simplified troubleshooting before integration into the aircraft radio-control architecture.

<figure class="project-figure project-figure--medium">
  <video
    controls
    muted
    loop
    playsinline
    preload="metadata">
    <source
      src="{{ '/videos/delivery_plane/20250521_174541.mp4' | relative_url }}"
      type="video/mp4">
    Your browser does not support embedded video.
  </video>
  <figcaption>
    Integrated payload mechanism undergoing repeated bench testing before
    installation of the final radio-control interface.
  </figcaption>
</figure>

## Structural Integration and Fabrication

The airframe used a balsa wing with a plywood center section and a 2 mm plywood fuselage. Printed parts included the payload bay, cargo doors, thrust-line shim, tailwheel pivot, spinner, and nose components.

My fabrication and integration work included:

- payload-bay architecture and packaging
- four-bar linkage design
- servo and linkage mounting
- fuselage structural components
- avionics packaging
- motor-position and thrust-line adjustments
- ground-test and flight-test support

## Flight Testing and Iteration

The first flights exposed integration issues that were not fully apparent during bench testing.

### Flight 1 — Problems Identified

- aft center of gravity
- motor vibration and fastener loosening
- payload-servo mount failure
- excess tail mass

### Iteration

- moved the motor approximately 15 mm forward
- rebuilt the tail with lighter balsa construction
- secured critical fasteners with threadlocker
- redesigned and reinforced the servo mount

<figure class="project-figure project-figure--medium">
  <img
    src="{{ '/images/delivery_plane/motor_extension_and_shim.jpg' | relative_url }}"
    alt="Motor extension and angled thrust-line shim installed on the aircraft"
    loading="lazy">
  <figcaption>
    Plywood motor extension and 3D-printed thrust-line shim used to move the
    motor approximately 15 mm forward while introducing right and down thrust.
    The change helped correct the aft center of gravity and improve power-on
    behavior.
  </figcaption>
</figure>

### Flight 2 — Validation

The revised aircraft demonstrated improved stability, reliable payload-door operation, and successful in-flight payload release.

> **Test lesson:** Kinematic motion alone was not sufficient validation. The mechanism also had to survive vibration, fastener loosening, structural deflection, and repeated actuation under installed conditions.


## Engineering Perspective

This project reinforced that the payload system could not be developed independently from the rest of the aircraft. Its dimensions, mass, linkage geometry, servo placement, structural loads, and service requirements directly influenced the fuselage architecture, avionics packaging, and aircraft center of gravity.

It also demonstrated the limitations of validating mechanisms only through kinematic analysis and bench testing. Future development would include earlier full-mass deployment testing, formal vibration testing of critical hardware, and continuous center-of-gravity tracking throughout fabrication.

## Flight Video

<div class="video-wrapper">
  <iframe
    src="https://www.youtube.com/embed/oGGQHPh8Jqk"
    title="Payload delivery aircraft successful package drop"
    allow="encrypted-media; gyroscope; picture-in-picture"
    allowfullscreen>
  </iframe>
</div>
