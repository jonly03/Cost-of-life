# EXP-0001 Evidence Base v0.1 — Librarian claim map

Status: **review-ready / claim acceptance remains outside Librarian authority**

This artifact maps Biology_1 BIO-0001 through BIO-0014 to registered REF objects. A mapping means that the source supports the stated proposition **within the qualification shown here**. It does not mean that every clause, population, threshold, or model inference in a compound BIO claim was directly measured by every mapped source.

## Claim-level evidence map

| BIO claim | Registered evidence | Librarian finding |
|---|---|---|
| BIO-0001 cellular energy / ATP | REF-0002, REF-0023 | **Supported at mechanism/whole-body energy level.** Continuous cellular ATP regeneration is foundational physiology. External food replenishment cadence is separate. |
| BIO-0002 oxygen delivery | REF-0001, REF-0016 | **Supported with qualification.** The oxygen cascade and dependence of aerobic metabolism on ongoing delivery are strongly supported. No universal quantitative reserve or ambient-O2 threshold is established here. |
| BIO-0003 CO2 elimination | REF-0015 | **Supported at mechanism level.** Respiratory CO2 removal is integral to acid-base homeostasis. Exact ventilation and tolerance limits remain state-dependent. |
| BIO-0004 circulation/perfusion | REF-0001, REF-0016 | **Supported.** Perfusion is part of oxygen/substrate transport and metabolite/heat distribution. No universal cardiac-output minimum is supported. |
| BIO-0005 body water/osmolality | REF-0004, REF-0013, REF-0019 | **Strongly supported with anti-calendar qualification.** Body-water state, regulation, losses and large variation in turnover are supported. AI/turnover must not become a 24-hour drinking-water minimum. |
| BIO-0006 electrolyte homeostasis | REF-0004, REF-0005, REF-0015, REF-0019 | **Supported at regulated-state level.** Dietary reference values do not establish acute survival minima or same-day replacement. |
| BIO-0007 metabolic substrate reserves | REF-0002, REF-0003, REF-0014, REF-0017 | **Supported for appropriately scoped stocked adults; population qualification is essential.** Direct 24-hour fasting evidence plus fasting physiology supports endogenous substrate bridging. |
| BIO-0008 indispensable amino acids | REF-0003 | **Partially supported / horizon unresolved.** Exogenous essentiality is authoritative; precise reserve/turnover horizon is not directly quantified by the current evidence base. |
| BIO-0009 essential fatty acids | REF-0003, REF-0022 | **Supported with population qualification.** Essentiality is established and deficiency literature supports separation from a universal same-day intake rule. Exact healthy-person depletion horizon remains unresolved. |
| BIO-0010 micronutrients | REF-0006, REF-0007, REF-0008, REF-0009 | **Strongly supported as a heterogeneity claim.** Biology_2 still needs nutrient-specific decomposition before quantitative model use. |
| BIO-0011 thermal homeostasis | REF-0011, REF-0012, REF-0021 | **Supported.** Heat balance is multivariate and both heat/cold physiology depend on environment, activity, clothing and organismal capacity. |
| BIO-0012 waste processing / renal excretion | REF-0015, REF-0020 | **Supported with wording qualification.** Renal acid/nitrogen handling and urea/ammonia physiology are supported. Internal excretion remains distinct from sanitation infrastructure. |
| BIO-0013 sleep/recovery | REF-0010, REF-0018 | **Supported for recurring health/function dependency; no survival minimum verified.** Consensus guidance and acute-deprivation evidence do not establish a universal acute survival minimum. |
| BIO-0014 viable external environment | REF-0001, REF-0011, REF-0012, REF-0016, REF-0021 | **Supported as a multivariate boundary-condition claim, not quantitatively complete.** Contaminants, pressure bounds and other hazards need hazard-specific evidence. |

## Provenance discipline

“The source states X” and “an agent inferred Y using source X” remain separate.

- REF-0013 measures **water turnover**; it does not state a universal oral-water survival requirement.
- REF-0017 directly studies metabolism after a **24-hour fast**; it cannot establish that every human can safely omit food for 24 hours.
- REF-0010 recommends regular adult sleep duration for health; it is not a 24-hour survival minimum.
- REF-0012 provides occupational heat-protection criteria; those criteria are not universal lethal boundaries.
- REF-0003 establishes nutrient essentiality/reference requirements; it does not establish ingestion of each essential nutrient in every calendar day.

## Evidence gaps retained for Biology_2 / Red Team

1. Quantitative inspired-O2, barometric-pressure and hypercapnia boundaries remain context-specific.
2. BIO-0008 needs stronger primary evidence on amino-acid pools, protein turnover and time-to-functional-deficiency for a modeled replenishment horizon.
3. BIO-0009 needs healthy-population evidence before assigning a numeric reserve horizon.
4. BIO-0010 must be decomposed nutrient-by-nutrient for quantitative PEOM treatment.
5. BIO-0012 does not establish acute tolerable interruption durations for renal excretion.
6. BIO-0013 has no verified universal 24-hour survival threshold; accumulated sleep state at t0 matters.
7. BIO-0014 is incomplete for contaminants and pressure/hypoxia hazard surfaces.
8. Modifiers must remain parameterized; this evidence does not instantiate a universal reference human.

## Librarian conclusion

Evidence Base v0.1 is sufficient to support **serious Red Team review of Biology_1**. It is not sufficient to convert the 14 claims into universal quantitative daily requirements.

The strongest cross-cutting finding is methodological: the evidence repeatedly supports separating physiological requirement from observed consumption and from external replenishment cadence. Population reference intakes, measured turnover, expenditure and safety criteria are different evidence objects and must not be silently substituted for one another.


## Librarian_2 audit after RedTeam_1

Red Team PR #9 (RT-0001 through RT-0008) was audited against the registered evidence. The following evidence dispositions supersede any broader wording in the first-pass table above where they conflict.

| Challenge | Librarian disposition | Evidence consequence |
|---|---|---|
| RT-0001 oxygen inventory | **Sustained.** | REF-0001/0016 support continuing oxygen delivery but not a literal absence of internal O2 inventory. REF-0026 adds direct support for transient body oxygen stores during apnea. BIO-0002 should be narrowed; do not parameterize store magnitude yet. |
| RT-0002 water source accounting | **Sustained.** | REF-0004/0013/0019 support water balance, and metabolic water is a legitimate inflow. The earlier evidence-map wording is corrected: external preformed water is not the sole source term. Avoid double-counting water produced from oxidized substrate. |
| RT-0003 amino-acid stock category | **Sustained and evidence strengthened.** | REF-0024 and REF-0025 distinguish dynamic amino-acid/protein turnover from a dedicated costless nutrient reserve. Fasting supply can involve body-protein proteolysis and nitrogen loss. No safe replenishment horizon is assigned. |
| RT-0004 essential-fatty-acid horizon | **Sustained.** | REF-0003 establishes essentiality; REF-0022 is specialized clinical evidence. Evidence Base v0.1 does **not** verify “>24 h under ordinary stocked conditions” as a general-population horizon. BIO-0009 should mark horizon unresolved. |
| RT-0005 elimination vs consumption | **Sustained as semantic/modeling correction.** | REF-0015/0020 describe CO2/renal elimination as output/excretion processes. They do not justify classifying those outputs as consumed external resources. |
| RT-0006 electrolyte conservation | **Sustained as model-boundary correction.** | REF-0004/0005/0015/0019 support regulated compartments and renal/homeostatic control. Internal redistribution cannot be treated as net creation of a whole-body conserved electrolyte stock. |
| RT-0007 protein double counting | **Sustained and evidence strengthened.** | REF-0024/0025 reinforce that body protein is a physical tissue inventory participating in turnover/catabolism. It must not simultaneously appear as an independent energy reserve and an independent amino-acid reserve without conservation links. |
| RT-0008 environmental completeness | **Sustained.** | Existing sources cover important oxygen and thermal dimensions, not an exhaustive environmental hazard surface. BIO-0014 is supportable only as an umbrella/decomposition claim. |

### Corrected support statuses for challenged BIO claims

- **BIO-0002:** qualified support; wording revision required before claim-level verification.
- **BIO-0003:** physiological mechanism supported; quantity-role semantics require revision.
- **BIO-0005:** physiological stock/flow claim supported after inclusion of metabolic-water source.
- **BIO-0006:** biological homeostasis claim supported; downstream conservation boundary must be corrected.
- **BIO-0007:** scoped fasting/substrate claim remains supported; body-protein ownership must be canonicalized in the model.
- **BIO-0008:** essentiality supported; stock representation and replenishment horizon remain unresolved. REF-0024/0025 strengthen turnover provenance.
- **BIO-0009:** essentiality supported; claimed >24 h general replenishment horizon **not verified**.
- **BIO-0012:** renal/nitrogen mechanism supported; elimination must not be semantically collapsed into consumption.
- **BIO-0014:** umbrella environmental dependency supported; completeness **not verified**.

### Librarian_2 conclusion

RedTeam_1 does not overturn Evidence Base v0.1's central anti-calendar finding, but it identifies several places where the first-pass source mapping was too permissive. Evidence Base v0.1 is therefore retained as a provenance base with this audit as a corrective layer. The challenged clauses above should not be treated as verified until Biology_2/Data_2 adopt the corrections or provide stronger evidence.

New evidence registered in response: REF-0024 through REF-0026.
