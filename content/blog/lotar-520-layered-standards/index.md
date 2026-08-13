---
title: "LOTAR NAS9300-520 Isn't a New Simulation Standard. It's a New Layer on Standards You Probably Already Use."
date: 2026-08-12
type: news
params:
  author: Hubertus Tummescheit
  summary: "LOTAR's Part 520 doesn't reinvent simulation exchange — it adds an archiving and retrieval layer on top of Modelica, FMI, and SSP, following the same layered-standards pattern already used elsewhere in the industry."
  tags: ["LOTAR", "MBSE", "Modelica", "FMI", "SSP", "Compliance"]
---

## LOTAR NAS9300-520 Isn't a New Simulation Standard. It's a New Layer on Standards You Probably Already Use.

{{< logo-centered image="/images/LOTAR_logo.png" alt="LOTAR - Long Term Archiving and Retrieval" >}}

*This is Part 2 of a series — read [Part 1](/blog/lotar-520-simulation-models-are-evidence/) here.*

A common misconception about LOTAR's Part 520 is that it's introducing a new way to build or exchange simulation models. It isn't. It's introducing a new way to archive and retrieve models that are already built on standards most simulation engineers use today: [Modelica](https://modelica.org/) for the equations, and [FMI](https://fmi-standard.org/) (Functional Mock-up Interface) and [SSP](https://ssp-standard.org/) (System Structure and Parameterization) for packaging and composing them into systems.

FMI and SSP are [Modelica Association](https://modelica.org/) standards — open, royalty-free, and deliberately industry-agnostic. They're used in automotive, aerospace, industrial equipment, buildings, and energy. That breadth is the point: nobody has to reinvent model exchange for their sector.

### The "Layered Standards" Pattern

What the Modelica Association pioneered instead is a layered-standards architecture: a stable core (FMI, SSP) plus optional, industry-specific layers built on top for particular use cases. Automotive has already done this in partnership with [ASAM](https://www.asam.net/) — [FMI-LS-BUS](https://fmi-standard.org/news/2025-07-21-fmi-ls-bus-v1.0-release/) for network/bus simulation, [FMI-LS-XCP](https://fmi-standard.org/news/2024-12-03-fmi-ls-xcp-v1.0.0/) for measurement and calibration protocol support, both released to serve virtual-ECU workflows that ISO 26262-driven development increasingly depends on.

LOTAR's Part 520 is the same architectural move, aimed at a different problem: instead of a layer for running simulations together, it's a layer for archiving and retrieving them decades later. Structurally, that means defining, on top of Modelica/FMI/SSP, a manifest of metadata that doesn't naturally exist in those formats: model usage and intent, validity ranges, and — critically — an explicit statement of what physical phenomena the model represents and what it deliberately neglects. Rather than inventing this from scratch, the workgroup deliberately built on prior art — prostep ivip's [Credible Simulation Process](https://www.prostep.org/en/projects/smart-systems-engineering-smartse-1) and NASA's [HDBK-7009B](https://standards.nasa.gov/standard/nasa/nasa-std-7009) guidance on model and simulation credibility — both to move faster and to align with tooling that already exists. A model that opens perfectly in 2045 is still useless if nobody encoded what it was actually good for.

### Where It Gets Hard: Connecting to the Rest of the Digital Record

An archived model can't just sit as a self-contained, orphaned file — it needs to connect back to the requirements it satisfies, the verification results that used it, the systems-engineering models around it, and the bill of materials it belongs to. That integration layer matters much more for the other parts of the [LOTAR 500-series](https://lotar-international.org/lotar-workgroups/model-based-systems-engineering/) — Part 510/515 (requirements) and Part 530 (architecture models) — than it does for Part 520 itself, whose main job is packaging the model. [MoSSEC (ISO 10303-243)](https://www.iso.org/standard/72491.html), the STEP standard for modeling and simulation information in a systems-engineering context, is one of the standards in play for that broader linking job, but it's a supporting piece rather than the center of Part 520's own scope.

The LOTAR working group asked Modelon to build a first implementation of the archiving package end to end in [Modelon Impact](https://www.modelon.com/modelon-impact/), presented at the [2021 Modelica Conference](https://ecp.ep.liu.se/index.php/modelica/article/view/181) and refined through follow-on work at the [2023](https://ecp.ep.liu.se/index.php/modelica/issue/view/83) and [2025](https://ecp.ep.liu.se/index.php/modelica/issue/view/105) conferences. I am currently building on top of that, adding [SSP-Traceability](https://github.com/modelica/ssp-ls-traceability) and the draft LOTAR 520 schema. The finding that mattered most: Modelica, FMI, and SSP were never designed to hook automatically into the rest of the digital product record — requirements traceability, SE models, BOM structures. That stitching has to be deliberately engineered, and it remains open work across the whole LOTAR 500-series family, not something Part 520 alone can solve.

### Why This Matters Outside Aerospace

The reusable part isn't any one manifest schema — it's the architecture: a generic simulation-interchange base, an industry-specific archiving layer on top, loosely connected to whatever systems-engineering or quality record the industry already keeps. Automotive, with ISO 26262's traceability demands on virtual ECU and simulation-based verification, is arguably one step from needing exactly this. Medical device and process industries, with their own retention and traceability regimes, are in a similar position — most of them just haven't had a workgroup sit down and write it yet.

Next in this series: what to actually change in day-to-day modeling practice, regardless of which industry's version of this standard eventually lands.

For more info, please fill in the [contact form](/Company/) or {{< appointment >}}
