# RedTeam_1 — EXP-0001 adversarial synthesis review

Status: **completed first pass / challenges open**

## Scope reviewed

Red Team reviewed Biology_1 (BIO-0001..BIO-0014), Data_1 (DATA-0001..DATA-0008), and Evidence Base v0.1 as durable desk artifacts. This is a synthesis attack, not an independent reconstruction of the investigation.

Eight consequential challenges are registered as RT-0001 through RT-0008.

## Challenge summary

| RT | Targets | Severity | Failure mode | Disposition |
|---|---|---:|---|---|
| RT-0001 | BIO-0002, DATA-0004 | medium | source-to-claim overreach | qualify oxygen-store language/model |
| RT-0002 | BIO-0005, DATA-0005 | high | stock/flow + source-to-claim overreach | include metabolic-water pathway consistently |
| RT-0003 | BIO-0008, DATA-0006 | high | stock/category error | separate free amino-acid pools from body protein |
| RT-0004 | BIO-0009 | high | unsupported replenishment horizon | remove or source >24 h horizon |
| RT-0005 | BIO-0003, BIO-0012, DATA-0002 | high | category error | distinguish output/elimination from consumption |
| RT-0006 | BIO-0006, DATA-0005 | high | stock/flow conservation error | make electrolyte stock boundary explicit |
| RT-0007 | BIO-0007, BIO-0008, DATA-0003, DATA-0006 | high | double counting | canonicalize body-protein inventory |
| RT-0008 | BIO-0014, DATA-0004, DATA-0007 | medium | unjustified completeness/universality | validate only as umbrella claim |

## What survived the attack

The central anti-calendar architecture is strong. Red Team found no basis in the reviewed corpus to overturn these synthesis rules:

- a 24-hour observation window does not establish a 24-hour replenishment horizon;
- population reference intakes, measured turnover and recommendations are not survival minima;
- pre-existing physiological inventories must be represented rather than erased;
- capacities and regulated states are not consumables;
- missing quantitative thresholds should remain unresolved rather than filled with averages;
- sleep guidance should not be promoted into an acute survival minimum;
- thermal support is conditional on organism-environment interaction rather than universally synonymous with shelter.

These are **review findings about the synthesis**, not blanket validation of every BIO/DATA object.

## Validation-for-model-use disposition

### Candidate after targeted revision

The following claims/specifications appear structurally suitable for scoped model use once cross-branch evidence relationships are integrated and any linked challenge below is resolved:

- BIO-0001 cellular energy dependency
- BIO-0004 perfusion/circulation dependency
- BIO-0011 thermal-homeostasis dependency
- BIO-0013 sleep/recovery as function/health dependency, explicitly not a 24-hour survival minimum
- DATA-0001 general hybrid grammar
- DATA-0002 time-window accounting **after RT-0005 semantic correction**
- DATA-0007 thermal representation, subject to BIO-0014 remaining an incomplete umbrella
- DATA-0008 process/state framing, with no quantitative sleep or renal interruption threshold implied

### Hold from quantitative validation

- BIO-0008: essentiality supported; replenishment horizon unresolved and stock representation needs revision (RT-0003).
- BIO-0009: same-day universality rejected, but >24-hour horizon is insufficiently supported for the stated population (RT-0004).
- BIO-0010 / DATA-0006: micronutrients remain an aggregate/indexed family; nutrient-specific quantitative use is premature.
- BIO-0012 / DATA-0008: mechanism is supportable, but acute tolerable interruption durations remain unresolved.
- BIO-0014: use only as an umbrella/decomposition requirement, not as a complete environmental admissibility surface (RT-0008).

### Revision required before model use in challenged dimensions

BIO-0002/DATA-0004, BIO-0005/DATA-0005, BIO-0006/DATA-0005, BIO-0007/8 with DATA-0003/6, and BIO-0003/0012 with DATA-0002 require the changes described in their RT objects before those challenged semantics are treated as validated.

## Cross-cutting Red Team findings

**Inventory Blindness:** Biology_1 and Data_1 mostly defend against it successfully. The main residual risk is not erased inventory but *mischaracterized inventory*—especially protein/amino-acid pools and oxygen.

**False daily requirements / calendar forcing:** no major calendar-forcing defect was found. The strongest residual case is BIO-0009, where an anti-calendar conclusion was turned into an inadequately sourced positive >24-hour horizon.

**Averages masquerading as minima / false precision:** no consequential instance was found in Data_1. Null/symbolic parameters are appropriately retained.

**Hidden healthy-adult assumptions:** BIO-0007 scopes its fasting inference; Evidence Base v0.1 also warns against universality. This remains a parameterization risk rather than a current universal claim. Special-population branches are still required before broad quantitative use.

**Reference-human ambiguity:** Data_1 explicitly declines to instantiate a reference human. This is appropriate for Wave 1, but no later quantitative parameter set should be called universal without a declared population vector.

**Category errors:** RT-0005 is consequential because elimination/output is not cleanly separated from consumption.

**Stock/flow confusion and double counting:** RT-0006 and RT-0007 are the highest-priority mathematical corrections.

**Unsupported thresholds:** the synthesis generally avoids manufacturing them. Evidence gaps should remain explicit.

**Source-to-claim overreach:** RT-0001, RT-0002 and RT-0004 identify clauses that outrun or mismatch the registered support.

**Omitted modifiers / unjustified universality:** most BIO claims enumerate modifiers well. BIO-0014 remains intentionally broad and therefore cannot be treated as exhaustive.

## Required next pass

Biology_2 should answer RT-0001 through RT-0005 and RT-0008 where they touch biological wording/scope. Data_2 should answer RT-0001 through RT-0003 and RT-0005 through RT-0008 where they touch representation. Librarian_2 should verify any new evidence used to resolve RT-0001, RT-0003 or RT-0004 and audit the source-to-claim mappings after revisions.

Legitimate unresolved disagreement or missing evidence should remain open rather than being silently normalized.

## Promotion recommendation

**Do not integrate RedTeam_1 as a declaration that the full scientific core is validated.** Integrate the challenges and review findings as the adversarial input to Biology_2 + Data_2 + Librarian_2. Scientific Core v0.1 should be considered only after those responses are durable and the open high-severity challenges have explicit dispositions.
