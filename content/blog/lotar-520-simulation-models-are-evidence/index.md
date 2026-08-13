---
title: "Your Simulation Models Are Evidence. Do You Know If They'll Survive to Be Used as Such?"
date: 2026-08-06
type: news
params:
  author: Hubertus Tummescheit
  summary: "Simulation models used in certification need to remain usable for decades. LOTAR's Part NAS9300-520 — and a growing web of product liability, medical device, and functional safety regulation — make model archiving a legal issue, not just an engineering one."
  tags: ["LOTAR", "MBSE", "Modelica", "Compliance", "Aerospace"]
---

## Your Simulation Models Are Evidence. Do You Know If They'll Survive to Be Used as Such?

{{< logo-centered image="/images/LOTAR_logo.png" alt="LOTAR - Long Term Archiving and Retrieval" >}}

An aircraft type-certified today can remain in commercial service for 30–50 years. The simulation models that helped certify it — flight control laws, hydraulic and thermal system models, structural load cases — need to remain usable for just as long: openable, re-runnable, and trustworthy, on hardware and software that hasn't been invented yet.

That's the problem [LOTAR](https://lotar-international.org/lotar-workgroups/model-based-systems-engineering/) (LOng Term Archiving and Retrieval) exists to solve. It's an established program in aerospace and defense, already covering CAD geometry, PDM data, and electrical harness definitions. The newer front is simulation and analysis models — and specifically, the [Model-Based Systems Engineering (MBSE) workgroup's Part 520](https://lotar-international.org/lotar-workgroups/model-based-systems-engineering/), which targets analytical models described by specification or executable code: differential, algebraic, and discrete equations. In practice, that means Modelica-class models.

### Why Frame This as a Legal and Business Issue, Not Just an Engineering One

The scenarios that make this concrete are business-driven, not technical: a part needs re-certifying twenty years after entry into service; an in-service incident needs investigating; a derivative product needs evaluating against the original design intent; a supplier goes out of business and the OEM has to answer questions the supplier used to own. In each case, the question isn't "do we still have the report" — it's "can we still open, trust, and re-run the model that produced it." For most organizations today, the honest answer is no. The model lived on one engineer's laptop, in one tool version, following conventions nobody wrote down.

### This Is Not an Aerospace-Only Exposure

Aerospace has unusually long asset lifecycles, which is why it moved first. But the legal and regulatory logic generalizes cleanly:

- The EU's [Product Liability Directive](https://eur-lex.europa.eu/eli/dir/2024/2853/oj/eng) sets a general 10-year expiry on liability claims from the date a product was placed on the market — extended to 25 years for injuries with long latency periods. That clock runs regardless of industry, and it runs against whatever evidence a manufacturer can produce, model included.
- The EU [Medical Device Regulation (MDR)](https://eur-lex.europa.eu/eli/reg/2017/745/2025-01-10/eng) requires manufacturers to retain technical documentation — including verification and validation data — for 10 years after the last device is placed on the market, and 15 years for implantable devices. Simulation and analysis increasingly form part of that verification evidence.
- [ISO 26262](https://www.iso.org/publication/PUB200262.html), the automotive functional safety standard, requires a safety case with unbroken, bidirectional traceability between hazards, requirements, and verification evidence across the full item lifecycle. Where that evidence is a simulation model rather than a static document, the traceability requirement quietly becomes an archiving requirement too. ISO 26262 sits in a family of sector-specific derivatives of [IEC 61508](https://www.iec.ch/functional-safety), the generic functional safety standard — the same pattern repeats in rail ([EN 50126/50128/50129](https://ldra.com/en-5012x/)) and process industries ([IEC 61511](https://en.wikipedia.org/wiki/IEC_61511)).

None of these standards currently spell out "archive your Modelica model in a tool-neutral, metadata-rich package for 20 years." But the obligations they do spell out — produce evidence on demand, keep it traceable, retain it for a defined period — are very hard to satisfy if the model underneath the evidence has quietly become unreadable.

### The Gap Organizations Don't See Until They're Asked

Most simulation teams optimize for getting today's project done: fastest tool, most convenient file format, tribal knowledge instead of written assumptions. That's rational under normal delivery pressure. It becomes a liability the day someone outside the original team — a regulator, a lawyer, a new engineer twenty years later — needs to open that model and trust what it says.

The next article in this series covers what LOTAR's Part 520 actually specifies technically, and why the same architecture is directly reusable outside aerospace.

For more info, please fill in the [contact form](/Company/) or {{< appointment >}}
