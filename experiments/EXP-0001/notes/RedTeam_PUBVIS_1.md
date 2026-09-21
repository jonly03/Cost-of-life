# RedTeam_PUBVIS_1 — EXP-0001 Wave 1 Public-Translation Audit

## 1. Executive disposition

**HOLD FOR REVISION**

PUB-0001 and VIS-0001 preserve the central Scientific Core architecture well for public translation. The anti-calendar rule, Inventory Blindness, typed system distinctions, oxygen correction, metabolic-water provenance, canonical body-protein ownership, unresolved essential-fatty-acid horizon, Output/Elimination semantics, environmental incompleteness and the economic boundary all survive translation.

One consequential cross-artifact defect remains: **RT-0009**. The package can cause a reasonable reader to interpret sleep/recovery as an acute 24-hour viability requirement even though canonical BIO-0013/DATA-0008 support it at function/health layers and explicitly do not establish a 24-hour survival threshold.

No other Critical/High translation defect was found.

## 2. Must fix before release

### RT-0009 — outcome-layer collapse for sleep/recovery — HIGH

**PUB element:** section “So what does a human need for 24 hours?”, sentence beginning “Across a 24-hour period, continued human viability depends on...” and ending with “longer-horizon nutrient and recovery dependencies...”

**VIS element:** primary diagram, PROCESSES column, where “sleep / recovery” is presented alongside ATP/metabolism, circulation, gas exchange and renal processing without an outcome-layer qualifier.

**Canonical basis:** BIO-0013; DATA-0008; TERM-0011 Viability; TERM-0013 Function; TERM-0014 Health; REF-0010; REF-0018.

**Mismatch:** Wave 1 does not establish sleep as an acute 24-hour survival requirement. PUB's summary grammatically places recovery dependencies inside what continued viability depends on. VIS visually reinforces coequal status with acute viability processes.

**Likely public misunderstanding:** “The project found that sleep is one of the things a human must get during each 24-hour period to stay alive.”

**Required correction:** Publication should separate viability dependencies from longer-horizon function/health dependencies in that synthesis sentence. Visualization should label or otherwise distinguish sleep/recovery as function/health rather than allowing it to read as a coequal 24-hour viability process. No new science, threshold, or redesign is required.

## 3. Should fix

No additional blocking scientific correction is required.

One low-risk visual clarity issue may be considered: the STOCKS panel uses one reservoir-shaped container for several biologically distinct stocks. Because the panel is explicitly plural, labels free amino-acid pool and body protein/tissue separately, and marks body protein as functional tissue/not consequence-free reserve, Red Team does **not** elevate this to a challenge. If the visual is later simplified further, those separations must survive.

## 4. Acceptable simplifications

- “A living human is not an empty container that resets at midnight.” Faithfully communicates t0 inventories and the anti-calendar rule.
- The reservoir analogy for Inventory Blindness is safe because PUB explicitly limits the analogy and VIS labels the balance as stock-flow grammar, not a universal physiological equation.
- Qualitative oxygen treatment is safe: “finite O2 buffer + continuing external access” preserves RT-0001 without inventing reserve magnitude.
- Grouping glycogen and adipose as endogenous substrate removes detail without asserting identical kinetics or magnitude.
- Water treatment safely preserves initial body-water stock, preformed water, metabolic water from substrate oxidation and losses.
- Electrolytes are safely split into “whole-body electrolytes” in STOCKS and “compartment gradients” in BOUNDED STATES.
- The environment box is safe despite geometric closure because “open-ended hazard surface,” the unknown marker and legend explicitly deny completeness.
- No commercial shelter, bottled oxygen, fixed food bundle or sanitation technology is depicted as biologically mandatory.
- The timescale ribbon stays qualitative and explicitly leaves amino-acid and EFA horizons unresolved.
- PUB's fasting discussion is acceptably scoped to metabolically stable adults with adequate stores.
- The “minimum cost of one human day” appears only as the intuitive model the investigation rejects; the ending states that economic translation is incomplete.

## 5. PUB-0001 assessment

**Overall:** scientifically faithful except for RT-0009.

The headline/subheadline correctly reject a universal daily shopping list without claiming daily needs do not exist. Requirement/Consumption/Replenishment and observation-window/replenishment-horizon distinctions are clear. Oxygen, water, energy/body-protein, essential nutrients, outputs, thermal/environmental conditions and economic boundaries track canonical scope. The “What we still don't know” section preserves quantitative, population, environmental, sleep and economic limits.

The consequential exception is the synthesis sentence under “So what does a human need for 24 hours?” It uses **continued human viability depends on** as the governing clause and includes “recovery dependencies.” That is stronger than BIO-0013's function/health evidence and conflicts with PUB's own later limitation.

## 6. VIS-0001 assessment

**Overall:** structurally faithful except for the sleep/recovery outcome-layer implication contributing to RT-0009.

The primary diagram centers an organism boundary with typed objects rather than commodities. Arrow thickness is not mapped to quantity. Spatial grouping communicates type, not chronology. The environmental field is explicitly incomplete. Inputs are conditional. Outputs are clearly outputs/exchange. The semantic strip and anti-calendar callout are prominent.

Oxygen is not shown as zero inventory; water/metabolic-water provenance is clear; body protein and free-AA pool are separately named; body protein is marked functional tissue; electrolyte whole-body inventory and compartment gradients are separated; EFA and amino-acid horizons are explicitly unresolved.

The main problem is that “sleep / recovery” uses the same process capsule grammar and undifferentiated PROCESSES column as ATP/metabolism, circulation, gas exchange and renal processing. A fast viewer receives no cue that the evidentiary outcome layer differs.

## 7. Cross-artifact consistency assessment

PUB and VIS are otherwise compatible in system grammar, anti-calendar principle, inventory logic, output semantics, environmental scope and economic boundary.

RT-0009 is cross-artifact because PUB's outcome-layer overreach and VIS's visual equivalence reinforce each other. The qualification in PUB's “What we still don't know” section does not fully rescue the dominant combined implication.

No contradiction was found for oxygen, water, body protein, amino acids, EFA, electrolytes, Output/Elimination, environmental incompleteness or commercial-solution boundaries.

## 8. 15-second headline test

### PUB-0001
**Likely takeaway:** “The project found that you cannot calculate what a person needs for a day by listing daily food, water and other products; the body starts with stores, different requirements run on different clocks, and the study has not calculated a universal daily minimum or price.”

**Classification:** **FAITHFUL**

### VIS-0001
**Likely takeaway:** “A human is an open system with stored reserves, regulated states, processes and environmental inputs; using something during 24 hours does not mean it must be replaced that day.”

**Classification:** **ACCEPTABLE SIMPLIFICATION**

Secondary risk: sleep/recovery visually appears equivalent in outcome status to circulation/gas exchange.

### Combined PUB + VIS
**Likely takeaway:** “The first result is not a daily survival shopping list or a price. It is a stock-and-flow model showing that some needs are continuous, some are buffered by existing inventory, and replenishment happens on different or unresolved timescales.”

**Classification:** **ACCEPTABLE SIMPLIFICATION, WITH ONE MATERIAL CORRECTION REQUIRED**

The combined package is faithful on the central discovery, but the mutually reinforcing sleep/recovery presentation can create one stronger-than-canonical conclusion.

## 9. EF-PUB-0001 downstream verification

**PASS.**

The repaired canonical state propagated successfully into both refreshed artifacts. Neither retains the zero-O2-inventory interpretation; water/metabolic-water, body protein/free-AA, electrolyte, Output/Elimination and environmental semantics match the repaired state. BIO-0009 does not imply a known longer-than-24-hour EFA interval: PUB says unresolved and VIS labels it unresolved. PUB provenance mapping resolves to canonical BIO v2 objects. EF-PUB-0001 remains durable history and is explicitly marked RESOLVED. No new post-reconciliation contradiction was found.

## 10. New RT objects

**RT-0009 — cross_artifact_inconsistency / outcome-layer collapse — HIGH — OPEN**

Artifact: BOTH. Targets BIO-0013 and DATA-0008. See challenges/registry.yaml for the durable challenge object.

No other consequential translation defect warranted a new RT object.

## 11. Residual limitations worth disclosing

Preserve the limitations the package already states:
- no universal reference human;
- nutrient-specific horizons remain unresolved where stated, especially amino acids and EFA;
- environmental hazard coverage is incomplete;
- many quantitative thresholds and interruption tolerances remain unresolved;
- sleep evidence is function/health oriented and does not establish a universal acute 24-hour survival minimum;
- EXP-0001 has not calculated a monetary minimum cost of a human day or universal commercial bundle.

No additional caveat layer is required.

## 12. Final confirmations

| Acceptance question | Answer |
|---|---|
| Is Inventory Blindness represented correctly? | **YES** |
| Is Requirement != Consumption != Replenishment intact? | **YES** |
| Is observation window != replenishment horizon intact? | **YES** |
| Do unresolved quantities remain unresolved? | **YES** |
| Is EFA replenishment horizon still unresolved? | **YES** |
| Are Output/Elimination semantics intact? | **YES** |
| Is environmental incompleteness preserved? | **YES** |
| Are outcome layers kept sufficiently distinct? | **NO** — RT-0009. |
| Does the package avoid implying a universal commercial solution? | **YES** |
| Does the package avoid implying EXP-0001 calculated “the cost of one human day”? | **YES** |
| Could a reasonable public reader/viewer leave with a materially stronger conclusion than Scientific Core v0.1? | **YES** — specifically, that sleep/recovery was established as an acute 24-hour survival requirement. |

## Final Red Team disposition

**HOLD FOR REVISION**

Return RT-0009 to the Publication and Visualization desks for narrow correction. Do not rewrite or redesign the package wholesale. After both owning desks correct the outcome-layer implication, Red Team should mechanically verify the changed sentence/visual element and rerun the combined 15-second test.

This audit does not authorize external publication. Final release authority remains with the human PI.
