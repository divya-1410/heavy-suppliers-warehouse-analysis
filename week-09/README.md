# Week 09 – Forecasting and Predictive Analytics

## 1. Overview

Week 09 focuses on applying forecasting and predictive analytics techniques to improve demand planning, inventory management, and warehouse operations.

The objective is to analyse historical demand, evaluate forecasting models, estimate future product demand, identify potential inventory risks, and develop data-driven reorder-point recommendations.

The work is divided into two parts:

- **Part 1:** Demand and Inventory Forecasting
- **Part 2:** Stockout and Reorder Prediction

## 2. Project Structure

```text
Week-09/
│
├── README.md
│
├── Part 1 - Demand and Inventory Forecasting/
│   ├── README.md
│   ├── Data and Demand Analysis/
│   ├── Forecasting Results/
│   └── Reports/
│
└── Part 2 - Stockout and Reorder Prediction/
    ├── README.md
    ├── Data and Risk Analysis/
    ├── Scenario Analysis/
    └── Reports/
```

## 3. Part 1 – Demand and Inventory Forecasting

**Contributor:** Joy Peter

### Objectives

- Analyse historical product demand.
- Examine weekly and product-level demand patterns.
- Compare different forecasting models.
- Evaluate model performance using forecasting error metrics.
- Analyse forecast bias and prediction errors.
- Identify suitable forecasting models for individual products.
- Generate future demand estimates.
- Explore demand-planning applications.

### Methodology

The analysis includes:

1. Historical weekly product demand analysis.
2. Product-level demand profiling.
3. Forecast model comparison.
4. Pooled and product-level model evaluation.
5. Forecast bias and error analysis.
6. Best-model identification for individual products.
7. Future demand forecasting.
8. Demand-planning comparison.

### Deliverables

**Data and Demand Analysis**
- `weekly_product_demand.csv`
- `week9_product_demand_profile.csv`

**Forecasting Results**
- `forecast_model_comparison.csv`
- `product_level_model_comparison.csv`
- `week9_pooled_wape_comparison.csv`
- `week9_forecast_bias_analysis.csv`
- `week9_best_model_per_product.csv`
- `week9_model_error_summary.csv`
- `week9_forecast_error_analysis.csv`
- `week9_demand_planning_comparison.csv`
- `week9_future_demand_forecasts.csv`
- `week9_future_forecast_summary.csv`

**Reports**
- Demand and Inventory Forecasting findings documentation.

## 4. Part 2 – Stockout and Reorder Prediction

**Contributor:** Divya Gupta

### Objectives

- Identify potential stockout-risk indicators.
- Analyse historical product demand.
- Examine actual supplier lead times.
- Calculate proposed reorder points.
- Compare proposed reorder points against existing reorder levels.
- Evaluate safety-stock and reorder-point scenarios.
- Identify inventory policies requiring further review.

### Methodology

The analysis uses historical sales, purchase orders, and inventory information.

The proposed reorder point is calculated using:

`Reorder Point = (Average Daily Demand × Median Lead Time) + Safety Stock`

Records where the proposed reorder point exceeds the existing reorder level are flagged for reorder-policy review.

Scenario analysis is also performed by varying demand, supplier lead time, and safety-stock assumptions.

### Key Findings

- 180 product-branch inventory records analysed.
- 6 branches and 30 products covered.
- Historical sales data covered January 2019 to December 2024.
- Overall average daily demand: approximately 3.13 units.
- Overall median actual supplier lead time: approximately 17.9 days.
- 179 out of 180 records (99.44%) flagged for reorder-policy review.

### Scenario Analysis

| Scenario | Proposed Reorder Point |
|---|---:|
| Baseline | 101.24 units |
| Lower Demand (-20%) | 90.03 units |
| Higher Demand (+20%) | 112.44 units |
| Longer Lead Time (+25%) | 115.24 units |
| Higher Demand + Longer Lead Time | 140.55 units |
| Severe Stress Scenario | 177.07 units |

### Deliverables

**Data and Risk Analysis**
- `week9_stockout_reorder_risk_screening.csv`
- `week9_branch_risk_summary.csv`
- `week9_category_risk_summary.csv`
- `week9_stockout_risk_indicators_summary.xlsx`

**Scenario Analysis**
- `week9_reorder_point_scenario_analysis.csv`
- `week9_reorder_point_scenario_analysis.xlsx`

**Reports**
- Stockout Risk Indicators Findings Report.

## 5. Data Limitations

A significant data-quality issue was identified in the inventory master dataset: all 180 records showed current-stock values exceeding their respective maximum-stock values.

As a result:

- Current-stock values could not be treated as reliable.
- Confirmed historical stockout events could not be established.
- Actual reorder quantities were not calculated.
- The 179 flagged records represent reorder-policy review cases, not confirmed stockouts.
- Scenario results represent sensitivity analysis rather than validated product-specific forecasts.

Forecasting results and inventory recommendations should be interpreted within the limitations of the available datasets and analytical assumptions.

## 6. Overall Conclusion

Week 09 combines historical demand forecasting with inventory risk analysis to support better warehouse planning and operational decision-making.

Part 1 focuses on understanding demand behaviour, comparing forecasting models, and estimating future product demand.

Part 2 examines potential inventory risks, evaluates existing reorder levels, and explores alternative reorder-point scenarios using historical demand and supplier lead-time information.

Together, these analyses provide a foundation for improving demand planning, inventory replenishment policies, and data-driven warehouse operations.

## 7. Future Improvements

- Integrate demand forecasts into inventory replenishment planning.
- Improve inventory data quality and validation.
- Incorporate reliable historical stock balances.
- Obtain confirmed stockout records for predictive model validation.
- Account for seasonal demand variations and supplier lead-time variability.
- Continuously evaluate forecasting and inventory-planning performance.

---

**Project:** Heavy Suppliers Warehouse Analysis  
**Week:** 09  
**Theme:** Forecasting and Predictive Analytics  
**Contributors:** Joy Peter and Divya Gupta
