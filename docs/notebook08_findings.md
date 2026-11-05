
# Notebook 08 — Sensitivity & Decision Analysis

## Executive Summary

This analysis evaluates the sensitivity of a
hypothetical consumer electronics supply network
to capacity, freight, and demand assumptions.

All scenarios were modeled using the same 12-week
Pyomo optimization framework validated in
Notebooks 04 and 07.

## Reference Network

- Optimized cost: **$404,131.20**
- Planning horizon: **12 weeks**
- Original demand: **6,180 units**
- Customer fulfillment requirement: **100%**
- Original terminal inventory requirements: **Preserved**

## Experiment Coverage

- Supplier capacity experiments: **6**
- Manufacturing capacity experiments: **3**
- Standard freight price experiments: **4**
- Demand growth experiments: **4**
- Reference case: **1**
- Total optimization experiments: **18**

## Findings

### 1. Supplier and Manufacturing Capacity

The highest absolute modeled savings among tested capacity expansions came from **SUP_A +30%**, generating **$7,883.00** over 12 weeks before expansion costs.

Capacity savings represent an upper bound on
justifiable expansion spending for the modeled
12-week cost benefit, before accounting for
unmodeled operational and risk considerations.

### 2. Transportation Economics

At the highest tested standard freight increase (+100%), the reoptimized network cost was **$421,925.20**, compared with the original **$404,131.20**.

Freight sensitivity includes both the direct
effect of modified transportation prices
and the network's operational response.

### 3. Demand Growth

The largest tested demand increase with a verified optimal full-service solution was **+10%**. Other tested growth levels did not produce verified optimal solutions and require status-specific interpretation.

Infeasible or otherwise non-optimal outcomes
must be distinguished from verified optimal
full-service solutions.

### 4. Investment Decision Framework

For each capacity experiment, the analysis measures:

- Total savings against the original network
- Extra weekly capacity
- Additional capacity unit-weeks
- Break-even capacity premium
- Marginal value of each expansion interval

Capacity values are specific to the tested
network and planning horizon.

## Validation

- Reference model cost reconciled
- Original parameters restored after experiments
- Every optimal result independently audited
- Cost-category totals reconciled
- Tableau reporting datasets exported

## Limitations

- Hypothetical network parameters
- Deterministic 12-week optimization
- Fixed supplier and transportation lead times
- No capital expenditure estimates
- No explicit supplier reservation fees
- No probabilistic demand uncertainty
- No quantified disruption risk reduction
- Original terminal inventories preserved

## Business Recommendations

1. Prioritize capacity investments only where
   demonstrable operational value exceeds the
   full cost of implementation.
2. Use sensitivity experiments to distinguish
   genuinely binding constraints from
   apparently constrained but low-value resources.
3. Evaluate transportation decisions jointly
   with inventory and production planning.
4. Use demand-growth feasibility tests to
   identify conditions requiring capacity or
   network redesign.
5. Extend the analysis with resilience
   benefits before making final investments.

## Next Steps

1. Build executive Tableau dashboards.
2. Integrate scenario and sensitivity reporting.
3. Perform end-to-end reproducibility checks.
4. Finalize the Project 2 portfolio case study.
