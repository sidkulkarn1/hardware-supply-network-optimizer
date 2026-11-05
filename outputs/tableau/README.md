# Project 2 — Tableau Reporting Data Dictionary

## Purpose
Reporting datasets for the End-to-End Hardware Supply Network Optimizer portfolio project.

All network quantities, costs and capacities are hypothetical.

## Reporting Rules

- Connect each CSV as an independent Tableau data source unless a relationship has been explicitly validated.
- Do not sum executive KPIs across unrelated fact tables.
- `Week` is a planning-period index from 1 to 12.
- `Reference` means the original optimized model.
- Scenario incremental costs are not expected losses or probability-weighted risk.
- Sensitivity cost changes reflect reoptimization under changed assumptions.
- Non-optimal experiments do not have verified optimized financial values.
- Supplier and manufacturing tables represent the optimized reference solution.

## Dataset Inventory

| Dashboard | File | Rows | Grain | Purpose |
|---|---|---:|---|---|
| 01_cost | `01_cost/network_kpis.csv` | 2 | One row per plan | Executive cost, savings and service KPIs |
| 01_cost | `01_cost/network_cost_categories.csv` | 8 | One row per plan and cost category | Baseline versus optimized network costs |
| 01_cost | `01_cost/network_savings_bridge.csv` | 4 | One row per cost category | Contribution of each category to total savings |
| 02_sourcing | `02_sourcing/supplier_weekly.csv` | 72 | One row per supplier, component and order week | Optimized supplier orders and capacity utilization |
| 02_sourcing | `02_sourcing/manufacturing_weekly.csv` | 12 | One row per production week | Optimized production and plant capacity |
| 02_sourcing | `02_sourcing/component_inventory_weekly.csv` | 36 | One row per component and week | Component inventory and zero-buffer exposure |
| 03_distribution | `03_distribution/freight_modes.csv` | 8 | One row per plan, DC and freight mode | Standard versus expedited freight mix |
| 03_distribution | `03_distribution/freight_lanes.csv` | 4 | One row per transportation lane | Baseline versus optimized lane decisions |
| 03_distribution | `03_distribution/dc_weekly.csv` | 48 | One row per plan, DC and week | Customer service, shipping, inventory and storage |
| 04_risk | `04_risk/scenario_summary.csv` | 5 | One row per disruption scenario | Disruption cost and operational impact |
| 04_risk | `04_risk/scenario_costs.csv` | 20 | One row per scenario and cost category | Scenario cost decomposition |
| 04_risk | `04_risk/sensitivity_summary.csv` | 18 | One row per sensitivity experiment | Experiment cost changes and solver status |
| 04_risk | `04_risk/sensitivity_costs.csv` | 64 | One row per experiment and cost category | Sensitivity cost decomposition |
| 04_risk | `04_risk/capacity_value.csv` | 9 | One row per tested capacity expansion | Capacity savings and investment break-even value |
| 04_risk | `04_risk/freight_sensitivity.csv` | 4 | One row per freight experiment | Freight price and operational decision effects |
| 04_risk | `04_risk/demand_sensitivity.csv` | 4 | One row per demand-growth experiment | Growth feasibility and incremental supply cost |

## Recommended Tableau Relationships

Use separate sources for the initial dashboards.
Only create relationships when matching dimensions and source grains are understood.

### Dashboard 1 - What did we improve? 
- Executive cards: `network_kpis.csv`
- Cost comparison: `network_cost_categories.csv`
- Savings waterfall: `network_savings_bridge.csv`

### Dashboard 2 - What are the constraints?
- Supplier analysis: `supplier_weekly.csv`
- Production utilization: `manufacturing_weekly.csv`
- Inventory buffers: `component_inventory_weekly.csv`

### Dashboard 3 - How did we achieve savings?
- Shipping mode mix: `freight_modes.csv`
- Lane allocation: `freight_lanes.csv`
- DC inventory and service: `dc_weekly.csv`

### Dashboard 4 - What should we do next? 
- Disruption comparison: `scenario_summary.csv`
- Disruption cost categories: `scenario_costs.csv`
- Sensitivity experiments: `sensitivity_summary.csv`
- Sensitivity cost categories: `sensitivity_costs.csv`
- Capacity investment value: `capacity_value.csv`
- Freight economics: `freight_sensitivity.csv`
- Demand growth: `demand_sensitivity.csv`

## Key Metric Definitions

**Total network cost:** Procurement, manufacturing, freight and DC holding cost over 12 weeks.

**Savings:** Baseline modeled cost minus optimized modeled cost.

**Service level:** Fulfilled customer units divided by customer demand units.

**Supplier utilization:** Ordered units divided by available weekly order capacity.

**Storage utilization:** Inventory present before weekly customer fulfillment divided by DC storage capacity.

**Capacity investment value:** Modeled network cost reduction before the cost of adding capacity.

## Data Lineage

- Notebook 03: Baseline planning
- Notebook 04: Network optimization
- Notebook 05: Sourcing and manufacturing
- Notebook 06: Transportation and distribution
- Notebook 07: Disruption scenarios
- Notebook 08: Sensitivity and investment value
- Notebook 09: Tableau reporting preparation

## Important Limitations

The model is deterministic. It does not establish actual future financial savings, capital costs, probabilistic disruption risk or real-world service performance.