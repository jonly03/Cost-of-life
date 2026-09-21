# Canonical BIO Registry Reconciliation — EF-PUB-0001

Experiment: **EXP-0001**  
Scope: **canonical registry integrity repair only; no new Biology investigation**  
Baseline audited: Scientific Core v0.1 on `main` at `82add596c772b6e4f58977a6d91be7efeb2a5689`

## Finding

Canonical `claims/registry.yaml` contained the Biology_1-era BIO registry even though Biology_2, Data_2, the Evidence Base, terminology and RedTeam_2 were canonical on `main`. RedTeam_2 had formally resolved RT-0001 through RT-0008 on the basis of Biology_2 corrections that were not actually reflected in the canonical BIO objects.

This reconciliation copies only already-accepted Wave 1 corrections into the registry and restores accepted REF/RT relationships. It does not create Biology_3 conclusions or new parameters.

## BIO-by-BIO audit

| BIO ID | Registry state | Accepted state | Discrepancy | Correction | Evidence/challenge basis |
|---|---|---|---|---|---|
| BIO-0001 | v1 wording faithful; provenance links empty | Biology_1 wording retained | Provenance drift only | Added accepted REF links; no scientific wording change | REF-0002, REF-0023; RedTeam_2 no wording correction |
| BIO-0002 | v1 asserted no physiologically meaningful O2 store | Biology_2 recognizes finite short-duration lung/blood/myoglobin O2 inventory; magnitude unresolved | **Material scientific version drift** | Restored Biology_2 wording, horizon/limitation, RT and REF links; v2 | RT-0001 resolved; REF-0001, REF-0016, REF-0026; Data_2 S_O2_short |
| BIO-0003 | quantity_role=Consumption | Output/Elimination | **Category-error drift** | quantity_role -> Output/Elimination; RT/REF links; v2 | RT-0005 resolved; REF-0015; Data_2 semantic accounting |
| BIO-0004 | v1 wording faithful; provenance links empty | Biology_1 wording retained | Provenance drift only | Added REF links | REF-0001, REF-0016 |
| BIO-0005 | external fluids/food framed as replacement source | preformed water + metabolic water; metabolic water traced to substrate oxidation and not independent external resource | **Material stock/flow drift** | Restored Biology_2 claim, boundary, assumption, dependencies, RT/REF links; v2 | RT-0002 resolved; REF-0004, REF-0013, REF-0019; Data_2 water provenance |
| BIO-0006 | generic body electrolyte pools | explicit whole-body inventory vs compartment pools; internal transfers conserve enclosing mass | **Boundary/conservation drift** | Restored Biology_2 boundary and limitation; RT/REF links; v2 | RT-0006 resolved; REF-0004/0005/0015/0019; Data_2 conservation rule |
| BIO-0007 | endogenous stores + external input; no protein ownership rule | one canonical body-protein/tissue inventory shared across energy and amino-acid transformations | **Inventory-ownership drift** | Restored canonical protein ownership boundary/limitation; RT/REF links; v2 | RT-0007 resolved; REF-0002/0003/0014/0017; Data_2 canonical inventory ownership |
| BIO-0008 | implied generic replenishment horizon; body protein and AA pools insufficiently separated | free AA pool distinct from canonical body protein; safe depletion/replenishment horizon unresolved | **Material stock/horizon drift** | Restored Biology_2 horizon, assumptions, uncertainty and limitations; RT/REF links; v2 | RT-0003/0007 resolved; REF-0003, REF-0024, REF-0025; Data_2 |
| BIO-0009 | asserted >24 h horizon under ordinary stocked conditions | horizon unresolved; anti-calendar conclusion retained without positive duration claim | **Unsupported-horizon drift** | Retracted >24 h assertion; preserved unresolved horizon; RT/REF links; v2 | RT-0004 resolved by retraction; REF-0003, REF-0022 |
| BIO-0010 | v1 aggregate micronutrient claim | Same Wave 1 state; quantitative decomposition still held | Provenance drift only | Added REF links; no new decomposition/parameters | REF-0006/0007/0008/0009; RedTeam_2 residual hold |
| BIO-0011 | v1 thermal claim faithful | Same Wave 1 state | Provenance drift only | Added REF links | REF-0011, REF-0012, REF-0021 |
| BIO-0012 | quantity_role=Consumption | Output/Elimination; acute interruption tolerance unresolved | **Category-error drift** | quantity_role -> Output/Elimination; preserved unresolved threshold; RT/REF links; v2 | RT-0005 resolved; REF-0015, REF-0020; Data_2 |
| BIO-0013 | v1 sleep/function-health claim faithful | Same Wave 1 state; no 24 h survival minimum | Provenance drift only | Added REF links; no quantitative sleep parameter | REF-0010, REF-0018; RedTeam_2 residual hold |
| BIO-0014 | broad environmental claim could be read as complete surface | open-ended umbrella/decomposition claim; child hazards incomplete | **Completeness/scope drift** | Restored Biology_2 umbrella wording, incomplete-hazard uncertainty/limitation, RT/REF links; v2 | RT-0008 resolved by scope restriction; REF-0011/0012/0021; Data_2 environmental completeness rule |

## Result

- **9 BIO objects required Biology_2 semantic restoration:** BIO-0002, BIO-0003, BIO-0005, BIO-0006, BIO-0007, BIO-0008, BIO-0009, BIO-0012, BIO-0014.
- **5 BIO objects required provenance reconciliation only:** BIO-0001, BIO-0004, BIO-0010, BIO-0011, BIO-0013.
- No persistent BIO IDs changed.
- No missing numerical parameters were invented.
- Existing unresolved Wave 1 items remain unresolved.
- No PUB-0001 files were modified.

## Consequential integration questions

**None identified that require new scientific judgment.** Every semantic correction above is mechanically recoverable from canonical Biology_2 + Data_2 + RedTeam_2. The addition of `Output/Elimination` is already part of accepted Scientific Core semantics in Data_2, RedTeam_2 and the canonical glossary's Consumption definition; this repair applies that accepted semantic state to the two stale BIO fields.

## Required pre-integration checks

1. **Librarian verification:** confirm that the restored `supported_by` arrays faithfully mirror canonical REF relationships and that no source is being made to support a stronger clause than Evidence Base v0.1 permits.
2. **Narrow Red Team canonical-consistency check:** verify that the reconciled BIO objects match the exact corrections on which RT-0001..RT-0008 were closed.
3. Director integration review.
