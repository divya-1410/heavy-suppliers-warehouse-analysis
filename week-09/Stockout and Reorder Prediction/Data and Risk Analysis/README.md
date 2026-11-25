# Data and Risk Analysis

## Overview

This folder contains the data preparation outputs and risk-screening analysis conducted as part of Week 09 – Part 2: Stockout and Reorder Prediction.

The analysis focuses on identifying product-branch records that may require reorder-policy review using historical demand, supplier lead times, and existing inventory parameters.

## Files Included

| File | Description |
|---|---|
| `week9_stockout_reorder_risk_screening.csv` | Product-branch-level risk screening with demand, lead-time, reorder-point calculations, and risk flags |
| `week9_branch_risk_summary.csv` | Branch-wise summary of reorder-policy risk indicators |
| `week9_category_risk_summary.csv` | Product-category-wise summary of reorder-policy risk indicators |
| `week9_stockout_risk_indicators_summary.xlsx` | Combined Excel workbook containing branch and category risk summaries |

## Analysis Highlights

- 180 product-branch inventory records analysed.
- 6 branches and 30 products covered.
- Average daily demand: approximately 3.13 units.
- Median actual supplier lead time: approximately 17.9 days.
- 179 records flagged for reorder-policy review.

## Risk Identification Method

The proposed reorder point was calculated using:

`Reorder Point = (Average Daily Demand × Median Lead Time) + Safety Stock`

The proposed reorder point was compared with the existing reorder level.

Records where the proposed reorder point exceeded the existing reorder level were flagged for further review.

## Important Limitations

The inventory master contained unreliable current-stock values, with all 180 records showing current stock above maximum stock.

Therefore, the risk flags represent potential reorder-policy review cases and must not be interpreted as confirmed stockouts.

Actual reorder quantities were not calculated because reliable current-stock values were unavailable.

## Conclusion

The files in this folder provide the detailed data outputs and supporting summaries for evaluating inventory reorder-policy risks across products, categories, and branches.

**Project:** Heavy Suppliers Warehouse Analysis  
**Week:** 09  
**Part:** 02 – Stockout and Reorder Prediction
