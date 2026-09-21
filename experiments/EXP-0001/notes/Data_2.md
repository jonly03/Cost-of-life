# Data_2 — EXP-0001 Red Team response

Status: **revised after RedTeam_1 / challenged biological claims remain upstream-dependent**

Data_2 revises DATA-0001..DATA-0008 in response to RT-0001..RT-0008. The central anti-calendar architecture survives, but Red Team identified real representation defects that required correction.

## Disposition by challenge

| Challenge | Data disposition |
|---|---|
| RT-0001 | **Accepted.** DATA-0004 now permits a finite short-duration O2 inventory and models environment-to-inventory-to-tissue flow. Magnitude remains unresolved. |
| RT-0002 | **Accepted.** DATA-0005 preserves preformed-water input and metabolic-water production separately. Metabolic water is traced to substrate oxidation to prevent double counting as an independent external resource. |
| RT-0003 | **Accepted.** DATA-0006 no longer treats amino acids as a generic nutrient reserve. Free amino-acid pools and canonical body-protein/tissue stocks are separate. |
| RT-0004 | **Accepted as upstream constraint.** DATA-0006 does not encode a >24 h essential-fatty-acid horizon as validated. H remains unresolved absent stronger evidence. |
| RT-0005 | **Accepted.** Output/Elimination is now distinct from Use/Consumption. CO2 and renal waste are modeled as outputs. |
| RT-0006 | **Accepted.** DATA-0005 now distinguishes whole-body electrolyte stock from compartment stocks; internal transfers cancel across the enclosing boundary. |
| RT-0007 | **Accepted.** DATA-0003 and DATA-0006 share one canonical body-protein stock. Protein cannot be counted independently as energy reserve and amino-acid reserve. |
| RT-0008 | **Accepted.** BIO-0014 is treated only as an umbrella. Respiratory and thermal models explicitly cover partial hazard surfaces and cannot certify complete environmental viability. |

## Conservation rule strengthened

Data_1 used a permissive internal term G_i. Red Team showed that this could hide mathematically invalid creation/destruction when stock boundaries were ambiguous. Data_2 therefore requires directed transfers and declared boundaries:

```text
dS_i/dt = sum_a(F_ai) - sum_b(F_ib) + B_i
```

where `B_i` is limited to true production/destruction for the declared boundary. For transfers internal to an enclosing conserved system:

```text
sum_i internal_transfer_i = 0
```

This is now mandatory for electrolyte compartment models and is the default conservation discipline for later material-balance models.

## Canonical inventory ownership

A physical inventory must have one canonical owner. Multiple models may reference it, but may not instantiate independent copies.

The first explicit application is body protein:

```text
S_bodyprotein_r
   |-- proteolysis --> free amino-acid pools
   |                     |-- protein synthesis
   |                     |-- oxidation
   |                     +-- other loss
   +-- other tissue loss
```

DATA-0003 and DATA-0006 therefore share the same `S_bodyprotein_r`.

## Water provenance

Whole-body water balance is represented as:

```text
dS_water/dt =
    F_water_preformed
  + F_water_metabolic
  - sum(F_water_loss)
```

but `F_water_metabolic` is internally produced through oxidation of substrate represented by DATA-0003. A future economic/resource layer must not charge both the substrate and its metabolic-water product as independent external inputs.

## Oxygen timescale correction

Data_1's assumption that no meaningful oxygen inventory should be introduced was too strong. Data_2 includes `S_O2_short`, allowing finite initial lung/blood/myoglobin oxygen to buffer short interruptions. The model still does **not** infer that this stock can sustain a 24-hour observation window.

## Semantic accounting correction

Data_2 distinguishes:

- **Requirement** — condition/process/state/capacity/flow needed for a stated outcome.
- **Use/Consumption** — use or depletion of a specifically identified input/stock.
- **Output/Elimination** — material leaving the organism or a declared boundary.
- **Replenishment** — restoration of an inventory from outside its declared boundary.

This prevents CO2 exhalation and renal excretion from becoming consumed economic resources.

## Environmental completeness rule

`e_resp` and `e_thermal` are child hazard surfaces, not a complete `e_viable`. The environmental umbrella is open-ended until hazard-specific child claims/models establish coverage. Absence of a modeled hazard is not evidence of safety.

## What survived unchanged

Red Team found the core architecture defensible: observation window != replenishment horizon; initial inventories matter; averages/recommendations are not minima; state != stock != capacity; missing parameters remain unresolved; outcome layers remain distinct; and conditional thermal support is not automatically housing.

## Remaining holds

Data_2 is structurally improved but cannot resolve upstream evidence gaps. Quantitative validation remains on hold for amino-acid replenishment horizons, essential-fatty-acid horizons, micronutrient-specific stocks/horizons, environmental completeness, acute renal interruption tolerances, quantitative sleep dynamics, and most physiological thresholds.

The next integration question is therefore not whether every model is numerically complete. It is whether the revised grammar is now safe enough to carry validated claims without introducing conservation errors, double counting, semantic category errors, or unsupported horizons.
