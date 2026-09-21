# Editorial_1 — EXP-0001 Wave 1 terminology audit

Status: **completed first pass / proposed terminology**

## Scope

This desk reviewed the durable Wave 1 outputs available on the upstream specialist branches, with particular attention to Biology_2, Data_2, Evidence Base v0.1 + Librarian_2, and RedTeam_1. The purpose of this pass is conceptual consistency, not public narrative.

The canonical working vocabulary is proposed in `terminology/glossary.yaml` as TERM-0001 through TERM-0021.

## Semantic rules for downstream work

1. **Requirement != Consumption != Replenishment.** A required state/process/flow can be supported by initial stock or internal production and need not imply an external transaction during the observation window.
2. **Observation window != replenishment horizon.** Twenty-four hours is the EXP-0001 observation interval, not a default nutrient, water, energy, or other replenishment cadence.
3. **Stock != Flow != State != Process != Capacity.** These are different model objects. A concentration state is not a total inventory; a realized flow is not capacity; a process is not automatically a consumable.
4. **Reserve is conditional availability, not a second stock.** A reserve must point to a canonical physical stock or capacity. Body protein cannot be independently duplicated as both energy reserve and amino-acid reserve.
5. **Output/Elimination != Consumption.** CO2 exhalation and renal excretion are boundary outputs. This resolves the semantic defect identified by RT-0005 and adopted in Data_2.
6. **Resource != Environmental Condition != Delivery Mechanism != Infrastructure.** A physiological dependency does not specify the commercial or engineered means by which it is satisfied.
7. **Viability != Stability != Function != Health != Comfort.** Evidence supporting one outcome layer cannot be promoted to another without an explicit evidentiary bridge.
8. **Cost != Price.** Cost requires an accounting perspective and boundary; price is transaction-specific monetary exchange information.

## High-risk ambiguous phrases

The following phrases should not appear unqualified in later synthesis:

- "daily requirement" — specify whether this means physiological requirement, reference intake, observed turnover, recommended intake, or external replenishment during W.
- "water requirement" — distinguish body-water state requirement, water loss/turnover, total dietary water, preformed external water, and same-window replenishment.
- "energy requirement" — distinguish continuous metabolic energy/ATP availability from external caloric intake or food purchase.
- "oxygen requirement" — distinguish tissue oxygen delivery/flux, breathable environmental access, finite short-duration internal O2 inventory, and purchased oxygen.
- "nutrient reserve" — identify the actual stock; do not imply a dedicated costless store where physiology instead mobilizes functional tissue.
- "waste requirement" — specify processing/elimination versus external sanitation or waste-management infrastructure.
- "shelter requirement" — thermal/environmental viability does not by itself establish a universal requirement for a building or housing product.
- "cost of X" — identify whose cost, what is included, the system boundary, geography/time, and whether the reported number is a cost or a market price.
- "minimum" — state the outcome threshold, population, conditions, time horizon, and evidence. A mean, recommendation, AI/RDA, turnover estimate, or safety criterion is not automatically a minimum.

## Upstream consistency findings

Biology_2 and Data_2 have already absorbed the most consequential Red Team semantic corrections: transient oxygen inventory is acknowledged; metabolic water is separated from preformed external water; amino-acid pools are separated from canonical body protein; essential-fatty-acid horizon remains unresolved; output/elimination is separated from consumption; electrolyte boundaries obey conservation; body protein has canonical ownership; and the environmental admissibility surface remains explicitly incomplete.

The Librarian audit supports these corrections and preserves the key provenance distinction: evidence for physiological mechanisms or reference values does not automatically establish a universal 24-hour external replenishment requirement.

## Economics boundary

At this pass, the durable `research/economics` branch contains no ECON claims and no substantive EXP-0001 economics note. TERM-0020 (Cost) and TERM-0021 (Price) are therefore **editorial working definitions**, not accepted economic findings. They are intentionally conservative guardrails for later mapping and should be reviewed against substantive economics work before promotion to canonical terminology.

## Publication hold

No public-facing story should yet claim that EXP-0001 has established "the cost of keeping a human alive for one day." Wave 1 has established a safer conceptual grammar for asking that question. Quantitative thresholds, population instantiation, environmental completeness, several nutrient replenishment horizons, and the economic mapping remain unresolved or incomplete.

## Recommended integration gate

Before Scientific Core / Publication synthesis is promoted:

- preserve TERM IDs and semantic distinctions during cross-branch integration;
- resolve or explicitly disposition the RT objects against revised BIO/DATA objects;
- ensure evidence relationships are integrated rather than inferred from chat;
- require economic objects to declare accounting perspective, boundary, time, geography, and the distinction between cost and price;
- reject any downstream model that converts a 24-hour observation window into a same-day purchase/replenishment assumption without an explicit dependency and initial-state argument.
