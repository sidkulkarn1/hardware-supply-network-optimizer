## Final Summary — Disruption Scenario Analysis

### Objective
Evaluate supply network resilience under four
hypothetical operational disruptions.

### Reference Performance
- Optimized cost: **$404,131.20**
- Original demand: **6,180 units**

### Scenario Results
- **Reference**: $404,131.20; incremental cost $0.00; demand 6,180 units
- **Supplier_Disruption**: $417,631.20; incremental cost $13,500.00; demand 6,180 units
- **Demand_Surge**: $418,967.70; incremental cost $14,836.50; demand 6,336 units
- **Manufacturing_Disruption**: $405,741.20; incremental cost $1,610.00; demand 6,180 units
- **Freight_Inflation**: $413,920.45; incremental cost $9,789.25; demand 6,180 units

### Methodology
- Rebuilt the 12-week Pyomo model for every scenario.
- Applied scenario-specific changes to constraints
  or cost parameters.
- Reoptimized purchasing, production, shipments,
  and inventory decisions.
- Verified optimal solutions and independently
  replayed inventory flows.

### Interpretation
Incremental costs are measured against the original
optimized network. Demand-surge costs include the
cost of additional customer units, so they must
not be interpreted solely as disruption penalties.

### Limitations
- Hypothetical supplier and manufacturing capacities
- Deterministic demand and lead times
- No probabilistic disruption estimates
- Full service and fixed terminal inventory required
- Supplier outage represents an order-acceptance
  interruption, not cancellation of prior deliveries

### Next Steps
1. Perform capacity and cost sensitivity analysis.
2. Evaluate mitigation strategies and marginal value.
3. Develop Tableau executive dashboards.