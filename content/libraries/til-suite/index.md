---
title: "TIL Suite — Thermodynamic Simulation Library"
date: 2026-05-07
description: >
  Modelica library for thermodynamic system simulation — heat pumps, HVAC,
  battery cooling, refrigeration circuits and more — by our partner TLK-Thermo,
  available in Dymola and Modelon Impact.
draft: false
---

## TIL Suite — Thermodynamic Simulation Library

{{< content-container >}}
{{% block-left-aligned %}}
The [TIL Suite](https://tlk-energy.de/en/software/til-suite) is a
[Modelica](https://modelbased.cloud/tools/modelica/) library developed by our
partner [TLK-Thermo](https://tlk-thermo.com/) that helps you understand and
optimize thermodynamic systems. Through simulation and analysis with TIL you
will find answers to complex engineering questions — study the defrosting
behaviour of heat pumps, design control concepts for ventilation systems, or
optimize the cooling of a battery system.

TIL Suite runs in [Dymola](https://www.3ds.com/products/catia/dymola) and
[Modelon Impact](https://modelbased.cloud/tools/modelica/), and is
available through Model Based Innovation as part of our libraries offering.
We at [TLK Energy](https://tlk-energy.de/en) actively participate in the
development of the library and use TIL Suite in service projects across a
wide range of thermal applications.

> *"At Danfoss, we use the TIL Suite model library in Dymola and Modelon
> Impact to develop our products more effectively. TIL Suite helps us design
> components for heat pumps for residential and industrial use, as well as
> innovative cooling solutions for data centers."*
> — Enno Vredenborg, Senior Manager Digital Solutions at Danfoss
{{% /block-left-aligned %}}
{{< block-left-aligned >}}
{{< responsive-image src="images/til-suite/til-suite-hero.webp" alt="TIL Suite system model on a laptop" >}}
{{< /block-left-aligned >}}
{{< /content-container >}}

---

### What You Can Study with TIL Suite

{{< content-container >}}

{{< block-centered icon="/images/til-suite/icon-usability.svg" alt="Usability icon" title="Design and Comparison">}}
Design and comparison of different system variants to find the optimal
configuration early in the project.
{{< /block-centered >}}

{{< block-centered icon="/images/til-suite/icon-reliability.svg" alt="Reliability icon" title="Transient Analysis">}}
Investigation of transient plant behaviour under realistic varying boundary
conditions and load profiles.
{{< /block-centered >}}

{{< block-centered icon="/images/til-suite/icon-support.svg" alt="Support icon" title="Control Development">}}
Development and testing of control strategies in a risk-free simulation
environment before hardware integration.
{{< /block-centered >}}

{{< block-centered icon="/images/til-suite/icon-usability.svg" alt="Optimization icon" title="Parameter Studies">}}
Parameter studies, sensitivity analyses and identification of optimization
potentials across the design space.
{{< /block-centered >}}

{{< /content-container >}}

---

### Example Applications

{{< content-container >}}
{{< block-left-aligned >}}
{{< responsive-image src="images/til-suite/heatpump-model.png" alt="CO2 heat pump model in TIL Suite" >}}
{{< /block-left-aligned >}}
{{% block-left-aligned %}}

#### Heat Pump

A CO2 cycle representing a typical air-to-water heat pump for a building, with
a tube bundle gas cooler on the high-pressure side and a finned-tube evaporator
on the low-pressure side, plus an internal heat exchanger. The system can be
simulated over different time periods, with constant or varying ambient
conditions. Results are visualized in a p-h diagram using
[DaVE](https://tlk-thermo.com/index.php/en/software-products/dave) showing the
complete thermodynamic cycle.

{{% /block-left-aligned %}}
{{< /content-container >}}

{{< content-container >}}
{{< block-left-aligned >}}
{{< responsive-image src="images/til-suite/hvac-model.png" alt="TIL model of a ventilation system" >}}
{{< /block-left-aligned >}}
{{% block-left-aligned %}}

#### Ventilation System

A ventilation system model consisting of fans, heat recovery, adiabatic
recooler, droplet separators, coolers, dehumidifiers, air heaters and steam
humidifiers. The model can be tested under variable operating conditions
(weather data) and different control concepts can be compared. Results are
shown in an hx-diagram demonstrating conditioning performance for both summer
and winter conditions.

{{% /block-left-aligned %}}
{{< /content-container >}}

{{< content-container >}}
{{< block-left-aligned >}}
{{< responsive-image src="images/til-suite/battery-model.png" alt="TIL model of an electric car battery cooling circuit" >}}
{{< /block-left-aligned >}}
{{% block-left-aligned %}}

#### Battery Cooling

A model of an electric car with an attached cooling circuit connecting battery,
vehicle interior and surroundings. At low ambient temperatures the battery waste
heat heats the interior; at high summer temperatures a three-way valve switches
to cool the battery against outside air. The model supports dimensioning of heat
exchangers and tuning of pump and fan controls, validated against the HFET
driving cycle.

{{% /block-left-aligned %}}
{{< /content-container >}}

---

### Supported System Types

TIL Suite can be used to model a wide range of thermal systems:

{{< content-container >}}
{{% block-left-aligned %}}
- Refrigeration circuits
- Heat pump systems
- Hydraulic networks
- Fuel cell and hydrogen systems
- Clausius-Rankine processes
- Adsorption systems and hydrogen filling stations
- Ventilation and air-conditioning systems
{{% /block-left-aligned %}}
{{< /content-container >}}

---

### Package Contents

TIL Suite is a modular software package. The base version ships with three
components and can be extended with optional add-on libraries for specific
domains.

{{< content-container >}}

{{< block-centered icon="/images/til-suite/til-suite-logo.svg" alt="TIL Suite logo" title="TIL — Included">}}
Model library for thermal components and systems. Incorporates experience from
numerous projects and test bench experiments.
{{< /block-centered >}}

{{< block-centered icon="/images/til-suite/tilmedia-logo.svg" alt="TILMedia logo" title="TILMedia — Included">}}
Thermophysical substance property library. Enables simulations with air, water
and various refrigerants quickly and accurately.
{{< /block-centered >}}

{{< block-centered icon="/images/til-suite/tilfilereader-logo.svg" alt="TILFileReader logo" title="TILFileReader — Included">}}
Imports tabular data from CSV and Dymola result files — integrate measurement
data or product specifications directly into simulations.
{{< /block-centered >}}

{{< /content-container >}}

#### Optional Add-On Libraries

{{< content-container >}}

{{< block-centered icon="/images/til-suite/til-addon.svg" alt="Add-on icon" title="Hydrogen">}}
Models of fuel cells, electrolysis, liquefaction and refueling stations.
{{< /block-centered >}}

{{< block-centered icon="/images/til-suite/til-addon.svg" alt="Add-on icon" title="Automotive">}}
Models of vehicle cabins, air conditioning and motor cooling circuits.
{{< /block-centered >}}

{{< block-centered icon="/images/til-suite/til-addon.svg" alt="Add-on icon" title="Adsorption">}}
Models for gas purification, drying, temperature and pressure swing processes.
{{< /block-centered >}}

{{< block-centered icon="/images/til-suite/til-addon.svg" alt="Add-on icon" title="Heat Storage">}}
Water tanks with different heat exchanger configurations.
{{< /block-centered >}}

{{< block-centered icon="/images/til-suite/til-addon.svg" alt="Add-on icon" title="PCM Storages">}}
Phase change material models and heat exchanger variants for latent heat storage.
{{< /block-centered >}}

{{< block-centered icon="/images/til-suite/til-addon.svg" alt="Add-on icon" title="High Dynamic">}}
For robust simulations with switching processes and transient boundary conditions.
{{< /block-centered >}}

{{< /content-container >}}

---

### Why TIL Suite

{{< content-container >}}

{{< block-centered icon="/images/til-suite/icon-usability.svg" alt="Usability icon" title="Usability">}}
Open and modifiable Modelica code that can be easily customized and integrated
into your own projects and toolchains.
{{< /block-centered >}}

{{< block-centered icon="/images/til-suite/icon-reliability.svg" alt="Reliability icon" title="Reliability">}}
Continuously developed code that has been successfully used in industry for
years, validated against real measurement data.
{{< /block-centered >}}

{{< block-centered icon="/images/til-suite/icon-support.svg" alt="Support icon" title="Support">}}
You are not alone. TLK Energy and Model Based Innovation support customers with
training, video chats and individual consulting services.
{{< /block-centered >}}

{{< /content-container >}}

---

### Resources

| Resource | Link |
| --- | --- |
| Product website | [tlk-energy.de/en/software/til-suite](https://tlk-energy.de/en/software/til-suite) |
| TIL Adsorption add-on | [tlk-energy.de/en/software/til-suite/adsorption](https://tlk-energy.de/en/software/til-suite/adsorption) |
| Hydrogen systems add-on | [tlk-energy.de/en/software/til-suite/hydrogen-systems](https://tlk-energy.de/en/software/til-suite/hydrogen-systems) |
| Modelica training | [tlk-energy.de/en/modelica-training](https://tlk-energy.de/en/modelica-training) |
| Contact / get a quote | [Schedule an appointment](https://calendly.com/welcome-to-tlk-energy/30min) |
| Developer | [TLK-Thermo GmbH](https://tlk-thermo.com/) |
| Sold by | [TLK Energy GmbH](https://tlk-energy.de/en) |
