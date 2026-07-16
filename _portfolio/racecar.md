---
layout: project-case-study
title: "1/10th-Scale Autonomous Racecar"
subtitle: "Sensor packaging and chassis integration for a racecar-form autonomy platform"
date: 2025-08-20
collection: portfolio
permalink: /racecar/

project_type: "Autonomous Systems · Sensor Packaging"
hero_image: /images/1_10th_racecar/01_Jack_Robot_v6.jpg
hero_mobile_fit: contain
hero_summary: >-
  Final CAD architecture integrating dual lidar, camera, compute, and GPS
  hardware within a protected, serviceable racecar package compatible with
  standard RC body shells.

intro_title: "A research platform redesigned into an integrated autonomous racecar"
intro: >-
  The final packaging architecture retained the existing perception hardware,
  added a second lidar, reduced exposed components, improved service access,
  and enabled the platform to use conventional RC body shells.

role: "Mechanical Design Lead"
timeline: "August 2025"
team: "Autonomous racing development team"
organization: "Triton AI"
status: "Completed"

tools:
  - CAD
  - 3D Printing
  - Livox Mid-360
  - Camera Integration
  - Rapid Prototyping
  - RC Chassis Hardware

skills:
  - Sensor Packaging
  - Chassis Integration
  - Serviceability
  - Rapid Prototyping

process_heading: "From baseline packaging to an integrated racecar platform"

process:
  - title: "Baseline"
    detail: "Documented the existing research-robot packaging and sensor positions."
  - title: "Constraints"
    detail: "Preserved sensor fields of view, GPS position, strength, and body compatibility."
  - title: "CAD Repackaging"
    detail: "Developed compact mounts for lidar, camera, compute, and body interfaces."
  - title: "Prototype"
    detail: "Printed and test-fit front and upper sensor hardware."
  - title: "Body Integration"
    detail: "Created repeatable templates and cutouts for shell installation."
  - title: "Validation"
    detail: "Verified fit, durability, access, and sensor placement."

results_heading: "Validated through fit, fabrication, and vehicle testing"

results:
  - value: "2× LiDAR"
    label: "Top and front perception coverage"
  - value: "Body Ready"
    label: "Compatible with standard RC body shells"
  - value: "Reduced"
    label: "External hardware protrusions"
  - value: "Improved"
    label: "Sensor and compute protection"
  - value: "Repeatable"
    label: "Body-shell and lidar installation"
  - value: "Serviceable"
    label: "Faster access for testing and repair"

featured: true
order: 4
card_title: "1/10th-Scale Autonomous Racecar"
card_category: "Sensor Packaging"
card_image: /images/1_10th_racecar/01_Jack_Robot_v6.jpg
card_summary: >-
  Sensor packaging and chassis integration for autonomous racing.
card_tags:
  - CAD
  - 3D Printing
  - Sensors
  - Integration

previous_project:
  title: "OpenSauce 2025 Autonomous Demo"
  url: /openSauce/
next_project:
  title: "ECE/MAE 148 Autonomous Vehicle"
  url: /final_project/
---

## The Challenge

The existing vehicle functioned as a research robot, with sensors and compute hardware exposed above and around the chassis. The goal was to preserve the perception system while transitioning the platform into a racecar form factor that could accept standard RC body shells.

The redesign needed to:

- retain the existing top lidar
- preserve GPS antenna position
- add a front Livox Mid-360 lidar
- maintain camera visibility
- protect sensors and compute hardware
- survive impacts and vibration
- improve serviceability
- support repeatable body installation

> **Engineering implication:** Packaging changes could not compromise perception geometry. Every mechanical improvement had to preserve sensor field of view and calibration assumptions.

## Baseline Assessment

The original configuration placed the sensor package prominently above the chassis. This supported research access but limited body compatibility and left hardware exposed.

I documented:

- existing mounting points
- sensor heights and orientations
- cable-routing constraints
- body-shell interference
- likely impact zones
- service-access requirements

<figure class="project-figure project-figure--wide">
  <img
    src="{{ '/images/1_10th_racecar/20250814_111441.jpg' | relative_url }}"
    alt="Original autonomous research vehicle hardware layout"
    loading="lazy">
  <figcaption>
    Original research-oriented configuration with sensors and compute hardware exposed above the chassis.
  </figcaption>
</figure>

## Packaging Architecture

The completed CAD architecture—shown in the page hero—integrated the top lidar, front lidar, camera, GPS antenna, compute hardware, and body interfaces into a common chassis-mounted package.

I developed the layout around the existing chassis interfaces, sensor relationships, service requirements, and available body envelope. The design needed to reduce exposed hardware while preserving access to critical components.

The initial CAD established the shared chassis interfaces and provided a packaging envelope for evaluating body clearance, sensor position, fastener access, and cable routing before fabricating new mounts.

<figure class="project-figure project-figure--wide">
  <img
    src="{{ '/images/1_10th_racecar/00_Jack_Robot_modified_hole_size_v4.jpg' | relative_url }}"
    alt="Initial CAD repackaging concept for the autonomous racecar"
    loading="lazy">
  <figcaption>
    Initial CAD repackaging concept used to coordinate the perception hardware, compute enclosure, chassis interfaces, and RC body envelope.
  </figcaption>
</figure>

## Front Lidar Integration

A second Livox Mid-360 lidar was integrated into the front area of the vehicle.

The mount needed to position the lidar low enough for body compatibility while preserving usable forward coverage. Camera placement, front-body geometry, impact exposure, cable routing, and access to the existing chassis also had to be coordinated with the lidar mount.

Mount concepts were produced through CAD and 3D printing, then test-fit on the chassis to compare physical clearance and sensor position before selecting the final arrangement.

<div class="project-gallery__grid">
  <figure class="project-gallery__item">
    <img src="{{ '/images/1_10th_racecar/20250818_193222.jpg' | relative_url }}" alt="Front lidar mount prototypes">
    <figcaption><strong>Mount Iterations</strong><span>Printed concepts used to evaluate physical fit and lidar position.</span></figcaption>
  </figure>
  <figure class="project-gallery__item">
    <img src="{{ '/images/1_10th_racecar/20250814_183841.jpg' | relative_url }}" alt="Selected front lidar mounting position">
    <figcaption><strong>Selected Position</strong><span>Front lidar packaged within the chassis and body envelope.</span></figcaption>
  </figure>
</div>

<div class="engineering-decision">
  <p class="engineering-decision__label">Engineering Decision</p>
  <p><strong>Package the front lidar within the body envelope without optimizing sensor height alone.</strong></p>
  <p>The selected position balanced forward coverage, body compatibility, impact exposure, camera placement, cable routing, and access to the existing chassis.</p>
</div>

## Body Integration

Once the sensor positions were established, the body shell needed to install consistently around the front lidar and camera without obstructing their view or preventing removal for service.

The body installation process included:

- test fitting printed mounts
- checking sensor clearances
- creating cut templates
- validating camera and lidar visibility
- confirming removal and service access

<div class="project-gallery__grid">
  <figure class="project-gallery__item">
    <img src="{{ '/images/1_10th_racecar/20250815_121627.jpg' | relative_url }}" alt="Body-shell cut template for the front lidar">
    <figcaption><strong>Cut Template</strong><span>Repeatable body preparation for the front lidar installation.</span></figcaption>
  </figure>
  <figure class="project-gallery__item">
    <img src="{{ '/images/1_10th_racecar/20250815_124622.jpg' | relative_url }}" alt="Front lidar and camera mounted through the racecar body">
    <figcaption><strong>Integrated Sensors</strong><span>Front lidar and camera installed with the completed body shell.</span></figcaption>
  </figure>
</div>

Creating a physical cut template made body preparation repeatable. Replacement shells could be aligned to the established sensor geometry without recreating the opening by eye or repeating the complete measurement process.

<div class="engineering-decision">
  <p class="engineering-decision__label">Manufacturing Decision</p>
  <p><strong>Use a reusable cut template to standardize the body opening around the front sensors.</strong></p>
  <p>This improved installation consistency and allowed replacement shells to be prepared without reconstructing the geometry from scratch.</p>
</div>

## Mechanical Validation

The completed packaging was checked through repeated installation and removal of the printed mounts and body shell. Validation focused on the mechanical requirements that could be confirmed directly during integration:

- chassis and body fit
- camera and lidar visibility
- sensor clearance through the body openings
- cable-routing clearance
- access to fasteners and serviceable hardware
- repeatable body-shell alignment

These checks confirmed that the sensors could be integrated within the racecar body while retaining access for continued development and hardware changes.

## Engineering Outcomes

The redesign converted the original research-oriented platform into a compact autonomous racecar compatible with standard RC body shells. The final architecture retained the existing top lidar and GPS position while adding a front Livox Mid-360, integrating the camera, and reducing exposed hardware.

Standardized mounting interfaces and repeatable body-cut templates improved serviceability and made future sensor or body-shell changes easier to implement without rebuilding the entire platform.

## Engineering Perspective

This project reinforced that sensor packaging is part of perception-system design. A mechanically convenient location can still be unacceptable if it changes field of view, introduces occlusion, complicates calibration, or exposes the sensor to impacts.

The final architecture therefore balanced mechanical protection, body compatibility, serviceability, and perception geometry rather than optimizing any one requirement independently.
