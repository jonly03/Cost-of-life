# Data_1 — EXP-0001 quantitative representation

Status: **proposed / faithful-encoding candidate for Biology_1**

Data_1 is the Data & Quantitative Modeling Desk's first representation of BIO-0001 through BIO-0014. Durable model objects are DATA-0001 through DATA-0008 in `models/registry.yaml`.

## Modeling stance

The model is intentionally **not** a table of daily human requirements. It is a constrained hybrid dynamical-system grammar that can represent stocks, flows, bounded states, capacities, processes, conditional external dependencies, initial conditions, uncertainty and multiple time horizons.

The experiment observes a living organism over

```text
W = [t0, t0 + 24 hours]
```

but no model rule equates `|W|` with a replenishment horizon.

## Core grammar

For a physiological stock:

```text
dS_i/dt = sum(inputs_i) - sum(outputs_i) + G_i
```

where `G_i` permits internal conversion/recycling. Integrating over the observation window gives a change in inventory, not automatically an external purchasing requirement.

For bounded states:

```text
x_j(t) in A_j(z, outcome)
```

where `A_j` is an outcome- and modifier-specific admissible region. If Biology/Evidence does not establish `A_j`, it stays unresolved.

For capacities:

```text
|F_k(t)| <= C_k(t)
```

when the flow/capacity relation is biologically justified. Capacity is not itself treated as a consumable.

For conditional external dependencies:

```text
D_m(t) = 1{condition_m(S,x,e,z,t)}
```

This permits, for example, thermal support to become necessary only when organism + environment cannot maintain an admissible thermal state.

## Requirement / Consumption / Replenishment

These are separate model roles.

- **Requirement**: a necessary condition, state, process, capacity or flow for a stated outcome.
- **Consumption**: throughput, use, depletion or elimination during an interval.
- **Replenishment**: restoration of an inventory from outside the organism.

Thus:

```text
Replenishment_i = R_i(S_i(t0), Delta S_i(W), outcome, H_i, modifiers)
```

and Data_1 explicitly rejects both `Replenishment_i = Consumption_i(W)` by definition and `H_i = 24h` by default.

## Biology_1 mapping

| Model | Biology claims | Representation |
|---|---|---|
| DATA-0001 | BIO-0001..BIO-0014 | General stock/flow/state/process/capacity/environment grammar |
| DATA-0002 | BIO-0001/2/3/5/6/7/8/9/10/12 | Observation vs replenishment accounting |
| DATA-0003 | BIO-0001/7/8/9 | Continuous energy flow + endogenous substrate inventories |
| DATA-0004 | BIO-0002/3/4/14 | Oxygen/CO2 flows constrained by respiratory/perfusion capacities and environment |
| DATA-0005 | BIO-0005/6/12 | Water/electrolyte stocks, regulated states and loss/input pathways |
| DATA-0006 | BIO-0008/9/10 | Nutrient-indexed inventories and heterogeneous horizons |
| DATA-0007 | BIO-0011/14 | Heat balance, bounded thermal state and conditional support |
| DATA-0008 | BIO-0012/13 | Waste processing capacities plus initial sleep/recovery state |

All fourteen Biology_1 claims therefore have at least one explicit representation.

## Failure-mode defenses

**Inventory Blindness:** every claim involving a reserve can carry `S(t0)`; external input is not inferred solely from use/loss.

**Calendar forcing:** observation window and replenishment horizon are separate variables.

**Stock/flow confusion:** stocks have inventory units; flows have inventory/time dimensions. A flow integrated over time may change a stock but is not the stock.

**State/capacity confusion:** a regulated concentration/temperature/state is not a reserve or throughput capacity.

**False precision:** null/symbolic values are valid model states. Missing biology stays missing.

**Average-as-minimum error:** the grammar has no operation that promotes a population average, RDA/AI, recommended sleep duration, resting VO2 or similar reference value into a survival threshold.

**Outcome migration:** survival, physiological stability, function, long-term health and comfort remain separate constraint layers.

## What Data_1 deliberately does not do

Data_1 does not select a reference human, estimate daily calories/water/oxygen, infer nutrient minima, choose lethal thresholds, price resources, or convert environmental requirements into commodities. Those require later validated claims and evidence.

## Known incompleteness

1. BIO-0010 is still an aggregate micronutrient claim; DATA-0006 therefore remains an indexed family rather than a parameterized set of nutrient models.
2. Biology_1 leaves most quantitative thresholds and initial stock magnitudes unresolved.
3. Environmental safety in BIO-0014 is multivariate and needs hazard-specific decomposition before numerical simulation.
4. Special-population branches are not yet explicit enough for parameterized modeling.
5. Sleep lacks a validated quantitative state variable/transfer function in Biology_1.
6. Sanitation outside the body remains downstream of internal excretion and should not be silently attached to BIO-0012.

## Data_1 acceptance proposition

Data_1 is ready for review if the question is: **Can the model encode Biology_1 without manufacturing daily quantities or erasing its distinctions?**

It is not yet a calibrated physiological simulation. Parameterization should wait for Evidence Base mapping, Biology revisions where needed, and Red Team challenges.
