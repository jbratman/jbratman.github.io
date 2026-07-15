---
layout: project-case-study
title: "Payload Delivery Aircraft"
subtitle: "Col. Pollo J. Rosso — RC aircraft and in-flight payload delivery system"
date: 2025-06-15
collection: portfolio
permalink: /payload_deliv/

project_type: "Aerospace Engineering · Senior Capstone"
hero_image: /images/delivery_plane/DSC_0420.jpg
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

<div class="engineering-decision">
  <p class="engineering-decision__label">Engineering Decision</p>
  <p><strong>Four-bar linkage with a near-locked closed geometry.</strong></p>
  <p>This reduced continuous servo holding load, improved packaging efficiency, and helped the cargo doors remain secure under vibration and aerodynamic loading.</p>
</div>

### Linkage Analysis

I developed a MATLAB model to evaluate servo rotation, linkage position, and cargo-door travel before fabrication. This allowed the team to compare geometry options and identify binding or insufficient travel before manufacturing hardware.

### Bench-Test Controls

A Python Tkinter interface was used during bench testing to command the deployment servos and repeatedly cycle the mechanism. This simplified troubleshooting before integration into the aircraft radio-control architecture.

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

### Flight 2 — Validation

The revised aircraft demonstrated improved stability, reliable payload-door operation, and successful in-flight payload release.

> **Test lesson:** Kinematic motion alone was not sufficient validation. The mechanism also had to survive vibration, fastener loosening, structural deflection, and repeated actuation under installed conditions.

## My Contributions

- aircraft configuration and sizing studies
- propulsion and propeller analysis
- payload-system architecture
- four-bar linkage design
- MATLAB mechanism simulation
- Python deployment-test interface
- structural CAD and fabrication
- servo, linkage, and avionics integration
- ground and flight testing
- post-test redesign and repair

## Results

The completed aircraft successfully flew with the competition payloads and deployed the required volume payload in flight.

The final configuration achieved:

- approximately 1.4 kg empty weight
- approximately 2.125 kg gross weight
- approximately 0.68 kg weight payload
- approximately 700 cm³ volume payload
- approximately 24% MAC loaded center of gravity
- repeatable payload-door operation
- successful in-flight payload release

## Lessons Learned

The payload system influenced fuselage dimensions, structure, servo placement, avionics packaging, center of gravity, and service access. It had to be designed as part of the aircraft architecture rather than as a late-stage subsystem.

A future iteration would include earlier full-mass deployment testing, formal vibration testing of critical hardware, and continuous center-of-gravity tracking throughout fabrication.

## Flight Video

<div class="video-wrapper">
  <iframe
    src="https://www.youtube.com/embed/oGGQHPh8Jqk"
    title="Payload delivery aircraft successful package drop"
    allow="encrypted-media; gyroscope; picture-in-picture"
    allowfullscreen>
  </iframe>
</div>
