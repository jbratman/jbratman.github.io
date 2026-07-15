---
layout: project-case-study
title: "1/10th-Scale Autonomous Racecar"
subtitle: "Sensor packaging and chassis integration for a racecar-form autonomy platform"
date: 2025-08-20
collection: portfolio
permalink: /racecar/

project_type: "Autonomous Systems · Sensor Packaging"
hero_image: /images/1_10th_racecar/01_Jack_Robot_v6.jpg
hero_summary: >-
  Repackaged lidar, camera, compute, and GPS hardware to convert a research
  robot into a durable, serviceable autonomous racecar compatible with standard RC bodies.

intro_title: "A research platform redesigned to function and present as an autonomous racecar"
intro: >-
  The update preserved the existing perception package while reducing external
  protrusions, adding a second lidar, improving service access, and enabling
  the use of conventional RC body shells.

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

## Front Lidar Integration

A second Livox Mid-360 lidar was integrated into the front area of the vehicle.

The mount needed to position the lidar low enough for body compatibility while preserving usable forward coverage. Camera placement and front-body geometry also had to be coordinated with the lidar mount.

<div class="engineering-decision">
  <p class="engineering-decision__label">Engineering Decision</p>
  <p><strong>Integrate the front lidar through a repeatable body-shell cut template.</strong></p>
  <p>This improved installation consistency and allowed replacement shells to be prepared without recreating the geometry from scratch.</p>
</div>

## Sensor and Compute Repackaging

I redesigned the mounting system for:

- top lidar
- front lidar
- camera
- GPS antenna
- compute hardware
- body-shell interfaces

The new layout reduced exposed hardware while keeping critical components accessible.

## Prototype and Body Integration

Mounts were iterated through CAD, 3D printing, test fitting, and shell modification.

The body installation process included:

- test fitting printed mounts
- checking sensor clearances
- creating cut templates
- validating camera and lidar visibility
- confirming removal and service access

## My Contributions

- primary CAD design for sensor and compute mounts
- lidar and camera packaging
- chassis interface design
- body-shell compatibility
- serviceability improvements
- prototype fabrication and test fitting
- installation planning
- mechanical validation

## Results

The final platform transitioned from a research-oriented robot into a compact autonomous racecar.

Key outcomes included:

- compatibility with standard RC car bodies
- front and top lidar integration
- preserved sensor functionality
- reduced external protrusions
- improved sensor protection
- improved service access
- repeatable body-shell preparation
- standardized mounting geometry for future updates

## Design Progression

### Original Configuration and Initial CAD

<div class="project-gallery__grid">
  <figure class="project-gallery__item">
    <img src="{{ '/images/1_10th_racecar/20250814_111441.jpg' | relative_url }}" alt="Original autonomous research vehicle hardware layout">
    <figcaption><strong>Original Layout</strong><span>Research-oriented packaging before the redesign.</span></figcaption>
  </figure>
  <figure class="project-gallery__item">
    <img src="{{ '/images/1_10th_racecar/00_Jack_Robot_modified_hole_size_v4.jpg' | relative_url }}" alt="Initial CAD redesign of the autonomous racecar">
    <figcaption><strong>Initial CAD</strong><span>First repackaging concept.</span></figcaption>
  </figure>
</div>

### Front Lidar Development

<div class="project-gallery__grid">
  <figure class="project-gallery__item">
    <img src="{{ '/images/1_10th_racecar/20250818_193222.jpg' | relative_url }}" alt="Front lidar mount prototypes">
    <figcaption><strong>Mount Iterations</strong><span>Printed concepts used to validate fit and position.</span></figcaption>
  </figure>
  <figure class="project-gallery__item">
    <img src="{{ '/images/1_10th_racecar/20250814_183841.jpg' | relative_url }}" alt="Selected front lidar mounting position">
    <figcaption><strong>Selected Position</strong><span>Front lidar integrated into the chassis envelope.</span></figcaption>
  </figure>
</div>

### Body Installation

<div class="project-gallery__grid">
  <figure class="project-gallery__item">
    <img src="{{ '/images/1_10th_racecar/20250815_121627.jpg' | relative_url }}" alt="Body-shell cut template for the front lidar">
    <figcaption><strong>Cut Template</strong><span>Repeatable body preparation for lidar installation.</span></figcaption>
  </figure>
  <figure class="project-gallery__item">
    <img src="{{ '/images/1_10th_racecar/20250815_124622.jpg' | relative_url }}" alt="Front lidar and camera mounted through the racecar body">
    <figcaption><strong>Integrated Sensors</strong><span>Front lidar and camera installed with the body shell.</span></figcaption>
  </figure>
</div>
