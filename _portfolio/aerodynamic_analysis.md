---
layout: project-case-study
title: "Aero-Structural Analysis"
subtitle: "Coupled CFD and FEA evaluation of aerodynamic support structures"
date: 2024-08-06
collection: portfolio
permalink: /aerodynamic_analysis/

project_type: "Engineering Analysis · Aerodynamics and Structures"
hero_image: /images/aero_analysis_project/Baseline Flow.jpg
hero_summary: >-
  Used CFD-derived aerodynamic loads and finite element analysis to compare
  structural concepts, material choices, load paths, stress, deflection, and safety margin.

intro_title: "Aerodynamic loading translated into structural design decisions"
intro: >-
  The project connected flow analysis and structural simulation so that mounting
  concepts could be evaluated using consistent, flight-relevant loading rather
  than isolated structural assumptions.

role: "Primary Analyst"
timeline: "Summer 2024"
team: "Individual analysis project"
organization: "UC San Diego"
status: "Completed"

tools:
  - CFD
  - FEA
  - CAD
  - MATLAB
  - Python
  - Technical Reporting

skills:
  - Aerodynamic Loading
  - Structural Analysis
  - Load-Path Evaluation
  - Design Comparison

process:
  - title: "Problem Definition"
    detail: "Defined mounting concepts, materials, constraints, and evaluation criteria."
  - title: "CFD Setup"
    detail: "Established steady-state flow conditions and pressure loading."
  - title: "Load Extraction"
    detail: "Converted pressure results into structural force inputs."
  - title: "FEA Setup"
    detail: "Defined materials, constraints, meshes, and load cases."
  - title: "Comparison"
    detail: "Evaluated stress, deformation, safety factor, and load paths."
  - title: "Recommendation"
    detail: "Identified the geometry and material tradeoffs driving structural performance."

results:
  - value: "CFD → FEA"
    label: "Coupled analysis workflow"
  - value: "Multiple"
    label: "Geometries and materials compared"
  - value: "Critical"
    label: "Stress regions identified"
  - value: "Verified"
    label: "Acceptable stress and safety margins"
  - value: "Geometry"
    label: "Strongest driver of peak stress"
  - value: "Documented"
    label: "Technical assumptions and conclusions"

featured: true
order: 6
card_title: "Aero-Structural Analysis"
card_category: "Engineering Analysis"
card_image: /images/aero_analysis_project/Baseline Flow.jpg
card_summary: >-
  CFD and FEA used to evaluate aerodynamic structural performance.
card_tags:
  - CFD
  - FEA
  - Structures
  - Aerodynamics

previous_project:
  title: "ECE/MAE 148 Autonomous Vehicle"
  url: /final_project/
---

## The Challenge

The objective was to evaluate aerodynamic mounting concepts under externally applied aerodynamic loads.

Each design needed to maintain acceptable:

- stress
- deformation
- safety factor
- stiffness
- load-path efficiency
- manufacturability

The central challenge was connecting realistic aerodynamic loading to structural response in a consistent way.

## Aerodynamic Modeling

Computational fluid dynamics was used to estimate pressure distribution and resultant aerodynamic force under representative steady-state operating conditions.

The CFD model provided a common loading basis for all structural concepts.

The analysis emphasized comparative evaluation rather than transient aerodynamic phenomena.

## Structural Modeling

Finite element analysis was used to evaluate:

- von Mises stress
- deformation
- safety factor
- critical regions
- load transfer through the mounting geometry

Multiple material options and geometric configurations were compared.

<div class="engineering-decision">
  <p class="engineering-decision__label">Engineering Decision</p>
  <p><strong>Keep the aerodynamic load case consistent across every structural concept.</strong></p>
  <p>This isolated the effect of geometry, material, and load path instead of allowing inconsistent loading assumptions to dominate the comparison.</p>
</div>

## Assumptions and Boundary Conditions

The analysis used the following assumptions:

- CFD-derived forces represented equivalent steady-state external loads
- material behavior remained linear elastic
- constraints represented the intended mounting interfaces
- load cases were selected for direct design comparison
- local manufacturing details outside the primary load path were simplified

## Design Comparison

The analysis showed that mount geometry and load-path definition had a stronger effect on peak stress and deformation than material choice alone.

Changing material improved stiffness and strength, but poorly directed loads still produced concentrated stress.

This led to a design focus on:

- smoother load transfer
- reduced stress concentration
- better constraint placement
- more direct force paths
- targeted reinforcement

## My Contributions

- defined the analysis workflow
- created the aerodynamic model
- estimated pressure and resultant loading
- developed the structural model
- defined boundary conditions
- compared materials and geometries
- interpreted stress and deformation trends
- documented assumptions and conclusions

## Results

The project:

- estimated representative aerodynamic loads
- identified critical stress regions
- compared structural response across candidate designs
- quantified stiffness and safety-factor tradeoffs
- verified acceptable stress levels for selected configurations
- demonstrated the importance of geometry and load path

## Design Takeaways

The most important conclusion was that structural performance depended strongly on how the design carried load—not only on the nominal strength of the selected material.

Coupling CFD and FEA early in the process supported better tradeoffs between:

- strength
- stiffness
- weight
- geometry
- manufacturability
- safety margin

## Lessons Learned

Aero-structural simulation is most useful when the assumptions connecting the two domains are explicit. Reliable conclusions depend on traceable loads, realistic constraints, and consistent comparison criteria.
