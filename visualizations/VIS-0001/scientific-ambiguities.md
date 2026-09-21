# VIS-0001 — Scientific and model ambiguities discovered during visualization

These are not visual-design defects. They are places where the canonical substrate is incomplete, internally inconsistent, or intentionally unresolved and therefore constrain what VIS-0001 may safely depict.

## 1. EF-PUB-0001 — canonical BIO registry inconsistency — resolved

**Historical significance:** high; **current publication blocker from this issue:** none.

During initial VIS-0001 development, the Design & Visualization Desk independently identified that `claims/registry.yaml` retained Biology_1-era fields while Biology_2, Data_2, RedTeam_2 and Editorial_1 recorded accepted corrections. The issue was later tracked as **EF-PUB-0001**.

The canonical registry has now been reconciled and integrated on `main` after Biology reconciliation, Librarian provenance verification, and Red Team canonical-consistency/mechanical verification.

**Visualization disposition:** the inconsistency did not determine VIS-0001's core architecture because the first visual pass already followed the accepted integrated correction state. Post-reconciliation review found only targeted clarity refinements: explicit whole-body vs compartment electrolyte labeling, explicit free-amino-acid-pool vs body-protein distinction, and explicit naming of unresolved amino-acid / essential-fatty-acid horizons.

The original discovery is preserved here as durable design history rather than deleted.

## 2. Output/Elimination is conceptually accepted but schema normalization is incomplete

RT-0005 is resolved at the scientific/model level. Editorial_1 defines Output/Elimination as distinct from Consumption. The global claim schema/registry has not fully normalized this role.

**Visualization action:** outputs are visually separated from resource/input arrows.

## 3. Short-duration oxygen inventory magnitude is unresolved

The revised architecture requires a finite short-duration oxygen inventory, but its magnitude/distribution is intentionally not parameterized.

**Visualization action:** VIS-0001 shows oxygen continuity plus a qualitative short buffer on the timescale ribbon, with no volume, rate, or concentration.

## 4. Water replenishment is highly conditional

Initial body-water stock, metabolic water, preformed water intake, and losses all contribute. Loss rates vary with climate, activity, health, and other modifiers.

**Visualization action:** no daily water number; preformed water is shown as a conditional boundary input.

## 5. Amino-acid replenishment/depletion horizon is unresolved

Body protein can contribute amino acids through proteolysis, but it is functional tissue and must not be depicted as a dedicated, costless nutrient reserve.

**Visualization action:** one canonical body-protein/tissue stock is shown with an explicit consequence warning. No horizon number is shown.

## 6. Essential-fatty-acid horizon is unresolved

The unsupported >24-hour generalization was specifically removed in RedTeam_2.

**Visualization action:** nutrient horizons appear under “variable / unresolved,” not as a longer-than-one-day quantitative claim.

## 7. Micronutrients cannot be represented as one homogeneous stock

BIO-0010 explicitly requires nutrient-specific decomposition.

**Visualization action:** micronutrients are omitted from the primary stock labels rather than compressed into a misleading single reservoir.

## 8. Acute waste-processing interruption tolerances are unresolved

The need for renal/excretory processing is structurally supported, but a universal short-term interruption threshold is not.

**Visualization action:** renal processing is shown as a process; no countdown or acute threshold is drawn.

## 9. Sleep has different outcome semantics from acute viability

Wave 1 supports sleep/recovery as relevant to function and longer-horizon health, but not as a manufactured universal 24-hour survival minimum.

**Visualization action:** sleep/recovery is shown among processes, but without a “must consume X hours today” treatment.

## 10. Environmental viability surface is incomplete

BIO-0014 is an umbrella/decomposition claim. Respiratory and thermal child models do not exhaust contaminants, pressure, trauma, and other hazards.

**Visualization action:** the environmental field is explicitly labeled open-ended and uses a dashed uncertainty marker.

## 11. No universal reference human is instantiated

Body mass, composition, age, activity, climate, altitude, health status, pregnancy/lactation, and other modifiers matter differently across dependencies.

**Visualization action:** VIS-0001 explains structure rather than drawing a numeric “average human.”

## 12. Outcome layer can change what counts as a requirement

Viability, stability, function, health, and comfort are not interchangeable.

**Visualization action:** the primary visual uses viability/stability language conservatively. Later public variants should declare the target outcome whenever thresholds or quantities are introduced.
