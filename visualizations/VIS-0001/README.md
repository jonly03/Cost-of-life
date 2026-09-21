# VIS-0001 — The 24-Hour Human System

**Experiment:** EXP-0001  
**Desk:** Design & Visualization  
**Status:** proposed / ready for Director review  
**Publication status:** internal only — do not publish externally

## Purpose

VIS-0001 translates Scientific Core v0.1 into a public-facing visual explanation without converting the science into a flat list of daily quantities.

The core proposition is:

> A human organism is an open physiological system. During a 24-hour observation window, viability depends on flows, stocks, bounded states, processes, capacities, environmental conditions, and externally mediated access operating on different timescales.

The graphic therefore separates:

- **Requirement** — what must remain true for a declared outcome;
- **Consumption** — use, transformation, or depletion of a defined input or stock;
- **Replenishment** — restoration of an inventory from outside its declared boundary.

It also makes the anti-calendar rule explicit:

> **Used during 24 hours does not imply externally replenished during those same 24 hours.**

## Artifacts

- `VIS-0001-primary.svg` — primary system visualization.
- `VIS-0001-inventory-blindness.svg` — supporting stock-flow visual explaining Inventory Blindness.
- `VIS-0001-legend.svg` — reusable graphical grammar.
- `scientific-ambiguities.md` — ambiguities and publication-audit findings discovered while visualizing.

## Primary visual architecture

The primary artifact is organized around the **organism boundary**, not around product categories.

### Outside the boundary

The outer field represents the external world. It includes:

- environmental conditions such as breathable atmosphere and thermal conditions;
- accessible external resources such as preformed water and metabolic substrate;
- delivery/access mechanisms where relevant;
- receiving environment for outputs such as CO2, heat, water loss, and renal/fecal waste.

The environmental field is deliberately open-ended. It is **not** labeled as a complete set of all hazards.

### Crossing the boundary

Solid arrows represent flows that cross the organism boundary. Examples are intentionally qualitative:

- oxygen access / inflow;
- conditional preformed water and nutrient input;
- CO2 output;
- water and waste losses;
- heat exchange.

No universal daily quantity is shown.

### Inside the boundary

The internal grammar distinguishes four non-interchangeable object classes:

- **Stocks** — accumulated quantities such as body water, glycogen/adipose substrate, whole-body electrolyte inventories, and canonical body-protein/tissue inventory.
- **States** — regulated conditions such as osmolality/hydration state, compartment electrolyte gradients, and core thermal state.
- **Processes** — transformations and transport such as ATP turnover/metabolism, circulation, gas exchange, renal processing, and sleep/recovery.
- **Capacities** — abilities that constrain processes, such as respiratory, cardiovascular, renal, and thermoregulatory capacity.

Stocks can buffer flows. States can remain viable while stocks change. Processes can be continuously required without being commodities. Capacities can constrain viability without being consumed.

### Timescale ribbon

A bottom ribbon distinguishes the **24-hour observation window** from dependency-specific replenishment horizons.

It intentionally uses qualitative labels:

- seconds-to-minutes / effectively continuous for sustained oxygen access;
- continuous regulation/process for metabolism, circulation, gas exchange, and heat balance;
- hours-to-days or context-dependent for body-water replenishment;
- variable or unresolved for several nutrient depletion/replenishment horizons.

Unknown horizons are shown as unresolved rather than converted into daily numbers.

## Inventory Blindness visual

The supporting artifact contrasts an invalid inference:

`observed use or loss -> therefore same-window external replacement`

with a stock-aware balance family:

`later stock = initial stock + external inputs + internal production - outputs/use +/- internal transfers consistent with the declared boundary`

This is a generic stock-flow grammar derived from DATA-0001/Data_2, not a claim that every physiological variable obeys one identical scalar equation.

The figure uses water as a concrete example because Scientific Core v0.1 explicitly distinguishes:

- initial body-water stock;
- preformed external water;
- metabolic water produced from substrate oxidation;
- losses.

Metabolic water is visually tied back to substrate oxidation so it cannot be mistaken for an independent external resource.

## Mapping to canonical concepts

| Visual element | Canonical concept |
|---|---|
| organism outline | EXP-0001 declared system boundary and t0 initial conditions |
| reservoir shape | TERM-0006 Stock; BIO-0005, BIO-0006, BIO-0007/0008; DATA-0001, DATA-0003, DATA-0005, DATA-0006 |
| bounded-state target | TERM-0008 State; BIO-0005, BIO-0006, BIO-0011 |
| process capsule | TERM-0009 Process; BIO-0001, BIO-0003, BIO-0004, BIO-0012, BIO-0013 |
| capacity bracket | TERM-0010 Capacity; BIO-0002, BIO-0004, BIO-0011 |
| crossing arrow | TERM-0007 Flow |
| environmental field | TERM-0017 Environmental Condition; BIO-0002, BIO-0011, BIO-0014; DATA-0004, DATA-0007 |
| dashed unknown marker | unresolved parameter / incomplete hazard surface |
| timescale ribbon | TERM-0004 Replenishment plus observation-window vs replenishment-horizon rule |
| R / C / Rp semantic strip | TERM-0002 Requirement; TERM-0003 Consumption; TERM-0004 Replenishment |
| inventory-blindness warning | TERM-0001 Inventory Blindness |

## Scientific guardrails encoded in the design

The visuals intentionally do **not**:

- display a universal calorie, water, oxygen, electrolyte, sleep, or nutrient number;
- use RDA/AI/reference values as survival minima;
- imply all essential nutrients must be ingested every day;
- duplicate body protein as separate energy and amino-acid reserves;
- treat body protein as consequence-free reserve;
- count metabolic water as an independent external resource;
- show CO2 or renal waste as resources consumed;
- label shelter/housing as a universal biological requirement;
- depict the environmental hazard model as exhaustive;
- turn unresolved thresholds or horizons into visually precise boundaries.

## Design rationale

The visual grammar is built for later extension into resource, infrastructure, economic, and PEOM layers.

The same diagram can eventually be expanded outward:

`organism -> access/delivery -> resource -> infrastructure -> production -> cost/price`

without changing the meaning of the physiological layer. This protects the project from a common category error: replacing a biological dependency with a particular commercial product too early.

The visual style avoids anatomical realism. The organism is treated as a **system boundary with typed internal objects and boundary-crossing relations**, which is closer to the conceptual discovery of Wave 1 and more reusable across later waves.

## Post-reconciliation refresh — EF-PUB-0001 resolved

During initial VIS-0001 development, the Design & Visualization Desk independently identified the canonical BIO registry inconsistency later tracked as **EF-PUB-0001**. That discovery remains part of the durable design history.

The canonical BIO registry has since been reconciled on `main` and the repair passed Biology reconciliation, Librarian provenance verification, and Red Team canonical-consistency/mechanical verification before integration.

### Visual audit result

The stale registry **did not drive the core visual architecture**. VIS-0001 had already followed the accepted Biology_2/Data_2/RedTeam_2 semantics rather than copying stale registry clauses. No structural redesign is required.

Three targeted clarity corrections were made after reconciliation:

1. **Electrolytes** — the stock label now says **whole-body electrolytes**, while the state label says **compartment gradients**, making the stock/state/boundary distinction explicit.
2. **Amino acids vs body protein** — the stock panel now separately names a **free amino-acid pool** and the **canonical body-protein/tissue inventory**, with body protein marked as functional tissue rather than a consequence-free reserve.
3. **Unresolved nutrient horizons** — the timescale ribbon now explicitly names **amino-acid and essential-fatty-acid horizons as unresolved** rather than using the broader phrase “several nutrient horizons.”

Oxygen, water/metabolic-water provenance, Output/Elimination, and the open-ended environmental surface were already represented consistently with the repaired canonical state and required no substantive visual correction.

See `post-reconciliation-audit.md` for the element-by-element audit and canonical basis.

## Current review posture

VIS-0001 is **ready for the combined PUB/VIS Red Team public-translation audit**. It remains internal and must not be published externally before that audit and PI approval.
