---
layout: project-case-study
title: "Aero-Structural Analysis"
subtitle: "CFD-informed structural trade study of automotive rear-wing supports"
date: 2024-08-06
collection: portfolio
permalink: /aerodynamic_analysis/

project_type: "Engineering Analysis · Aerodynamics and Structures"
hero_image: /images/aero_analysis_project/Baseline Flow.jpg
hero_summary: >-
  Used SolidWorks Flow Simulation and finite element analysis to compare
  conventional under-wing and swan-neck stanchions across three material systems.

intro_title: "Connecting aerodynamic loading to a structural architecture decision"
intro: >-
  Rear-wing supports must carry substantial downforce without excessive stress or
  deflection, but their placement can also influence the aerodynamic performance of
  the wing. This individual study established a common CFD-derived load case and used
  it to compare two support geometries across steel, aluminum, and composite materials.

role: "Primary Analyst"
timeline: "Summer 2024"
team: "Individual project"
organization: "UC San Diego · MAE 150"
status: "Completed"

tools:
  - SolidWorks
  - Flow Simulation
  - Finite Element Analysis
  - CAD
  - Technical Reporting

skills:
  - Aerodynamic Loading
  - Structural Analysis
  - Material Selection
  - Trade Studies

process_heading: "From aerodynamic load estimation to structural recommendation"

process:
  - title: "Define"
    detail: "Established the operating condition, support concepts, materials, and safety target."
  - title: "Model"
    detail: "Created a representative rear wing and two stanchion architectures in CAD."
  - title: "Simulate Flow"
    detail: "Estimated the resultant wing load at the selected vehicle speed."
  - title: "Transfer Load"
    detail: "Applied one consistent structural load case to every candidate design."
  - title: "Compare"
    detail: "Evaluated stress, displacement, safety factor, and modeled mass."
  - title: "Recommend"
    detail: "Identified the architecture and material tradeoffs that should guide redesign."

results_heading: "A common load case exposed the architecture-level tradeoff"

results:
  - value: "750 N"
    label: "CFD-estimated downforce at 45 m/s"
  - value: "800 N"
    label: "Structural comparison load"
  - value: "2"
    label: "Mounting architectures evaluated"
  - value: "3"
    label: "Material systems compared"
  - value: "≈50%"
    label: "Lower stress in the swan-neck concepts"
  - value: "Steel"
    label: "Only material meeting the 3.0 safety-factor target in both geometries"

featured: true
order: 6
card_title: "Aero-Structural Analysis"
card_category: "Engineering Analysis"
card_image: /images/aero_analysis_project/Baseline Flow.jpg
card_summary: >-
  CFD-informed FEA trade study of rear-wing support geometry, stiffness, mass, and safety margin.
card_tags:
  - CFD
  - FEA
  - Structures
  - Aerodynamics

previous_project:
  title: "ECE/MAE 148 Autonomous Vehicle"
  url: /final_project/
---

## The Engineering Question

Automotive rear-wing stanchions transfer aerodynamic downforce into the vehicle structure. A conventional support mounts beneath the wing and provides a short, direct load path. A swan-neck support reaches over the wing, preserving more of the lower aerodynamic surface but introducing a substantially longer moment arm.

The study asked:

> How do mounting architecture and material selection affect stress, stiffness, mass, and safety margin under a consistent aerodynamic load?

The comparison used three candidate materials:

- alloy steel
- 6061 aluminum
- carbon-fiber epoxy

A minimum factor of safety of **3.0** was selected to provide margin beyond the nominal aerodynamic load.

## Aerodynamic Load Definition

A representative rear-wing model was configured with a 1700 mm span, a 304 mm chord, and a 2° angle of attack. SolidWorks Flow Simulation predicted approximately **750 N of downforce at 45 m/s**, corresponding to roughly 100 mph.

The structural study used a slightly higher **800 N downward load** for every geometry and material. Holding this load constant isolated the effects of support architecture and material properties.

<figure class="project-figure project-figure--wide">
  <img src="{{ '/images/aero_analysis_project/wing-flow-analysis.jpg' | relative_url }}"
       alt="SolidWorks flow simulation of the representative automotive rear wing"
       loading="lazy">
  <figcaption>
    Flow simulation used to establish the common aerodynamic load transferred into the structural models.
  </figcaption>
</figure>

<div class="engineering-decision">
  <p class="engineering-decision__label">Analysis Decision</p>
  <p><strong>Use one CFD-informed load case for every structural candidate.</strong></p>
  <p>Applying the same 800 N load, mounting assumptions, and comparison criteria allowed differences in stress and displacement to be attributed to geometry and material rather than inconsistent loading.</p>
</div>

## Mounting Architecture

Both concepts used the same nominal 0.25 in plate thickness and comparable wing-interface geometry. This created a controlled comparison between the short, direct load path of the conventional support and the extended load path of the swan-neck design.

<div class="project-gallery__grid">
  <figure class="project-gallery__item project-gallery__item--contain">
    <img src="{{ '/images/aero_analysis_project/under-wing-concept.jpg' | relative_url }}"
         alt="Conventional under-wing rear spoiler stanchion model"
         loading="lazy">
    <figcaption><strong>Under-Wing Support</strong><span>Short load path with the wing mounted directly above the stanchion.</span></figcaption>
  </figure>
  <figure class="project-gallery__item project-gallery__item--contain">
    <img src="{{ '/images/aero_analysis_project/swan-neck-concept.jpg' | relative_url }}"
         alt="Swan-neck rear spoiler stanchion model"
         loading="lazy">
    <figcaption><strong>Swan-Neck Support</strong><span>Upper-surface mounting preserves the wing underside but increases the structural moment arm.</span></figcaption>
  </figure>
</div>

## Structural Analysis

Each configuration was evaluated using the same loading and mounting assumptions. The comparison tracked:

- von Mises stress
- resultant displacement
- minimum factor of safety
- modeled component mass

The simulations were intended as a comparative screening study. Material behavior was treated as linear elastic, the aerodynamic force was applied as a steady load, and vehicle-side loading and fatigue were outside the analysis scope.

### Results Summary

| Architecture and material | Stress (GPa) | Displacement (mm) | Minimum FOS | Modeled mass (g) |
|---|---:|---:|---:|---:|
| Under-wing · alloy steel | 0.09881 | 0.008442 | 6.3 | 1822.22 |
| Under-wing · 6061 aluminum | 0.09719 | 0.02587 | 0.57 | 638.96 |
| Under-wing · carbon-fiber epoxy | 0.1014 | 0.6442 | 0.0099 | 272.15 |
| Swan-neck · alloy steel | 0.04375 | 0.4425 | 14.0 | 5407.86 |
| Swan-neck · 6061 aluminum | 0.04505 | 1.346 | 1.2 | 1896.26 |
| Swan-neck · carbon-fiber epoxy | 0.03748 | 34.377 | 0.027 | 807.67 |

Only the alloy-steel versions satisfied the selected factor-of-safety target of 3.0. The aluminum swan-neck remained above a factor of safety of 1.0 under the nominal load, but it did not meet the design target.

## Architecture Tradeoff

The swan-neck concepts experienced approximately **50–63% less peak stress** than their under-wing counterparts. However, the longer curved load path made them far less stiff in the tested geometry: displacement was approximately **52 times greater**, and modeled mass was approximately **three times higher** for the same material.

<div class="project-gallery__grid">
  <figure class="project-gallery__item project-gallery__item--contain">
    <img src="{{ '/images/aero_analysis_project/under-wing-stress.jpg' | relative_url }}"
         alt="Finite element stress result for the alloy-steel under-wing stanchion"
         loading="lazy">
    <figcaption><strong>Under-Wing Stress</strong><span>Higher peak stress, but a short and comparatively stiff load path.</span></figcaption>
  </figure>
  <figure class="project-gallery__item project-gallery__item--contain">
    <img src="{{ '/images/aero_analysis_project/swan-neck-stress.jpg' | relative_url }}"
         alt="Finite element stress result for the alloy-steel swan-neck stanchion"
         loading="lazy">
    <figcaption><strong>Swan-Neck Stress</strong><span>Lower peak stress under the same applied load.</span></figcaption>
  </figure>
  <figure class="project-gallery__item project-gallery__item--contain">
    <img src="{{ '/images/aero_analysis_project/under-wing-displacement.jpg' | relative_url }}"
         alt="Finite element displacement result for the alloy-steel under-wing stanchion"
         loading="lazy">
    <figcaption><strong>Under-Wing Displacement</strong><span>Minimal deflection from the direct support geometry.</span></figcaption>
  </figure>
  <figure class="project-gallery__item project-gallery__item--contain">
    <img src="{{ '/images/aero_analysis_project/swan-neck-displacement.jpg' | relative_url }}"
         alt="Finite element displacement result for the alloy-steel swan-neck stanchion"
         loading="lazy">
    <figcaption><strong>Swan-Neck Displacement</strong><span>Greater deflection caused by the extended moment arm.</span></figcaption>
  </figure>
</div>

<div class="engineering-decision">
  <p class="engineering-decision__label">Engineering Recommendation</p>
  <p><strong>Use the alloy-steel under-wing concept as the feasible baseline for the tested geometry.</strong></p>
  <p>It met the safety-factor target while providing substantially lower displacement and mass than the steel swan-neck. A swan-neck concept would require section optimization, local reinforcement, or a hybrid construction before its potential aerodynamic benefit could justify the structural penalty.</p>
</div>

## Limitations and Next Iteration

The study established a useful screening comparison, but a production design would require additional analysis:

- quantify the aerodynamic difference between the two mounting locations rather than applying one wing load to both
- include transient, lateral, fatigue, and vehicle-interface load cases
- refine fixtures, contacts, mesh convergence, and local stress concentrations
- optimize the swan-neck section instead of holding plate thickness constant
- model carbon-fiber construction with laminate orientation and anisotropic failure criteria
- validate the selected architecture with physical load testing

These limitations are especially important for the carbon-fiber results. A generic linear material definition and von Mises-style comparison are not sufficient to design a real laminate, so those values should be treated as preliminary screening results rather than a final composite design.

## Engineering Perspective

The analysis demonstrated that material substitution cannot compensate for an inefficient load path. Although the swan-neck geometry reduced peak stress, its longer moment arm created a substantial stiffness and mass penalty in the unoptimized design. Coupling aerodynamic loading with structural simulation made that tradeoff visible early, before committing to detailed design or fabrication.

## Project Documentation

The complete individual project report contains the modeling assumptions, material data, simulation results, and original discussion.

[View the Aero-Structural Analysis Report]({{ '/files/aero_analysis_project/aero-structural-analysis-report.pdf' | relative_url }}){: .btn .btn--primary }
