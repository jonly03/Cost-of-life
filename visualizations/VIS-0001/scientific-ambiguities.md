# VIS-0001 — Scientific and model ambiguities discovered during visualization

These are not visual-design defects. They are places where the canonical substrate is incomplete, internally inconsistent, or intentionally unresolved and therefore constrain what VIS-0001 may safely depict.

## 1. BIO registry does not reflect the integrated Red Team corrections

**Severity for publication:** high.

On `main`, `Biology_2.md`, `Data_2.md`, `RedTeam_2.md`, and `Editorial_1.md` state that RT-0001 through RT-0008 were incorporated and resolved.

However, `claims/registry.yaml` still contains version-1 BIO objects. Examples visible during this review include:

- BIO-0002 still says humans have no physiologically meaningful oxygen store capable of substituting for sustained delivery, while Biology_2/RedTeam_2 require explicit recognition of finite short-duration lung/blood/myoglobin oxygen inventories.
- BIO-0003 still carries `quantity_role: Consumption`, while Data_2/Editorial_1 classify CO2 elimination as Output/Elimination.
- BIO-0005 still uses pre-correction wording centered on external water replacement, while Biology_2/Data_2 explicitly add metabolic water and provenance.
- BIO-0009 still states a >24-hour replenishment horizon in ordinary stocked conditions, while Biology_2/RedTeam_2 say that assertion was retracted and the horizon remains unresolved.

**Visualization action:** VIS-0001 depicts the accepted corrections described by the integrated Wave-1 notes and records the registry mismatch rather than copying the stale clauses.

**Required before external publication:** normalize the BIO registry or document an explicit canonical precedence rule for the integrated Scientific Core.

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
