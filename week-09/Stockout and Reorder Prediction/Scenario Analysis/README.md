# Reorder-Point Scenario Analysis

## Overview

This folder contains the scenario-based analysis conducted as part of Week 09 – Part 2: Stockout and Reorder Prediction.

The objective is to understand how changes in product demand, supplier lead times, and safety-stock requirements can affect proposed inventory reorder points.

## Files Included

| File | Description |
|---|---|
| `week9_reorder_point_scenario_analysis.csv` | Scenario analysis results in CSV format |
| `week9_reorder_point_scenario_analysis.xlsx` | Excel workbook containing scenario results and assumptions |

## Methodology

The reorder point was calculated using:

`Reorder Point = (Average Daily Demand × Lead Time) + Safety Stock`

Different operational scenarios were created by adjusting demand, lead time, and safety-stock assumptions.

## Scenario Results

| Scenario | Proposed Reorder Point |
|---|---:|
| Baseline | 101.24 units |
| Lower Demand (-20%) | 90.03 units |
| Higher Demand (+20%) | 112.44 units |
| Longer Lead Time (+25%) | 115.24 units |
| Higher Demand + Longer Lead Time | 140.55 units |
| Severe Stress Scenario | 177.07 units |

## Key Observations

- Lower demand reduces the proposed reorder point.
- Higher demand increases replenishment requirements.
- Longer supplier lead times increase the amount of stock needed to cover demand.
- Combining higher demand, longer lead times, and increased safety stock produces the highest reorder-point estimate.

## Limitations

- The scenarios use aggregate-level assumptions.
- Results are sensitivity-analysis estimates, not validated demand forecasts.
- Product-specific reorder quantities were not calculated.
- Current-stock values in the inventory master were unreliable and could not be used for replenishment calculations.

## Conclusion

The scenario analysis demonstrates how changing operational conditions can influence inventory reorder-point requirements. It provides a foundation for reviewing inventory policies and planning for different demand and supply situations.

**Project:** Heavy Suppliers Warehouse Analysis  
**Week:** 09  
**Part:** 02 – Stockout and Reorder Prediction  
**Contributor:** Divya Gupta
