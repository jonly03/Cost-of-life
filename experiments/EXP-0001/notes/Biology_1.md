# Biology_1 — EXP-0001 physiological dependency graph

Status: **proposed / ready for evidence mapping and attack**

This document is the Biology & Human Requirements Desk's first-order synthesis for EXP-0001. The durable atomic propositions are BIO-0001 through BIO-0014 in `claims/registry.yaml`.

## Boundary

The subject is a living human organism at t0 with functioning baseline systems and pre-existing physiological inventories. The observation window is 24 hours. This boundary is deliberately different from a lifetime provisioning model.

## First-order graph

```text
Viability / physiological function
|
+-- Cellular energy availability [BIO-0001]
|   +-- Oxygen delivery [BIO-0002]
|   |   +-- viable external respiratory environment [BIO-0014]
|   |   +-- ventilation / gas exchange capacity
|   |   +-- circulation / perfusion [BIO-0004]
|   +-- Metabolic substrate availability [BIO-0007]
|       +-- endogenous glycogen/adipose/protein at t0
|       +-- exogenous energy replenishment over context-dependent horizon
|
+-- Acid-base / gas homeostasis
|   +-- CO2 elimination [BIO-0003]
|   +-- renal regulation [BIO-0012]
|
+-- Fluid / electrolyte homeostasis
|   +-- body-water stock and osmolality [BIO-0005]
|   +-- electrolyte stocks/gradients [BIO-0006]
|   +-- renal regulation and excretion [BIO-0012]
|
+-- Material / nutrient maintenance over time
|   +-- indispensable amino acids [BIO-0008]
|   +-- essential fatty acids [BIO-0009]
|   +-- heterogeneous micronutrient stocks [BIO-0010]
|
+-- Thermal homeostasis [BIO-0011]
|   +-- metabolic heat
|   +-- water availability / evaporative capacity
|   +-- circulation
|   +-- viable external environment / conditional protective mechanisms [BIO-0014]
|
+-- Waste processing and removal [BIO-0012]
|   +-- CO2 removal [BIO-0003]
|   +-- nitrogen processing / renal solute excretion
|
+-- Sleep / recovery state [BIO-0013]
    +-- primarily functional-performance and long-term-health layer in Biology_1
```

## Requirement / Consumption / Replenishment discipline

**Requirement** means a condition, process, capacity, flow or state that must be available or maintained for the stated outcome. It does not imply that a market good must be acquired in the observation window.

**Consumption/use** describes physiological throughput or depletion. Oxygen is continuously taken up; substrates are oxidized; water is lost; ATP turns over. These quantities are not automatically external replenishment quantities.

**Replenishment** describes restoration of an inventory from outside the organism. Replenishment timing depends on the size/state of the inventory at t0, ongoing losses/usage, synthesis/recycling, and the outcome threshold being protected.

## Inventory Blindness cases explicitly rejected

1. **Energy:** 24-hour metabolic expenditure is not identical to 24-hour food intake. Endogenous stores can bridge the observation window in appropriately scoped people.
2. **Water:** observed daily water loss creates a replenishment liability, but neither total-water Adequate Intake nor a population average is a universal survival minimum for the next 24 hours.
3. **Electrolytes:** regulated serum concentration is not equivalent to total-body inventory, and same-day turnover is not necessarily same-day dietary requirement.
4. **Protein/amino acids:** indispensable amino acids are long-run exogenous requirements, but tissue turnover and amino-acid pools break a simple daily input=use identity.
5. **Essential fatty acids:** essentiality does not imply daily ingestion.
6. **Micronutrients:** stores and turnover vary radically by nutrient; a daily multivitamin-style representation would be biologically false.
7. **Sleep:** recommended sleep duration is not automatically a survival threshold.

## Threshold layers

Biology_1 preserves five distinct outcome classes where evidence permits:

- **Survival:** continued organismal viability.
- **Physiological stability:** maintenance of regulated internal states without clinically significant destabilization.
- **Functional performance:** ability to perform cognitive/physical functions.
- **Long-term health:** avoidance of deficiency/disease risk over longer horizons.
- **Comfort:** subjective or nonessential thermal/behavioral adequacy.

A number valid for one layer must not silently migrate to another.

## Population/modifier rule

No universal reference human is instantiated in Biology_1. Quantitative downstream models must parameterize relevant modifiers, especially age/life stage, body mass and composition, activity, health, climate/thermal load, altitude, and pregnancy/lactation. Sex is retained where physiology or reference data make it relevant.

## Evidence posture

Biology_1 deliberately leaves `supported_by` empty. The Biology desk used authoritative physiology and dietary-reference literature to scope the propositions, but REF-* ownership and formal provenance mapping belong to the Librarian / Reference & Evidence Desk. Claims remain **proposed** until that mapping occurs.

High-priority evidence families for Librarian mapping include:
- respiratory physiology and the oxygen-delivery cascade;
- cellular/whole-body energetics and fasting substrate use;
- National Academies dietary reference work on water/electrolytes and nutrient essentiality;
- renal fluid/electrolyte/acid-base physiology;
- thermoregulation and environmental physiology;
- sleep-duration consensus plus experimental sleep-loss literature.

## Biology_2 targets after attack

- Decompose BIO-0010 into nutrient-specific stock/horizon claims where material to the model.
- Establish defensible quantitative state variables and ranges without converting reference intakes into minima.
- Add special-population branches where the healthy-adult reserve assumption fails.
- Clarify environmental hazard dimensions (oxygen partial pressure, heat/cold, contaminants, pressure).
- Resolve how sanitation/external waste handling enters the graph without confusing internal excretion with infrastructure.
- Incorporate REF-* mappings and answer RT-* challenges.
