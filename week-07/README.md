# Week 7 – Supplier and Procurement Analytics

## Phase 3: Supplier, Customer & Predictive Analytics

## Overview

Week 7 focuses on analysing supplier and procurement performance to understand purchasing patterns, supplier reliability, procurement dependency, and potential supply-chain risks.

The analysis combines supplier contribution, purchase value, order volume, delivery performance, supplier concentration, and diversification measures to provide a comprehensive view of the supplier ecosystem.

The objective is to evaluate supplier performance using validated procurement metrics, identify potential supplier-related risks, and understand how effectively procurement is distributed across suppliers, product categories, and branches.

## Objectives

- Analyse procurement spend and purchase value across suppliers.
- Compare suppliers using purchase order volume, procurement value, and delivery performance.
- Measure supplier delivery reliability using clearly defined metrics and appropriate denominators.
- Evaluate delivery delays using available receipt-date information.
- Measure supplier dependency through spend contribution and concentration metrics.
- Identify potentially critical suppliers using transparent and consistent risk criteria.
- Examine supplier diversification across product categories and branches.
- Compare supplier performance across relevant operational dimensions where data supports the analysis.
- Document analytical methods, assumptions, findings, and limitations.
- Maintain consistent procurement KPI definitions and version-controlled analytical outputs.

## Dataset Overview

The analysis uses the integrated purchase order dataset containing procurement, supplier, product, branch, and delivery-related information.

| Dataset Metric | Records / Count |
|---|---:|
| Integrated purchase order records | 155,495 |
| Received purchase order lines | 140,077 |
| Cancelled purchase order lines | 15,418 |
| Unique received purchase orders | 21,630 |
| Cancelled purchase orders | 2,370 |
| Suppliers | 8 |
| Branches | 6 |
| Products | 30 |
| Product categories | 15 |

Cancelled purchase orders are excluded from the primary received-procurement spend and delivery-performance calculations.

## Analytical Methodology

### 1. Supplier Contribution and Procurement Analysis

Procurement spend was aggregated by supplier to evaluate individual supplier contributions.

The analysis considers:

- Total purchase value by supplier.
- Supplier-wise procurement contribution.
- Purchase order volume.
- Relative supplier performance.
- Delivery-related indicators.

Received purchase orders are used for the primary procurement spend comparison.

### 2. Supplier Delivery Reliability

Supplier delivery performance is evaluated using unique received purchase orders and their recorded delivery statuses.

The following measures are considered:

- On-time deliveries.
- Late deliveries.
- Early deliveries.
- Supplier-wise late-delivery rates.
- Overall delivery performance.

Delivery reliability is interpreted using the recorded delivery-status classification, with unique received purchase orders as the denominator.

### 3. Supplier Spend Concentration and Dependency

Supplier concentration is evaluated using individual supplier spend shares and cumulative contributions.

The analysis includes:

- Largest individual supplier contribution.
- Combined contribution of the top three suppliers.
- Combined contribution of the top five suppliers.
- Herfindahl-Hirschman Index (HHI).

HHI is calculated as the sum of squared supplier spend shares expressed as percentages.

These measures help determine whether procurement spending is concentrated among a small number of suppliers or distributed more evenly.

### 4. Supplier Diversification

Supplier diversification is examined across product categories and operational branches.

The analysis evaluates:

- Number of suppliers serving each product category.
- Supplier availability across branches.
- Largest supplier contribution within each branch.
- Potential single-supplier dependencies.
- Distribution of procurement across the supplier network.

### 5. Supplier Risk Assessment

Potential supplier risks are evaluated using transparent indicators rather than relying on a single performance measure.

The assessment considers:

- High procurement spend contribution.
- Lower supplier reliability scores.
- Higher late-delivery rates.
- Longer supplier lead times.
- Limited supplier availability for products or branches, where supported by the data.

A supplier flagged for monitoring is not automatically classified as a critical supplier. Operational criticality requires additional evidence about substitutability, product importance, and business impact.

## Key Findings

### Procurement and Supplier Concentration

- Total received procurement spend was approximately ₹31,202.74 crore.
- Eight suppliers were included in the analysis.
- The largest individual supplier contribution was approximately 12.90%.
- The top three suppliers contributed approximately 38.12% of received procurement spend.
- The top five suppliers contributed approximately 63.21%.
- The calculated HHI was approximately 1,250.46, indicating relatively low supplier spend concentration.

### Delivery Performance

Across 21,630 unique received purchase orders:

| Delivery Status | Purchase Orders | Percentage |
|---|---:|---:|
| On Time | 17,392 | 80.40% |
| Late | 3,267 | 15.10% |
| Early | 971 | 4.49% |

The overall late-delivery rate was approximately 15.10%.

### Supplier Diversification

- All eight suppliers were represented across the six branches.
- All eight suppliers were represented across the fifteen product categories.
- No single supplier accounted for 20% or more of total received procurement spend.
- Branch-level largest supplier contributions ranged from approximately 12.86% to 14.12%.

### Potential Monitoring Priorities

- Tianjin OEM Supplies has the highest spend contribution, a reliability score of 3, and the longest recorded lead time of 28 days.
- Hangzhou OEM Supplies has the highest observed late-delivery rate at approximately 15.80% and a lead time of 26 days.
- Ningbo Distributor Supplies and Qingdao Distributor Supplies have reliability scores of 3 and may require additional performance monitoring.

These suppliers are identified as monitoring priorities based on available indicators, not as confirmed critical suppliers.

## Key Deliverables

The Week 7 analysis includes the following supporting files:

| File | Description |
|---|---|
| `supplier_spend_analysis.csv` | Supplier-wise procurement spend and contribution |
| `supplier_concentration_metrics.csv` | Supplier concentration measures and HHI |
| `supplier_delivery_performance.csv` | Supplier-wise delivery performance |
| `category_supplier_diversification.csv` | Supplier coverage across product categories |
| `branch_supplier_diversification.csv` | Supplier coverage and concentration across branches |
| `supplier_risk_assessment.csv` | Supplier risk indicators and monitoring priorities |
| `report.md` | Detailed analytical report, findings, methodology, and limitations |

## Data Validation and Analytical Considerations

- Procurement spend is evaluated using received purchase orders.
- Cancelled purchase orders are excluded from received-procurement spend calculations.
- Delivery performance is calculated using unique purchase orders rather than individual purchase order lines.
- Delivery-status classifications are used consistently for on-time, late, and early delivery comparisons.
- Receipt-date-based delay calculations are considered only where the required dates are available.
- Supplier concentration is measured using spend contribution and HHI.
- Supplier coverage does not independently establish that suppliers are interchangeable.
- Supplier reliability scores and lead times are interpreted as indicators, not definitive proof of operational risk.
- The unusually even supplier coverage and spend distribution should be validated against actual procurement operations before being treated as a confirmed business structure.

## Limitations

- The analysis depends on the completeness and accuracy of the available integrated procurement dataset.
- Spend concentration alone cannot establish supplier criticality.
- Supplier reliability scores are used as provided in the source data.
- Supplier coverage across categories and branches does not necessarily indicate equal capacity, quality, or substitutability.
- Additional information about supplier contracts, production capacity, inventory buffers, product criticality, and alternative sourcing would improve risk assessment.
- Findings should be interpreted within the scope of the available records and documented assumptions.

## Conclusion

Week 7 provides an integrated view of supplier contribution, procurement performance, delivery reliability, supplier concentration, and diversification.

The available data indicates that procurement spend is relatively evenly distributed across the eight suppliers, with no major single-supplier spend dependency identified.

Although the overall supplier structure appears diversified, delivery performance, reliability scores, and longer lead times remain important monitoring areas.

Combining procurement contribution with delivery and diversification measures provides a stronger foundation for identifying potential supplier risks and supporting more resilient procurement decisions.

## Phase 3 Progress

**Week 7 – Supplier and Procurement Analytics: Completed**

This analysis establishes the supplier-related analytical foundation for the remaining activities in Phase 3: Supplier, Customer & Predictive Analytics.
