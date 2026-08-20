---
title: "What LOTAR P520 Means for Engineering Practice — Now, Not After Ratification"
date: 2026-08-20
type: news
params:
  author: Hubertus Tummescheit
  summary: "P520 is still being drafted, but the credibility methodology it's built on — the Credible Simulation Process — already runs in automotive and beyond. Three things engineering leaders can act on before ratification."
  tags: ["LOTAR", "MBSE", "Modelica", "FMI", "SSP", "Compliance", "Credible Simulation Process"]
---

# What LOTAR P520 Means for Engineering Practice — Now, Not After Ratification

{{< logo-centered image="/images/LOTAR_logo.png" alt="LOTAR - Long Term Archiving and Retrieval" >}}

*This is Part 3 of a series — read [Part 1](/blog/lotar-520-simulation-models-are-evidence/) and [Part 2](/blog/lotar-520-layered-standards/) here.*

Standards take years to ratify, and P520 is no exception. The [LOTAR MBSE workgroup](https://lotar-international.org/lotar-workgroups/model-based-systems-engineering/)'s [Q3 2025 workshop](https://lotar-international.org/lotar-q3-2025-workshop-key-achievements/) in Seattle reported completion of the [AIA](https://www.aia-aerospace.org/)/[ASD-Europe](https://www.asd-europe.org/) Part 500 review and a white paper delivered to the Modelica conference community, alongside progress on related parts of EN/NAS 9300 like 9300-210 (released) and 9300-230/9300-205 (in ballot). Part 520 itself is still being drafted. That timeline is normal for an international standard with this scope, but it shouldn't be read as "nothing to do yet" — because the methodological core P520 is building on already exists, and it was never aerospace's alone.

That core is the [Credible Simulation Process (CSP)](https://setlevel.de/en/results/credible-simulation-process-framework), a framework [prostep ivip](https://www.prostep.org/en/projects/smart-systems-engineering-smartse-gb)'s Smart Systems Engineering (SmartSE) project group built to determine and document how much a given simulation result can be trusted — independent of industry. CSP didn't originate in aerospace: it's already running in automotive and autonomous-driving programs, and [prostep ivip's own 2024 white paper](https://www.prostep.org/fileadmin/prod-download/TechnicalPaper_Simulation-Credibility_2024_V8.1_v2.pdf) on it calls it explicitly "an international and cross-industry simulation credibility approach." It was developed through several German and European Research projects, among them the ITEA3 UPSIM Credibility Assessment Framework, grounding it. In an automotive context, it is the basis for the Modeling & Simulation SPICE® process model. P520 sits in that lineage: an aerospace-specific archiving layer on top of a credibility methodology that was never aerospace-specific.

**Three things engineering leaders can act on before ratification.**

*First: audit how your simulation models are actually packaged today.* If a model that fed a design decision only exists as a native file for one specific simulation tool and one specific version of it, you already have the exposure problem P520 is trying to solve — you just haven't been asked to prove it yet. Tool-independent packaging ([FMI](https://fmi-standard.org/), [SSP](https://ssp-standard.org/)) is the direction every relevant standard, in every industry referenced in this series, is converging on. Moving toward it now is not "getting ahead of aerospace regulation". It is closing a gap that already exists under [ISO 26262](https://www.iso.org/standard/68383.html), [EU MDR](https://eur-lex.europa.eu/eli/reg/2017/745/2024-07-09/eng), and the revised [Product Liability Directive](https://eur-lex.europa.eu/eli/dir/2024/2853/oj/eng), all of which can require you to reproduce or justify a historical engineering decision years after the fact.

*Second: treat provenance and decision context as a first-class deliverable, not an afterthought.* The hardest part of P520, by the LOTAR MBSE workgroup's own account, is the seam between the model-packaging standards (FMI/SSP) and the systems-engineering context standard [MoSSEC](https://www.iso.org/standard/72491.html) — because a model that runs but has lost the record of *why* it was run isn't useful evidence. You don't have to invent that record-keeping yourself: CSP already defines what a credibility record should contain — assumptions, verification and validation evidence, use history — and the [SSP Traceability](https://www.nafems.org/events/nafems/2026/the-ssp-traceability-standard-a-data-standard-supporting-the-credible-simulation-process-for-system-simulation-as-a-building-block-for-simulation-governance/) layered standard packages it on top of SSP and FMI in open, tool-agnostic form, so it travels with the model instead of living in a separate document that gets lost.

*Third: don't assume this stays in aerospace.* The core insight of this series is architectural, and CSP is the clearest proof of it: a credibility and archiving methodology built around one industry's needs is already running in a second (automotive) and feeding a third (via UPSIM and Modeling & Simulation SPICE®) — well before any of them had a mandate to use it. LOTAR P520 is aerospace's packaging of that same underlying idea — on top of generic [Modelica Association](https://modelica.org) standards (FMI, SSP, SSP-Traceability) that other industries already use for other purposes. In the same way [ASAM](https://www.asam.net/) built [FMI-LS-XCP](https://fmi-standard.org/news/2024-12-03-fmi-ls-xcp-v1.0.0/) and [FMI-LS-BUS](https://fmi-standard.org/news/2025-07-21-fmi-ls-bus-v1.0-release/) as an automotive layer on the same base for virtual ECU testing. Automotive, medical device, and energy engineering leaders watching this space now will have a head start when — not if — their own industry bodies look for a ready-made answer to the same "can we trust and still open this model in 20 years" problem.

This work has direct roots in the 2021 paper "Modelica, FMI and SSP for LOTAR of Analytical mBSE Models: First Implementation and Feedback," prototyped in [Modelon Impact](https://www.modelon.com/modelon-impact/). It's a thread I'm still pulling on: I'm a co-author again on [the latest installment](https://ecp.ep.liu.se/index.php/modelica/article/view/1360), "The Fundamental Modeling Practices and Specifications to support the Preservation and Reuse of Analytical Simulations," with Mark Williams, Ajaykumar Mst, and Jose María Alvarez-Rodríguez at the 2025 International Modelica & FMI Conference, which reports on the maturity of the LOTAR draft standards and the new FMI/SSP layered standards — including SSP Traceability — since that first paper. As a member of the Modelica Association board, the FMI steering committee, and the NAFEMS-INCOSE Systems Modeling & Simulation Working Group, I have presented on SSP Traceability and the Credible Simulation Process in NAFEMS's 2026 webinar series — the same CSP foundation this article just walked through.

**Sources**
- [LOTAR Q3 2025 Workshop – Key Achievements](https://lotar-international.org/lotar-q3-2025-workshop-key-achievements/)
- [The Fundamental Modeling Practices and Specifications to support the Preservation and Reuse of Analytical Simulations — International Modelica & FMI Conference 2025](https://ecp.ep.liu.se/index.php/modelica/article/view/1360)
- [LOTAR Model-Based Systems Engineering Workgroup](https://lotar-international.org/lotar-workgroups/model-based-systems-engineering/)
- [Aerospace Industries Association (AIA)](https://www.aia-aerospace.org/)
- [AeroSpace and Defence Industries Association of Europe (ASD-Europe)](https://www.asd-europe.org/)
- [ISO 10303-243:2021 — MoSSEC](https://www.iso.org/standard/72491.html)
- [Credible Simulation Process Framework — SET Level](https://setlevel.de/en/results/credible-simulation-process-framework)
- [prostep ivip: "Guard Rails for Simulation Credibility Standards and Recommendation" White Paper (2024)](https://www.prostep.org/fileadmin/prod-download/TechnicalPaper_Simulation-Credibility_2024_V8.1_v2.pdf)
- [prostep ivip SmartSE Recommendation V4 (2025)](https://www.prostep.org/fileadmin/prod-pay-download-8c1d/PSI11_RecV4_Final_aw.pdf)
- [NAFEMS: The SSP Traceability Standard — webinar series](https://www.nafems.org/events/nafems/2026/the-ssp-traceability-standard-a-data-standard-supporting-the-credible-simulation-process-for-system-simulation-as-a-building-block-for-simulation-governance/)

For more info, please fill in the [contact form](/Company/) or {{< appointment >}}
