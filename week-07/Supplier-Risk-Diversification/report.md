# Week 7: Supplier Risk and Diversification Analysis

## 1. Introduction

This analysis evaluates supplier dependency, procurement spend concentration, supplier diversification and delivery performance. The objective is to identify potential supplier-related risks and understand whether procurement operations depend heavily on a limited number of suppliers.

The analysis uses the integrated purchase order dataset containing supplier, product, branch, procurement and delivery information.

## 2. Dataset Overview

| Metric | Value |
|---|---:|
| Total purchase order line records | 155,495 |
| Received purchase order lines | 140,077 |
| Cancelled purchase order lines | 15,418 |
| Unique received purchase orders | 21,630 |
| Cancelled purchase orders | 2,370 |
| Number of suppliers | 8 |
| Number of branches | 6 |
| Number of products | 30 |
| Number of product categories | 15 |

Cancelled purchase orders were excluded from the primary procurement spend and received-order delivery analysis.

## 3. Supplier Spend Analysis

Total received procurement spend was approximately ₹31,202.74 crore.

Tianjin OEM Supplies recorded the highest contribution at 12.90%, followed by Shenzhen OEM Supplies at 12.64% and Hangzhou OEM Supplies at 12.58%.

The supplier contributions are relatively evenly distributed. No individual supplier contributes more than 13% of the total received procurement spend.

This suggests that the organisation does not have a major overall spend dependency on a single supplier in the analysed dataset.

## 4. Supplier Concentration Analysis

The following concentration measures were calculated:

| Metric | Result |
|---|---:|
| Largest supplier share | 12.90% |
| Top 3 supplier share | 38.12% |
| Top 5 supplier share | 63.21% |
| HHI | 1,250.46 |

The Herfindahl-Hirschman Index (HHI) was calculated by summing the squared percentage spend shares of all suppliers.

The resulting HHI indicates relatively low supplier-spend concentration. Procurement spending is distributed across multiple suppliers rather than dominated by one supplier.

## 5. Supplier Diversification

### Product Category Analysis

All eight suppliers are represented across all fifteen product categories.

This indicates that the dataset does not show a category-level single-supplier dependency.

### Branch Analysis

All eight suppliers are represented across the six branches.

The largest individual supplier shares by branch range from approximately 12.86% to 14.12%.

This indicates a broadly distributed supplier structure across the branches.

## 6. Supplier Delivery Performance

A total of 21,630 unique received purchase orders were evaluated.

| Delivery Status | Purchase Orders | Percentage |
|---|---:|---:|
| On Time | 17,392 | 80.40% |
| Late | 3,267 | 15.10% |
| Early | 971 | 4.49% |

The overall late-delivery rate is approximately 15.10%.

Hangzhou OEM Supplies has the highest supplier-specific late-delivery rate at 15.80%. Tianjin OEM Supplies has the longest recorded lead time at 28 days.

These indicators should be monitored when assessing procurement continuity and delivery reliability.

## 7. Potential Supplier Risk Assessment

The assessment considers four indicators:

1. Spend contribution: suppliers with at least 20% of total spend are flagged for concentration risk.
2. Supplier reliability: a reliability score of 3 or lower is treated as a monitoring indicator.
3. Delivery performance: a late-delivery rate more than three percentage points above the overall rate is treated as a potential concern.
4. Lead time: longer lead times are considered when prioritising supplier monitoring.

No supplier crosses the 20% spend-concentration threshold. No supplier exceeds the defined late-delivery threshold of 18.10%.

However, Tianjin OEM Supplies deserves monitoring because it combines the highest spend share, a reliability score of 3 and the longest lead time of 28 days.

Hangzhou OEM Supplies also deserves monitoring because it has the highest late-delivery rate and a relatively long lead time of 26 days.

Ningbo Distributor Supplies and Qingdao Distributor Supplies have reliability scores of 3 and should also be reviewed.

These are monitoring priorities rather than confirmed critical-supplier classifications.

## 8. Key Findings

- Procurement spend is distributed relatively evenly across eight suppliers.
- No supplier accounts for 20% or more of received procurement spend.
- The HHI of 1,250.46 indicates relatively low spend concentration.
- All suppliers are represented across all six branches and fifteen product categories.
- Approximately 80.40% of received purchase orders were delivered on time.
- The overall late-delivery rate is 15.10%.
- Tianjin OEM Supplies and Hangzhou OEM Supplies are the main monitoring priorities based on the available indicators.

## 9. Recommendations

1. Continue distributing procurement across multiple suppliers.
2. Monitor suppliers with lower reliability scores.
3. Review long-lead-time suppliers to identify opportunities for improving delivery schedules.
4. Track late-delivery rates regularly rather than relying only on aggregate performance.
5. Maintain alternative supplier options for important products.
6. Reassess supplier risk periodically using updated procurement and delivery data.

## 10. Limitations

- The analysis uses the available integrated purchase order dataset.
- Spend concentration does not independently establish operational criticality.
- Supplier reliability scores are used as provided in the dataset.
- Delivery performance is calculated using unique received purchase orders.
- The presence of multiple suppliers in a category or branch does not prove that all suppliers are interchangeable.
- The dataset's unusually even supplier coverage and spend distribution should be validated against actual procurement records before making operational decisions.
- Category-level exact spend concentration should be interpreted only after validating the underlying category-wise calculations.

## 11. Conclusion

The analysis indicates that the procurement structure is relatively diversified in terms of supplier spend, product category coverage and branch coverage.

No major single-supplier spend dependency was identified. However, delivery reliability, supplier reliability scores and longer lead times remain important monitoring areas.

Regular supplier performance reviews and continued diversification can help strengthen procurement resilience and reduce potential supply-chain disruptions.