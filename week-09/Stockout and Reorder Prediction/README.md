# Stockout and Reorder Prediction

## 1. Overview

This part of Week 09 focuses on identifying potential inventory risks and developing data-driven reorder-point recommendations using historical sales, inventory, and procurement data.

The objective is to examine product demand, supplier lead times, existing reorder levels, and safety-stock values to identify inventory records that may require policy review.

## 2. Objectives

- Identify potential stockout-risk indicators across products and branches.
- Analyse historical product demand.
- Examine actual supplier lead times.
- Calculate proposed reorder points.
- Compare proposed reorder points with existing reorder levels.
- Conduct scenario-based reorder-point analysis.
- Evaluate the reliability and limitations of the proposed approach.

## 3. Dataset Information

The analysis uses the following integrated datasets:

| Dataset | Purpose |
|---|---|
| `sales_orders_integrated.csv` | Historical delivered sales and demand analysis |
| `purchase_orders_integrated.csv` | Received purchase orders and supplier lead-time analysis |
| `inventory_master.csv` | Existing stock, maximum stock, reorder level, and safety-stock information |
| `products.csv` | Product names and category information |

The analysis covers 180 product-branch inventory records across 6 branches and 30 products.

Historical sales data covers January 2019 to December 2024.

## 4. Methodology

### 4.1 Demand Analysis

Average daily demand was calculated using historical delivered sales quantities over the observation period.

### 4.2 Supplier Lead-Time Analysis

Actual supplier lead times were examined using received purchase orders. The median actual lead time was used for the proposed reorder-point calculation.

### 4.3 Reorder-Point Calculation

The proposed reorder point was calculated using:

`Reorder Point = (Average Daily Demand × Median Lead Time) + Safety Stock`

### 4.4 Risk Screening

The proposed reorder point was compared against the existing reorder level.

Records where the proposed reorder point exceeded the existing reorder level were flagged for reorder-policy review.

### 4.5 Scenario Analysis

Multiple scenarios were evaluated by changing:
- Daily demand
- Supplier lead time
- Safety-stock assumptions

This helped examine how changes in operational conditions could affect proposed reorder points.

## 5. Key Findings

- Total inventory records analysed: 180.
- Total branches covered: 6.
- Total products covered: 30.
- Overall average daily demand: approximately 3.13 units.
- Overall median actual supplier lead time: approximately 17.9 days.
- Records flagged for reorder-policy review: 179 out of 180 (99.44%).

The results indicate that most existing reorder levels may require review under the proposed calculation method.

## 6. Scenario Analysis

The following scenarios were evaluated:

| Scenario | Proposed Reorder Point |
|---|---:|
| Baseline | 101.24 units |
| Lower Demand (-20%) | 90.03 units |
| Higher Demand (+20%) | 112.44 units |
| Longer Lead Time (+25%) | 115.24 units |
| Higher Demand + Longer Lead Time | 140.55 units |
| Severe Stress Scenario | 177.07 units |

These are aggregate-level sensitivity scenarios and should not be interpreted as product-specific reorder instructions.

## 7. Deliverables

### Data and Risk Analysis
- `week9_stockout_reorder_risk_screening.csv`
- `week9_branch_risk_summary.csv`
- `week9_category_risk_summary.csv`
- `week9_stockout_risk_indicators_summary.xlsx`

### Scenario Analysis
- `week9_reorder_point_scenario_analysis.csv`
- `week9_reorder_point_scenario_analysis.xlsx`

### Reports
- `Week-09_Stockout_Risk_Indicators_Findings_Report.docx`

## 8. Data Limitations

A significant data-quality issue was identified in the inventory master dataset: all 180 records showed current stock values exceeding their respective maximum stock values.

Due to this issue:

- Current stock values could not be treated as reliable.
- Confirmed historical stockout events could not be established.
- Actual reorder quantities were not calculated.
- Machine-learning prediction accuracy could not be evaluated.
- The 179 flagged records represent potential reorder-policy review cases, not confirmed stockouts.

The proposed approach is therefore an initial risk-screening and sensitivity-analysis framework rather than a validated stockout prediction model.

## 9. Conclusion

The analysis provides an initial framework for evaluating inventory replenishment policies using historical demand and supplier lead-time information.

The proposed reorder-point calculations and scenario analysis highlight areas where existing reorder levels may require review. However, reliable inventory balances and confirmed stockout records are necessary for further validation and development of a more accurate predictive model.

---

**Project:** Heavy Suppliers Warehouse Analysis  
**Week:** 09  
**Part:** 02 – Stockout and Reorder Prediction  
**Contributor:** Divya Gupta
