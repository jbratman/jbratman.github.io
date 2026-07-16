---
layout: project-case-study
title: "Autonomous Go-Kart"
subtitle: "Mechanical integration and subsystem development for an autonomous racing platform"
date: 2025-06-15
collection: portfolio
permalink: /Autonomous_Go-Kart/

project_type: "Autonomous Systems · Mechanical Integration"
hero_image: /images/go_kart/1750071646128.jpg
hero_summary: >-
  Led the mechanical development of an autonomous electric go-kart, improving
  braking response, electrical reliability, battery retention, packaging, and
  serviceability for repeated on-track testing.

intro_title: "Engineering Reliable Hardware for Autonomous Racing"
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

process_heading: "From system constraints to track-validated vehicle hardware"

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

results_heading: "Validated through build and track testing"

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

Triton AI is developing an autonomous electric go-kart to compete in the Autonomous Karting Series, where success depended on completing fast, consistent, and reliable autonomous laps. During the previous season, the team demonstrated race-winning pace but recurring mechanical and thermal reliability issues prevented the vehicle from consistently finishing events, ultimately resulting in a second-place overall finish.

Entering the new season, improving reliability became just as important as improving autonomous performance. As Mechanical Lead, I was responsible for designing, integrating, and validating the vehicle's mechanical subsystems to support reliable autonomous operation.

My work included brake actuation, electrical packaging, battery retention, sensor integration, and overall vehicle integration within an existing racing chassis. Every design balanced performance, durability, serviceability, and manufacturability while supporting a team that was continuously iterating on both hardware and software.

### Key Engineering Constraints

- Existing chassis geometry severely limited available mounting locations.
- Hardware needed to survive continuous vibration, impacts, and repeated track sessions.
- Sensor placement directly affected perception accuracy and autonomous performance.
- High-current electrical components generated significant thermal loads that influenced enclosure design.
- Components had to remain easily accessible for rapid maintenance and debugging between test sessions.
- Hardware designs needed to accommodate frequent software-driven changes without requiring complete redesigns.

> **Engineering implication:** Winning required more than advanced autonomy software. It requires maximizing productive testing time. Every hour spent repairing hardware, diagnosing thermal issues, or recalibrating sensors was an hour that couldn't be spent collecting data, validating software, or improving lap times. Reliable mechanical systems became a force multiplier for the entire engineering team.

## Brake System Analysis & Optimization

During autonomous testing, the brake system exhibited inconsistent response that made braking difficult to calibrate. Initial actuator movement produced little hydraulic pressure, compressing most of the available braking authority into a small portion of the actuator stroke. This limited braking resolution and reduced the controls team's ability to tune repeatable autonomous braking behavior.

Rather than relying on trial-and-error modifications, I developed a custom Python analysis tool to model the complete brake system. The model simulated the relationship between linear actuator displacement, linkage geometry, master-cylinder stroke, hydraulic pressure, clamp force, and braking torque, allowing design changes to be evaluated before manufacturing new hardware.

<figure class="project-figure project-figure--analysis">
  <img src="/images/go_kart/brake_gui.jpg" alt="Python brake analysis tool">
  <figcaption>
    Custom Python analysis tool developed to model linkage geometry, hydraulic pressure, clamp force, and braking torque while allowing rapid evaluation of alternative actuator positions.
  </figcaption>
</figure>

The analytical model was used to:

- Map actuator displacement to master-cylinder travel.
- Calculate changing mechanical advantage throughout the stroke.
- Estimate hydraulic pressure, clamp force, and braking torque.
- Compare alternate actuator mounting locations.
- Quantify the effects of linkage geometry before fabrication.

## Baseline Response

The initial analysis revealed that more than **25% of actuator travel** was consumed before meaningful master-cylinder displacement occurred. This dead-travel region compressed useful brake control into the remaining actuator stroke, making the system unnecessarily sensitive and difficult for the controls team to calibrate.

<figure class="project-figure project-figure--medium">
  <img src="/images/go_kart/Original_brake_response.jpg" alt="Original brake response">
  <figcaption>
    Initial brake response showing substantial actuator travel before hydraulic pressure increased, leaving a narrow region for useful brake modulation.
  </figcaption>
</figure>

<div class="engineering-decision">
  <p class="engineering-decision__label">Engineering Decision</p>
  <p><strong>Relocate the linear actuator slightly closer to the crank pivot to increase usable braking resolution while retaining the existing hydraulic system.</strong></p>
  <p>
    Rather than redesigning the hydraulic system, the analytical model showed that a small change in actuator position would improve the linkage geometry, allowing hydraulic pressure to build earlier in the actuator stroke while maintaining the existing brake hardware.
  </p>
</div>

## Concept Evaluation

The analytical model indicated that only a small change in actuator mounting location was required. Moving the actuator approximately one inch closer to the crank pivot and slightly higher improved the effective mechanical advantage early in the stroke while leaving the remainder of the brake hardware unchanged.

<figure class="project-figure project-figure--medium">
  <img src="/images/go_kart/brake_linkage_design.jpg" alt="Brake linkage concept">
  <figcaption>
    Simplified concept illustration showing the design intent. The actual implementation retained the original linkage while repositioning only the actuator mounting location.
  </figcaption>
</figure>

## Design Validation

The updated actuator location was re-evaluated using the analytical model before fabrication. The revised geometry produced hydraulic pressure much earlier in the actuator stroke, creating a response much closer to a linear relationship between actuator displacement and brake output while maintaining the required braking performance.

<figure class="project-figure project-figure--analysis">
  <img src="/images/go_kart/brake_analysis_tool.jpg" alt="Updated brake analysis">
  <figcaption>
    Updated analytical model showing improved brake response after repositioning the actuator, providing increased usable braking resolution while maintaining clamp force and braking torque.
  </figcaption>
</figure>

Developing the analytical model allowed actuator positions to be evaluated before modifying hardware. This reduced physical trial-and-error, provided quantitative justification for the final mounting location, and gave the controls team a significantly more predictable brake response for calibration.

## Implemented Hardware

The revised actuator mounting was fabricated and integrated into the autonomous race kart prior to track testing. Although the physical change consisted only of relocating the actuator mounting position, the completed system demonstrated approximately 25% less linkage free travel before brake engagement while retaining the existing hydraulic hardware.

<figure class="project-figure project-figure--wide">
  <img src="/images/go_kart/1750071649984.jpg" alt="Brake system installed on kart">
  <figcaption>
    Final actuator mounting integrated into Triton AI's autonomous race kart. A small change in actuator position produced a significant improvement in usable braking resolution without redesigning the brake hardware.
  </figcaption>
</figure>
<div class="brake-results-grid">
  <div class="brake-result-card">
    <span class="brake-result-card__value">~25%</span>
    <span class="brake-result-card__label">Reduction in linkage free travel</span>
  </div>

  <div class="brake-result-card">
    <span class="brake-result-card__value">Earlier</span>
    <span class="brake-result-card__label">Hydraulic pressure build-up</span>
  </div>

  <div class="brake-result-card">
    <span class="brake-result-card__value">Unchanged</span>
    <span class="brake-result-card__label">Existing hydraulic brake hardware</span>
  </div>

  <div class="brake-result-card">
    <span class="brake-result-card__value">Python</span>
    <span class="brake-result-card__label">Model-guided actuator repositioning</span>
  </div>
</div>

## Battery Retention & Packaging

The existing traction batteries were mounted in enclosures on the left and right side pods of the kart. Although this arrangement preserved the vehicle’s traditional layout, the batteries required more secure retention under vibration and dynamic track loading, and the enclosures needed better access for inspection and maintenance.

I developed two packaging concepts to evaluate whether the existing architecture should be improved or replaced.

### Concept 1 — Modified Side-Pod Enclosures

The first concept retained the existing left and right-side enclosures while replacing the improvised retention arrangement with universal automotive-style battery mounts. Quick-release pins and hinges were also evaluated to improve access without requiring the enclosures to be completely removed.

This approach offered several practical advantages:

- Reused much of the existing enclosure architecture.
- Required fewer changes to vehicle wiring and packaging.
- Improved battery retention using commercially available hardware.
- Preserved the kart’s existing appearance.
- Reduced fabrication time and implementation risk.

### Concept 2 — Center-Chassis Packaging

The second concept relocated both batteries toward the seat region. Centralizing the batteries would reduce lateral center-of-gravity offset and allow their position to partially counterbalance the motor’s mass.

However, this concept required a new enclosure and mounting structure, additional fabrication, possible wiring extensions, and further packaging development around the seat and rear chassis tubes. The available CAD also lacked sufficient detail to confirm every clearance before physical inspection.

<div class="project-comparison">
  <figure class="project-figure">
    <img
      src="{{ '/images/go_kart/wing_mount_battery_design.jpg' | relative_url }}"
      alt="Side-pod battery concept using an automotive-style hold-down"
      loading="lazy">
    <figcaption>
      <strong>Modified side-pod concept.</strong>
      Retained the existing vehicle architecture while improving battery
      retention and enclosure access.
    </figcaption>
  </figure>

  <figure class="project-figure">
    <img
      src="{{ '/images/go_kart/center_battery_design.jpg' | relative_url }}"
      alt="Center-chassis concept relocating the traction batteries behind the seat"
      loading="lazy">
    <figcaption>
      <strong>Center-chassis concept.</strong>
      Relocated the batteries toward the seat to centralize mass and partially
      offset the motor’s lateral weight.
    </figcaption>
  </figure>
</div>

<div class="engineering-decision">
  <p class="engineering-decision__label">Engineering Decision</p>
  <p><strong>Retain the side-pod architecture and improve the battery-retention system.</strong></p>
  <p>
    Although the center-chassis concept offered potential mass-distribution benefits,
    those benefits did not justify the additional cost, fabrication effort, packaging
    uncertainty, and disruption to the existing vehicle architecture. The side-pod
    solution addressed the immediate reliability problem while minimizing implementation
    risk.
  </p>
</div>

### Implemented Solution

The final design retained the existing side-pod arrangement and added universal automotive-style hold-down hardware. This provided more secure battery retention under vibration and track loading while preserving the existing vehicle layout and avoiding unnecessary changes to the electrical system.

The result was not the most aggressive packaging concept but the solution that best balanced reliability, cost, schedule, serviceability, and integration risk.

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


## Systems Engineering Perspective

This project reinforced that autonomous vehicle performance depends on far more than perception and controls software. Mechanical packaging, thermal management, serviceability, and subsystem integration directly determine how much productive testing a team can accomplish. Designing reliable hardware not only improves vehicle performance—it enables the software team to collect more data, iterate faster, and spend more time improving autonomy instead of repairing the vehicle.
