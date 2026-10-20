# Week 4 — Product Performance Analysis

## Project
CadetX — Heavy Suppliers Warehouse Analytics & Operations Optimization

## 1. Objective
Analyze product sales revenue, quantity sold, sales frequency,
branch performance, category performance, and monthly sales trends.
Validate key sales calculations and investigate unusually high product revenue.

## 2. Key Product Performance Findings

- Highest revenue product: P015 — Engine Block EB-600
- Revenue: 5,381,418,000
- Quantity sold: 45,222
- Sales frequency: 3,773 unique orders

- Lowest revenue product: P026
- Revenue: 13,901,640

- Highest quantity sold: P029
- Quantity: 47,066

- Highest sales frequency product: P011
- Unique orders: 3,982

## 3. Branch Performance

- Highest revenue branch: CHN001
- Revenue: 5,192,125,100
- CHN001 also recorded the highest number of unique sales orders
  among the branches analyzed.

## 4. Category Performance

- Highest revenue category: Engine
- Revenue: 8,406,075,600
- Hydraulic recorded the highest total quantity sold and the highest
  number of unique orders among the categories analyzed.

## 5. Unusually High Product Revenue Investigation

P014 — Transmission Assembly TA-800:
- Revenue: 3,760,422,500
- Quantity: 45,035
- Unique orders: 3,838
- Average unit price: 83,500
- Sold across 6 branches

P015 — Engine Block EB-600:
- Revenue: 5,381,418,000
- Quantity: 45,222
- Unique orders: 3,773
- Average unit price: 119,000
- Sold across 6 branches

These products were flagged by an IQR-based comparison of total revenue
across products. This does not by itself prove a data error or unusual
individual transaction. Their higher revenue should be interpreted in
the context of unit price, quantity, and product category.

## 6. Data Validation

- Sales records analyzed: 130,402
- Unique sales orders: 20,000
- Revenue calculation mismatches: 0
- Order-level revenue validation issues: 0
- Missing values in selected key sales columns: 0
- Duplicate (sales order ID, line number) combinations: 0
- Negative quantities: 0
- Negative line totals: 0
- Product sales frequency mismatches: 0
- Product master matching: all 30 product IDs matched successfully

Validation results apply to the checks performed and do not guarantee
that every possible data quality issue has been ruled out.

## 7. Business Recommendations

1. Review inventory availability and demand for high-revenue products
   such as P015 and P014.
2. Review P026's low revenue alongside its unit price, demand, and
   business importance before making stock decisions.
3. Compare branch-level demand to support stock allocation decisions.
4. Monitor monthly revenue, quantity, and order counts to identify
   changes in sales performance.
5. Continue validating sales calculations and product master relationships.

### Conclusion

The analysis identified differences in product, branch, and category
performance. The tested revenue calculations and selected data quality
checks passed without mismatches. These findings can support further
inventory and sales planning, while business decisions should also
consider cost, margin, stock levels, and operational requirements.

## Revenue Figure Reconciliation Note

The Week 4 product-performance report and Part 2 delivered-sales output contain different revenue totals for P014 and P015.

| Product | Week 4 report revenue | Part 2 delivered sales value |
|---|---:|---:|
| P014 — Transmission Assembly TA-800 | 3,760,422,500 | 3,302,258,000 |
| P015 — Engine Block EB-600 | 5,381,418,000 | 4,729,298,000 |

The analyses also contain different record counts: the report covers 130,402 sales records and 20,000 unique orders, while the Part 2 dataset contains 126,994 rows and 19,475 unique orders.

The exact cause of these differences has not been verified because the original analysis code is unavailable. The figures have been retained as reported in their respective outputs and should not be directly compared until the dataset scope and calculation definitions are confirmed.
