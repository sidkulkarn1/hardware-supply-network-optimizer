# End-to-End Hardware Supply Network Optimizer

## V1 Executive Summary & Final Results

**Report Date:** November 06, 2026  
**Planning Horizon:** 12 Weeks  
**Technology Stack:** Python, pandas, Pyomo, HiGHS, SQL, Tableau  
**Project Type:** Supply Chain Optimization & Decision Analytics

---

## 1. Executive Summary

This project developed an integrated optimization framework
for a hypothetical hardware supply network connecting supplier
sourcing, component inventory, manufacturing, transportation,
distribution centers, and customer fulfillment.

A rule-based baseline supply plan was compared against
a mathematical optimization model using Pyomo and HiGHS.

The optimized network reduced modeled total costs from
**$414,139.70** to **$404,131.20**,
generating **$10,008.50 in savings**,
equivalent to a **2.42% reduction**.

Both plans achieved **100% modeled customer fulfillment**.

The greatest positive source of cost improvement was
transportation optimization, generating
**$8,900.00 in freight savings**.

---

## 2. Business Problem

Hardware supply chains must coordinate multiple operational
decisions while operating under capacity, lead-time, and
inventory constraints.

These decisions include:

- Selecting suppliers and sourcing quantities.
- Planning component procurement and replenishment.
- Scheduling production against manufacturing capacity.
- Choosing transportation modes and distribution routes.
- Positioning finished-goods inventory across distribution centers.
- Meeting regional customer demand.
- Responding to supplier and manufacturing disruptions.

The objective was to minimize modeled total network cost
without sacrificing customer fulfillment.

---

## 3. Optimization Methodology

The project followed an integrated analytical workflow:

1. Import demand forecasts from Project 1.
2. Define hypothetical network operating assumptions.
3. Construct a rule-based baseline supply plan.
4. Formulate a constrained mathematical optimization model.
5. Solve the optimization problem using Pyomo and HiGHS.
6. Analyze supplier sourcing and manufacturing utilization.
7. Evaluate transportation and distribution decisions.
8. Reoptimize under hypothetical disruption scenarios.
9. Test capacity expansion and demand sensitivity.
10. Generate Tableau dashboards and executive reporting outputs.

The optimization model included supplier capacity,
supplier lead times, bill-of-materials requirements,
component inventory balance, manufacturing capacity,
transportation lane capacity, distribution center storage,
customer fulfillment, and terminal inventory constraints.

---

## 4. Financial Performance

| Performance Metric | Result |
|---|---:|
| Baseline Network Cost | $414,139.70 |
| Optimized Network Cost | $404,131.20 |
| Total Modeled Savings | $10,008.50 |
| Network Cost Reduction | 2.42% |
| Freight Savings | $8,900.00 |
| Freight Cost Reduction | 25.75% |
| Customer Fulfillment | 100.0% |

### Interpretation

Transportation optimization accounted for the largest
positive savings contribution.

The model improved coordination between production,
supplier procurement, distribution inventory, and freight
mode selection while preserving modeled service levels.

---

## 5. Sourcing and Manufacturing Performance

### Supplier Allocation

Supplier A accounted for **89.5%**
of modeled component purchasing.

This concentration reflects the optimizer's preference
for lower-cost sourcing but introduces a potential
supplier-dependence risk.

### Manufacturing Operations

| Manufacturing KPI | Result |
|---|---:|
| Total Finished-Goods Production | 5,665 units |
| Peak Weekly Production | 580 units |
| Weeks at Plant Capacity | 3 |

Manufacturing constraints were respected throughout
the optimized planning horizon.

---

## 6. Transportation and Distribution Performance

The optimized network reduced modeled freight expense
by **$8,900.00**,
equivalent to a **25.75% reduction**.

The optimization achieved these savings through
changes in standard versus expedited freight allocation,
transportation lane utilization, and timing of shipments.

Both distribution centers supported **100% customer
fulfillment** under the reference planning assumptions.

---

## 7. Disruption Scenario Analysis

The network was reoptimized under four hypothetical
operational disruptions.

| Disruption Scenario | Total Network Cost | Incremental Cost |
|---|---:|---:|
| Demand Surge | $418,967.70 | $14,836.50 |
| Supplier Disruption | $417,631.20 | $13,500.00 |
| Freight Inflation | $413,920.45 | $9,789.25 |
| Manufacturing Disruption | $405,741.20 | $1,610.00 |

### Interpretation

The largest incremental cost occurred under
**Demand Surge**,
increasing modeled network expense by
**$14,836.50**.

The demand-surge scenario included additional customer
volume, so its increase is not solely a disruption penalty.

These results demonstrate the financial consequences
of operational uncertainty under the modeled constraints.

---

## 8. Capacity Expansion Economics

The sensitivity analysis evaluated alternative
supplier and manufacturing capacity expansions.

| Capacity Lever | Extra Weekly Capacity | Gross Modeled Savings |
|---|---:|---:|
| SUP A | 405 units/week | $7,883.00 |
| Assembly Plant | 116 units/week | $508.00 |
| SUP B | 75 units/week | $0.00 |

### Highest-Value Opportunity

The best tested capacity expansion was
**SUP A**,
with **405
additional units of weekly capacity**.

This experiment generated
**$7,883.00
in gross modeled operating savings**.

Actual expansion investments, qualification costs,
and ongoing expenses must be evaluated before
treating these savings as a net investment benefit.

---

## 9. Demand Growth Sensitivity

The model was tested against additional
customer demand.

| Demand Growth | Optimized Network Cost | Status |
|---|---:|---|
| +5% | $433,341.45 | Optimal |
| +10% | $467,764.55 | Optimal |
| +15% | Not available | Infeasible |
| +20% | Not available | Infeasible |

At +5% demand growth, modeled network cost increased
by **$29,210.25 (7.23%)**.

At +10% demand growth, modeled network cost increased
by **$63,633.35 (15.75%)**.

The tested +15% and +20% scenarios were infeasible
under the current network constraints.

These experiments identify potential scalability
limitations, although they do not establish the
exact maximum feasible demand increase.

---

## 10. Executive Recommendations

### Recommendation 1 — Prioritize High-Value Capacity

Evaluate additional Supplier A capacity against
its estimated gross modeled operating savings
and the actual cost of expansion.

### Recommendation 2 — Manage Supplier Concentration

Investigate dual sourcing, contingency inventory,
and supplier diversification for critical components.

### Recommendation 3 — Improve Transportation Planning

Preserve opportunities to reduce expedited freight
through coordinated production and shipment scheduling.

### Recommendation 4 — Investigate Capacity Bottlenecks

Identify the binding constraints responsible
for demand-growth infeasibility.

Evaluate supplier capacity, production flexibility,
transportation capacity, and inventory positioning
before expanding demand commitments.

### Recommendation 5 — Build Resilience into Planning

Use disruption scenarios to evaluate the trade-offs
between operating efficiency, flexibility, and
risk exposure.

---

## 11. Executive Tableau Dashboards

Four dashboards summarize the project's results.

1. **Network Cost & Optimization Performance**
2. **Sourcing & Manufacturing Intelligence**
3. **Transportation & Distribution Intelligence**
4. **Risk, Scenario & Sensitivity Intelligence**

PDF exports are stored in:

`outputs/figures/`

The demand-growth comparison in Dashboard 4
should reflect the validated **+10% experiment**.

---

## 12. Modeling Limitations

This project uses hypothetical operating assumptions.

Important limitations include:

- Synthetic supplier, manufacturing, and distribution parameters.
- Deterministic costs, capacities, and lead times.
- No probability-weighted disruption forecasts.
- Limited demand-growth experiments.
- Simplified inventory and transportation assumptions.
- Capacity investment expenses not fully modeled.
- No guarantee that modeled savings translate
  into realized business savings.
- Results depend on the accuracy of input demand assumptions.

These limitations provide opportunities for
future model refinement and validation.

---

## 13. Conclusion

The End-to-End Hardware Supply Network Optimizer
demonstrates how mathematical optimization can
integrate sourcing, manufacturing, inventory,
transportation, and distribution decisions.

The model delivered a **2.42%
reduction in modeled network costs** while
maintaining **100.0% customer
fulfillment** under reference conditions.

Disruption and sensitivity experiments also identified
sourcing concentration, cost exposure, and
capacity limitations that should inform
future network planning decisions.

The completed project provides a foundation
for expanded stochastic modeling, deeper
supplier-risk analysis, and more advanced
hardware supply chain decision support.

---


