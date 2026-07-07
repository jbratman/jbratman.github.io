---
title: "Autonomous Go-Kart"
date: 2025-06-15
collection: portfolio
tags: [CAD, MATLAB, Python, Mechanical Design, Autonomous Systems]

excerpt: |
  **Overview**
  - **System:** Autonomous electric go-kart developed for Formula-style autonomous racing
  - **Role:** Mechanical Lead responsible for subsystem design, packaging, integration, and testing
  - **Tools:** CAD, MATLAB, Python, rapid prototyping, fabrication
  - **Outcome:** Designed, integrated, and validated mechanical systems supporting autonomous vehicle development and track testing

header:
  teaser: go_kart/1750071646128.jpg

featured: true
order: 2

card_category: "Mechanical Integration"

card_image: /images/go_kart/1750071646128.jpg

card_summary: >
  Led the mechanical development of Triton AI's autonomous go-kart.

card_tags:
  - Mechanical Design
  - Systems Integration
  - Autonomy
  
---

## Overview
- **System:** Autonomous go-kart platform for student racing autonomy
- **Role:** Mechanical Lead
- **Tools:** CAD, MATLAB, rapid prototyping
- **Outcome:** Designed and tested mechanical subsystems supporting autonomy development and on-track validation

## My Primary Engineering Responsibilities
- Led mechanical design and integration for the autonomous go-kart platform
- Designed and fabricated mounts for sensors, compute hardware, and wiring
- Ensured structural integrity and serviceability under vibration and track loads
- Supported autonomy and controls teams through hardware iteration and testing
- Participated in on-track testing to validate mechanical robustness

## Engineering Constraints & Environment
- High vibration and shock loads during on-track operation
- Limited mounting locations within an existing kart chassis
- Rapid iteration requirements during active testing periods
- Need for quick access and serviceability of sensors and compute hardware
- Close coupling between mechanical layout and autonomy sensor performance

## Build, Test, Iterate
- Fabricated and installed sensor and compute mounts for track testing
- Evaluated hardware durability during repeated on-track sessions
- Identified vibration-related issues and refined mounting designs
- Updated layouts to improve access, cable management, and serviceability

## Subsystem Design & Analysis
### Brake System Analysis Tool (Python GUI)

I developed a Python-based GUI to analyze the kinematic relationship between a linear actuator and the brake master cylinder after identifying inconsistent and poorly documented brake performance across prior configurations.

Initial testing revealed that more than 25% of the actuator stroke was consumed before generating meaningful master cylinder response, resulting in a narrow and difficult-to-control braking window. The analysis tool allowed actuator mounting geometry to be varied interactively in order to evaluate stroke utilization, mechanical advantage, and resulting brake force output.

- Modeled actuator-driven crank geometry to map actuator displacement to master cylinder stroke
- Quantified mechanical advantage and force transmission as a function of actuator mounting position
- Verified actuator force output against prior capstone assessments to establish reasonable force targets
- Identified suboptimal initial actuator placement that delayed brake engagement
- Used the tool to relocate the actuator closer to the crank pivot, improving stroke utilization and control resolution
- Collaborated with the controls team to demonstrate improved brake responsiveness, enabling more stable and predictable control calibration

The revised geometry produced a response closer to a 1:1 actuator-to-brake relationship, significantly widening the usable control window and improving braking consistency prior to hardware testing.

### Battery Box Design

I developed and evaluated two battery enclosure concepts to securely mount the traction batteries within the go-kart chassis while balancing structural integrity, vehicle dynamics, and project constraints.

The first concept retained the existing architecture, with batteries housed in the left and right side pods adjacent to the driver seat. This redesign focused on improving packaging and retention while maintaining compatibility with the current chassis layout.

The second concept proposed relocating the batteries to the seat region to centralize mass and improve the vehicle’s center of gravity. This configuration offered improved mass distribution and handling potential, with a future enclosure cover proposed to further enhance aerodynamic performance. This concept was ultimately not pursued due to program-level requirements to retain the traditional kart appearance for competition and demonstration purposes.

- Designed a revised side-pod battery mounting solution to withstand vibration, shock loads, and on-track dynamics  
- Evaluated centralized battery placement to reduce CG offset and improve mass centralization  
- Assessed structural retention, accessibility, and serviceability for both configurations  
- Considered aerodynamic implications and future enclosure enhancements  
- Balanced performance benefits against schedule, cost, and fabrication constraints  

Due to limited time and funding, the original side-pod battery configuration was retained for implementation. However, a universal automotive-style battery hold-down that I proposed was incorporated into the existing architecture, significantly improving battery retention and robustness under on-track vibration and dynamic loading.

### Electrical Housing Design

I redesigned the electrical housing and component layout after identifying a recurring thermal failure mode that had previously caused electrical shutdowns during competition testing.

Prior to my involvement, heat-generating components—particularly high-current solenoids—were packaged within a single enclosed electronics box, leading to overheating and intermittent system failures. My work focused on improving thermal management, component placement, and serviceability while maintaining protection in a high-vibration environment.

- Relocated heat-generating solenoids outside of the primary electronics enclosure to reduce internal thermal load
- Refined internal component placement to improve airflow and thermal separation
- Incorporated passive airflow paths to support convective cooling of remaining electronics
- Maintained protection from vibration, debris, and incidental contact during on-track operation
- Improved accessibility for inspection, debugging, and iterative testing

The revised layout significantly reduced thermal stress on critical electrical components, improving system reliability and preventing recurrence of thermal shutdowns during autonomous operation.


## Key Results
- Delivered mechanically robust hardware supporting autonomous testing on track
- Enabled reliable sensor and compute mounting under vibration and shock loads
- Improved serviceability and iteration speed during active testing cycles
- Supported autonomy development through dependable mechanical integration


