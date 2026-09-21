# Biology_2 — EXP-0001 response to RedTeam_1

Status: **revision complete / evidence and cross-desk reconciliation pending**

Biology_2 preserves Biology_1 as the historical first-pass synthesis and revises the durable BIO objects in `claims/registry.yaml`. Challenged claims are version 2 and now link to the relevant RT objects.

## Challenge dispositions

| Challenge | Biology target(s) | Disposition | Biology_2 response |
|---|---|---|---|
| RT-0001 | BIO-0002 | accepted | Replaced the claim that humans have no physiologically meaningful oxygen store. BIO-0002 now recognizes finite short-duration oxygen inventories in lungs, oxygenated blood/hemoglobin and myoglobin while preserving the requirement for renewed environmental oxygen over the 24-hour window. |
| RT-0002 | BIO-0005 | accepted | Body-water balance now includes metabolic water from substrate oxidation as well as preformed water from beverages/food. External preformed-water requirement is conditional on initial stock, metabolic production and losses. |
| RT-0003 | BIO-0008 | accepted | Free amino-acid pools are distinguished from body-protein/tissue inventory. No generic amino-acid reserve or replenishment horizon is asserted. Tissue proteolysis is explicitly physiologically consequential. |
| RT-0004 | BIO-0009 | accepted | Retracted the unsupported claim that the essential-fatty-acid replenishment horizon is >24 h in ordinary stocked people. Horizon is now unresolved; only the weaker anti-calendar inference remains. |
| RT-0005 | BIO-0003, BIO-0012 | accepted | CO2 elimination and renal excretion are reclassified from Consumption to Output/Elimination. This intentionally exposes a terminology/schema requirement for the Data/Editor desks rather than forcing outputs into an incorrect existing role. |
| RT-0006 | BIO-0006 | accepted as boundary correction | BIO-0006 now distinguishes whole-body electrolyte inventory from compartment-specific pools. Internal redistribution may alter compartment stocks but cannot change conserved whole-body mass. |
| RT-0007 | BIO-0007, BIO-0008 | accepted | Body protein/tissue is declared one canonical physical inventory with multiple transformations. It must not be duplicated as independent energy and amino-acid reserves. |
| RT-0008 | BIO-0014 | accepted | BIO-0014 is explicitly an open-ended umbrella/decomposition claim, not a complete viable-environment specification. Hazard-specific child claims are required for quantitative/completeness-sensitive use. |

## What did not change

RedTeam_1 did not overturn the central Biology architecture:

- observation window is distinct from replenishment horizon;
- physiological use does not imply equal same-window external replenishment;
- t0 inventories remain explicit boundary conditions;
- dietary reference values are not automatically survival minima;
- capacities and bounded states are not commodities;
- missing thresholds remain unresolved rather than being filled with population averages;
- sleep remains a functional-performance/long-term-health dependency without a manufactured 24-hour survival minimum;
- thermal support remains conditional on organism-environment interaction.

BIO-0001, BIO-0004, BIO-0010, BIO-0011 and BIO-0013 therefore remain version 1 in this pass. They are not declared universally validated; they simply did not require wording changes from the registered RedTeam_1 challenges.

## Revised graph semantics

### Oxygen

The model must now permit:

```text
finite O2 inventory at t0
        +
environmental O2 inflow
        |
        v
oxygen delivery -> tissue utilization
```

The finite inventory can matter at short timescales. It is not a substitute for continued access over EXP-0001's 24-hour window.

### Water

```text
preformed water intake ----+
                           |
metabolic substrate        +--> body-water stock/state --> losses
       |                   |
       +-> metabolic water-+
```

Metabolic water is generated from oxidation of substrate already represented elsewhere. It must not become a second independent external resource.

### Protein / amino acids

```text
             +--> protein synthesis
free AA pool +--> oxidation
     ^       +--> other AA-dependent processes
     |
proteolysis
     |
canonical body-protein/tissue stock
     |
protein synthesis <--- exogenous indispensable amino acids
```

There is no second body-protein reserve for the energy model. The same physical inventory can feed multiple transformations, so mass, nitrogen and energy accounting must share ownership.

### Electrolytes

Whole-body inventory and compartment states are distinct:

```text
external intake --> whole-body inventory --> external losses
                         |
             internal redistribution
                  /             \
          compartment A <----> compartment B
```

Internal transfers cancel at the whole-body boundary unless an actual source/sink crosses that boundary.

### Outputs

Biology_2 adds the semantic need for **Output/Elimination**. CO2 exhalation and renal waste excretion are required removal flows, not resource consumption. The formal terminology/schema owner should decide whether this becomes a new global `quantity_role` value or a separate output-role field.

## Remaining holds

Biology_2 does **not** resolve the following by assertion:

- BIO-0008: indispensable-amino-acid replenishment/depletion horizon remains unresolved.
- BIO-0009: essential-fatty-acid replenishment/depletion horizon remains unresolved.
- BIO-0010: micronutrient family remains unsuitable for aggregate quantitative use; nutrient-specific decomposition is still required.
- BIO-0012: acute tolerable interruption durations for waste-processing/excretion are unresolved.
- BIO-0014: environmental hazard surface remains incomplete.
- Special-population parameterization remains required before broad quantitative use.

## Cross-desk consequences

**Data_2** should use the same canonical body-protein inventory across energy and amino-acid models; repair electrolyte conservation; permit finite O2 inventory where timescale requires; retain metabolic water with explicit substrate provenance; and separate output/elimination from consumption.

**Librarian_2** should audit the evidence mapping for the revised clauses, especially oxygen inventories, amino-acid turnover/body-protein mobilization and any future attempt to parameterize essential-fatty-acid horizons.

**Editor/Terminology** should resolve the Output/Elimination semantic addition without collapsing it into Consumption.

**Red Team** should treat these as responses, not automatic closures. RT objects remain open until the Red Team accepts the revisions and records resolution.

## Promotion posture

Biology_2 is ready for cross-desk reconciliation but **not recommended for canonical integration by the Biology desk alone**. The high-severity challenges require explicit Red Team dispositions and relevant evidence/model updates before Scientific Core v0.1.
