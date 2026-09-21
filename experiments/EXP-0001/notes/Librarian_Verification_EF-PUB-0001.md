# Librarian Verification — EF-PUB-0001 BIO Registry Reconciliation

Experiment: **EXP-0001**  
Scope: **narrow provenance verification of Biology registry reconciliation only**  
Biology reconciliation reviewed: PR #13  
Canonical baseline reviewed: Scientific Core v0.1 on `main`

## 1. Overall verification result

**HOLD — PROVENANCE REPAIR REQUIRED**

The Biology reconciliation is substantially faithful to Biology_2, Data_2, Librarian_2, RedTeam_2 and the registered REF corpus. Thirteen of fourteen BIO objects are provenance-consistent, with several non-blocking notes preserving the distinction between direct source support and project inference.

One material residual mismatch remains in **BIO-0009**: the reconciled `replenishment_horizon` correctly says **unresolved**, but the unchanged `peom_implication` still says **“Treat essential lipids as longer-horizon nutrient stocks/flows.”** In the durable evidence state, REF-0003 establishes essentiality and REF-0022 provides specialized deficiency evidence, while Librarian_2 and RT-0004 explicitly reject a general >24-hour healthy-person replenishment horizon. “Longer-horizon” therefore reintroduces a positive duration inference that the reconciliation otherwise correctly retracts.

No new literature was required.

## 2. BIO-by-BIO verification table

| BIO | Disposition | Provenance verification |
|---|---|---|
| BIO-0001 | **VERIFIED WITH NOTE** | REF-0002 and REF-0023 support whole-body energy requirement and cellular ATP turnover respectively. The PEOM statement that energy can be supplied by internal and/or external substrates is a project synthesis across sources, not a sentence directly established by either source. No same-day food requirement is inferred. |
| BIO-0002 | **VERIFIED WITH NOTE** | REF-0001/0016 support the oxygen-delivery cascade; REF-0026 supports transient body oxygen stores during apnea. The reconciled finite short-duration inventory wording is consistent with RT-0001/Librarian_2 and does not quantify reserve size or safe interruption tolerance. “Cannot sustain the 24-hour window” is a project-level synthesis from finite short-duration storage plus continuing metabolic demand, not a directly measured 24-hour deprivation experiment. |
| BIO-0003 | **VERIFIED** | REF-0015 supports respiratory CO2 handling as part of acid-base homeostasis. Reclassification to Output/Elimination changes accounting semantics without strengthening the physiological proposition. Required ventilation remains explicitly state-dependent and unparameterized. |
| BIO-0004 | **VERIFIED** | REF-0001/0016 support perfusion as part of oxygen/substrate transport. The claim preserves organ-specific threshold uncertainty and does not convert cardiac-output averages into minima. |
| BIO-0005 | **VERIFIED WITH NOTE** | REF-0004/0013/0019 support body-water stock/state, losses, turnover variability and water-homeostasis regulation; Librarian_2/RT-0002 support inclusion of metabolic water. The “hours to days” replenishment-horizon field must remain qualitative and must not be read as a verified safe deprivation interval; the registered evidence does not establish a universal dehydration survival threshold. |
| BIO-0006 | **VERIFIED WITH NOTE** | REF-0004/0005/0015/0019 support electrolyte regulation, compartment physiology and water/acid-base relationships. The whole-body-versus-compartment conservation rule is a project modeling inference from a declared boundary plus mass conservation; it is not a quoted source conclusion. No same-day sodium/potassium minimum is inferred. |
| BIO-0007 | **VERIFIED WITH NOTE** | REF-0002/0003/0014/0017 support energy requirements, endogenous substrate use and scoped fasting physiology. The one-canonical-body-protein ownership rule is a project conservation/modeling inference adopted in Biology_2/Data_2/RT-0007; protein-turnover evidence is additionally registered under REF-0024/0025 through BIO-0008. The healthy-stocked-adult scope remains essential. |
| BIO-0008 | **VERIFIED WITH NOTE** | REF-0003 supports indispensable-amino-acid essentiality; REF-0024/0025 support dynamic protein turnover, proteolysis and tissue-derived amino-acid supply. The reconciled object correctly leaves the safe depletion/replenishment horizon unresolved and does not represent body protein as a consequence-free dedicated amino-acid reserve. “One canonical inventory” is a project ownership rule, not a source-stated biological label. |
| BIO-0009 | **HOLD** | The claim and `replenishment_horizon` correctly retract the unsupported >24-hour assertion, consistent with REF-0003/0022, Librarian_2 and RT-0004. However, `peom_implication: "Treat essential lipids as longer-horizon nutrient stocks/flows."` still asserts a positive longer horizon. The current corpus supports essentiality and rejection of calendar forcing, **not** a general healthy-person >24-hour or otherwise specified “longer-horizon” replenishment interval. |
| BIO-0010 | **VERIFIED WITH NOTE** | REF-0006/0007/0008/0009 support nutrient heterogeneity, differing stores/turnover/deficiency biology and the inadequacy of one micronutrient rule. The “months/years” wording remains qualitative family-level scope; no nutrient-specific model parameter is thereby validated. |
| BIO-0011 | **VERIFIED** | REF-0011/0012/0021 support multivariate heat/cold thermoregulation and interaction with environment, activity and protective mechanisms. The claim does not convert comfort or occupational limits into universal viability thresholds. |
| BIO-0012 | **VERIFIED** | REF-0015/0020 support renal acid-base/nitrogen handling and excretion. Output/Elimination is an accounting correction only; acute interruption tolerance remains explicitly unresolved. External sanitation remains outside the internal physiological proposition. |
| BIO-0013 | **VERIFIED WITH NOTE** | REF-0010 supports regular adult sleep guidance for health; REF-0018 supports acute functional/physiological impairment in young healthy adults. The object correctly avoids a universal 24-hour survival minimum and retains accumulated sleep state as an initial-condition issue. |
| BIO-0014 | **VERIFIED WITH NOTE** | REF-0011/0012/0021 directly support thermal environmental dimensions; BIO-0002 and its REF evidence provide the respiratory dependency. The reconciled object correctly makes BIO-0014 an open-ended umbrella and requires hazard-specific child claims. Pressure, contaminants and unmodeled hazards remain enumerated project scope dimensions, **not quantitatively established surfaces** in the registered corpus. |

## 3. REF relationship / provenance findings

### Stable IDs and traceability

- BIO-0001 through BIO-0014 remain stable; no persistent BIO ID was recycled.
- REF-0001 through REF-0026 remain stable.
- The reconciliation restores `supported_by` arrays for all fourteen BIO objects and `challenged_by` links for the challenged claims.
- The historical RT objects remain attached to reconciled claims rather than being erased after resolution.

### Bidirectional relationship caveats

Two pre-existing relationship-direction asymmetries remain and should be understood as metadata limitations, not new science:

1. **REF-0026** has `relationships.challenges: ["BIO-0002"]` and no `supports` entry because it was registered to challenge Biology_1's zero-inventory wording. The reconciled BIO-0002 now lists REF-0026 in `supported_by` because the same source supports the corrected finite-inventory clause. This is logically sound across claim versions, but the current source schema cannot express “challenged v1 / supports v2” explicitly. Do not erase the historical challenge relation merely to make the arrays symmetric.
2. Evidence Base v0.1's first-pass BIO-0014 row cited oxygen-transport sources REF-0001/0016 in addition to thermal REF-0011/0012/0021. The reconciled BIO-0014 `supported_by` array contains only the direct environmental/thermal refs and depends on BIO-0002 for respiratory physiology. This is acceptable if dependency traversal is honored; it should not be interpreted as direct REF support for pressure or contaminant thresholds.

### Source-versus-inference boundary

The following are project inferences built from supported premises, not direct statements by one REF source:

- finite O2 stores cannot sustain whole-body metabolism across the full 24-hour observation window;
- whole-body and compartment electrolyte ledgers must obey a single declared conservation boundary;
- body protein should have one canonical inventory owner across energy and amino-acid models;
- absence of evidence for same-day essential-fatty-acid ingestion does not establish a positive >24-hour safe horizon;
- BIO-0014's environmental hazard set is intentionally open-ended.

These are legitimate synthesis/modeling rules where already accepted, but they must not be described as direct source findings.

## 4. RT-0001 through RT-0008 evidence-sensitive verification

| RT | Verification |
|---|---|
| RT-0001 | **VERIFIED WITH NOTE.** REF-0026 supports transient internal O2 stores; REF-0001/0016 support ongoing delivery. No reserve magnitude or interruption tolerance is established. |
| RT-0002 | **VERIFIED.** REF-0004/0013/0019 and Librarian_2 support metabolic water as a legitimate inflow while prohibiting its double counting as an independent external resource. |
| RT-0003 | **VERIFIED.** REF-0024/0025 strengthen the distinction between dynamic free-AA availability and body-protein mobilization; no safe horizon is introduced. |
| RT-0004 | **NOT FULLY PRESERVED IN BIO-0009 OBJECT.** The positive >24-hour horizon was correctly retracted, but the stale “longer-horizon” PEOM implication remains. |
| RT-0005 | **VERIFIED.** Output/Elimination semantics are consistent with REF-0015/0020 and do not change the underlying physiological claims. |
| RT-0006 | **VERIFIED WITH NOTE.** Source physiology supports regulated compartments; the explicit cancellation/conservation rule is the project's boundary-aware mathematical interpretation. |
| RT-0007 | **VERIFIED WITH NOTE.** REF-0024/0025 support turnover/proteolysis; canonical inventory ownership is a project accounting rule preventing duplicate representation of the same tissue. |
| RT-0008 | **VERIFIED.** BIO-0014 is explicitly incomplete/open-ended; no source is used to claim complete hazard coverage. |

## 5. Remaining provenance inconsistencies

### Blocking

**BIO-0009 — stale PEOM implication**

Unsupported residual proposition:

> “Treat essential lipids as longer-horizon nutrient stocks/flows.”

The registered evidence supports essential-fatty-acid essentiality and supports rejecting the inference that a calendar-day boundary creates a daily minimum. It does not establish a general healthy-person “longer-horizon” replenishment interval. This wording conflicts with the same object's `replenishment_horizon: unresolved` and with RT-0004's resolution by retraction.

This should be repaired by Biology/Director reconciliation before the registry repair is integrated. No new evidence is needed or recommended merely to preserve the phrase.

### Non-blocking

- REF-0026's historical `challenges` direction versus reconciled BIO-0002's `supported_by` direction is version-context dependent and not expressible cleanly in schema v0.1.
- BIO-0005's “hours to days” language is not a verified safe dehydration/deprivation tolerance; retain it only as qualitative replenishment/state responsiveness, not as a survival interval.
- BIO-0010's family-level “months/years” language must not become nutrient-specific quantitative parameters.
- BIO-0014's named pressure/contaminant dimensions remain decomposition targets, not registered quantitative hazard surfaces.

## 6. New evidence required?

**No.**

The reconciliation can be verified or rejected using the existing canonical REF corpus and Librarian_2 audit. No missing already-relied-upon source required retrieval, and no new REF object was introduced.

## 7. Recommendation

**HOLD — PROVENANCE REPAIR REQUIRED**

The reconciliation is otherwise ready for the narrow Red Team consistency check, but BIO-0009 should first remove or neutralize the stale “longer-horizon” PEOM implication so the object is internally consistent with its unresolved horizon and the accepted RT-0004 resolution.

This verification does **not** approve PUB-0001 and does not merge PR #13.
