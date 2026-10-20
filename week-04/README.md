# Week 4 — Product Performance Analysis

## Project
**CadetX — Heavy Suppliers Warehouse Analytics & Operations Optimization**

## Objective
Analyze product sales performance and related business patterns, including revenue by product, quantity sold, sales frequency, branch and category performance, monthly sales trends, product movement, and unusually high product revenue. Validate key sales calculations and document business recommendations.

## Analysis Areas
- Product performance: revenue, quantity sold, and unique sales-order frequency
- Branch performance: revenue by branch
- Category performance: revenue and quantity by product category
- Monthly sales trends
- ABC/Pareto classification of products by delivered sales value
- 2024 product movement based on distinct delivered orders
- IQR-based screening of unusually high product revenue
- Sales calculation and selected data-quality validation checks

## Repository Structure

### `reports/`
- `week-04-analysis-report.md` — findings, validation results, recommendations, and conclusion
- `Week_04_Analysis_Results.xlsx` — analysis results workbook

### `outputs/`
- `week_04_all_graphs.png` — combined visual overview
- `product_performance_summary.csv` — product-level delivered sales summary
- `abc_pareto_classification.csv` — ABC/Pareto classifications
- `product_movement_2024.csv` — product movement classification for 2024
- `sales_value_outlier_screening.csv` — IQR-based revenue screening
- `abc_pareto_chart.png` — ABC/Pareto chart
- `product_movement_2024_chart.png` — 2024 product movement chart

## Key Findings
The supplied analysis report identifies P015 — Engine Block EB-600 as the highest-revenue product in its analysis, CHN001 as the highest-revenue branch, and Engine as the highest-revenue category.

The delivered-sales product analysis also identifies products for further review through ABC/Pareto classification, product movement analysis, and IQR-based screening.

## Data Validation
The supplied report records no mismatches in the tested revenue calculations, no negative quantities or line totals, and successful matching of all 30 product IDs to the product master in the checks performed.

These results apply only to the documented validation checks and do not guarantee that every possible data-quality issue has been ruled out.

## Business Recommendations
1. Review inventory availability and demand for high-revenue products.
2. Evaluate low-revenue products using unit price, demand, and business importance before making stock decisions.
3. Compare branch-level demand to support stock allocation.
4. Monitor monthly revenue, quantity, and order counts for changes in performance.
5. Continue validating sales calculations and product-master relationships.

## Limitations
The supplied overview report and delivered-sales CSV outputs contain differing revenue figures for some products. These values should not be treated as directly comparable until their dataset scope and calculation definitions are verified.

An IQR-based high-revenue flag identifies a product for investigation; it does not by itself prove a data error or an unusual individual transaction.

No separate analysis notebook was supplied for every analysis step. The repository therefore contains the available reports, workbook, charts, and CSV outputs rather than claiming complete notebook-based reproducibility.

## Conclusion
The Week 4 deliverables summarize product, branch, category, and time-based performance, together with product classifications, validation findings, and recommendations. The findings can support further inventory and sales planning when interpreted alongside data scope, stock levels, cost, margin, and operational requirements.
