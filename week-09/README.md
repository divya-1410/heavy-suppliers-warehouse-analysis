# Week 09 – Forecasting and Predictive Analytics

## Overview

Week 09 focuses on applying forecasting and predictive analytics techniques to improve demand planning, inventory management, and warehouse operations.

The objective is to use historical sales, inventory, and procurement data to understand demand patterns, identify potential inventory risks, and develop data-driven recommendations for better stock replenishment.

## Project Structure

### Part 1 – Demand and Inventory Forecasting
**Contributor:** Joy Peter

- Demand pattern analysis
- Historical sales trend analysis
- Inventory demand forecasting
- Forecast-based inventory planning

**Status:** Pending upload and integration.

### Part 2 – Stockout and Reorder Prediction
**Contributor:** Divya Gupta

This part focuses on identifying potential inventory risks and evaluating reorder-point recommendations using historical sales and procurement information.

#### Objectives
- Identify products and branches requiring reorder-policy review.
- Analyse historical demand and supplier lead times.
- Develop proposed reorder-point calculations.
- Examine safety-stock and reorder-point scenarios.
- Evaluate the reliability and limitations of the proposed approach.

#### Methodology

1. Integrated historical sales and procurement data.
2. Calculated average daily demand using delivered sales records.
3. Examined actual supplier lead times using received purchase orders.
4. Calculated proposed reorder points using:

   `Reorder Point = (Average Daily Demand × Lead Time) + Safety Stock`

5. Compared proposed reorder points against existing reorder levels.
6. Conducted scenario analysis by varying demand, lead time, and safety-stock assumptions.

#### Key Findings

- Analysed 180 product-branch inventory records.
- Historical sales data covered January 2019 to December 2024.
- The overall average daily demand was approximately 3.13 units.
- The overall median actual supplier lead time was approximately 17.9 days.
- 179 out of 180 product-branch records were flagged for reorder-policy review.
- Scenario analysis showed how changes in demand, supplier lead time, and safety stock affect proposed reorder points.

#### Important Data Limitations

The inventory master contained unreliable current-stock values, with all 180 records showing current stock above maximum stock.

Therefore:
- Confirmed stockout events could not be established.
- Actual reorder quantities were not calculated.
- The 179 flagged records represent potential reorder-policy review cases, not confirmed stockouts.
- Scenario results are sensitivity analyses, not validated demand forecasts or purchase instructions.

## Deliverables

Part 2 includes:

- Stockout and Reorder Risk Screening
- Branch-Level Risk Summary
- Category-Level Risk Summary
- Stockout Risk Indicators Findings Report
- Reorder-Point Scenario Analysis (CSV and Excel)

## Conclusion

Week 09 aims to connect historical demand analysis with predictive inventory planning. Part 2 provides an initial framework for identifying reorder-policy risks and evaluating alternative reorder-point scenarios.

The combined findings from both parts will be integrated once the demand and inventory forecasting analysis is completed.

## Future Improvements

- Integrate demand forecasting results from Part 1.
- Obtain reliable historical inventory balances.
- Incorporate confirmed stockout records.
- Validate reorder-point recommendations using historical inventory movements.
- Improve forecasting by accounting for seasonality and demand variability.

---

**Project:** Heavy Suppliers Warehouse Analysis  
**Week:** 09  
**Theme:** Forecasting and Predictive Analytics
