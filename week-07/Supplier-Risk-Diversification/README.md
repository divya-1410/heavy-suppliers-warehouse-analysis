# Supplier Risk and Diversification Analysis

## Overview

This analysis evaluates supplier dependency, procurement spend concentration, supplier diversification, and potential supply-chain risks.

The objective is to understand how procurement spending is distributed across suppliers, identify suppliers that may require additional monitoring, and assess supplier coverage across product categories and operational branches.

The analysis uses the integrated purchase order dataset containing supplier, purchase order, product, branch, procurement value, and delivery-related information.

## Objectives

- Analyse supplier dependency using procurement spend and contribution measures.
- Calculate supplier-wise spend shares and concentration metrics.
- Identify potentially critical suppliers using transparent risk indicators.
- Examine supplier diversification across product categories and branches.
- Evaluate supplier delivery performance and lead-time indicators.
- Identify suppliers requiring additional monitoring.
- Document analytical methods, assumptions, findings, and limitations.

## Analysis Methodology

### 1. Supplier Spend Analysis

Procurement spend is aggregated by supplier using received purchase orders.

The analysis includes:
- Total procurement spend by supplier.
- Supplier contribution percentage.
- Supplier ranking based on procurement spend.
- Comparison of supplier-level spend distribution.

### 2. Supplier Concentration Analysis

Supplier dependency is assessed using individual and cumulative spend contributions.

The following measures are considered:
- Largest individual supplier contribution.
- Top-three supplier contribution.
- Top-five supplier contribution.
- Herfindahl-Hirschman Index (HHI).

HHI is calculated by summing the squared percentage spend shares of all suppliers.

### 3. Supplier Diversification

Supplier coverage is examined across:
- Product categories.
- Operational branches.
- Procurement activities.

The analysis identifies whether the available data indicates reliance on a limited number of suppliers within a category or branch.

### 4. Supplier Risk Assessment

Potential supplier risks are evaluated using the following indicators:

| Risk Indicator | Assessment Criteria |
|---|---|
| Spend concentration | Supplier spend share of 20% or higher |
| Reliability score | Score of 3 or lower |
| Delivery performance | Late-delivery rate more than 3 percentage points above the overall rate |
| Lead time | Relatively longer recorded supplier lead time |
| Supplier dependency | Limited supplier availability across products or branches |

These criteria are used to identify monitoring priorities. They do not independently establish that a supplier is operationally critical.

## Key Findings

### Procurement Spend Concentration

- Total received procurement spend: approximately ₹31,202.74 crore.
- Number of suppliers analysed: 8.
- Largest supplier contribution: 12.90%.
- Top-three supplier contribution: 38.12%.
- Top-five supplier contribution: 63.21%.
- HHI: approximately 1,250.46.

The findings indicate relatively low supplier spend concentration, with procurement distributed across the eight suppliers.

### Supplier Diversification

- All eight suppliers are represented across all six branches.
- All eight suppliers are represented across all fifteen product categories.
- No supplier accounts for 20% or more of total received procurement spend.

The available data therefore does not indicate a single-supplier dependency at the overall spend, branch coverage, or product-category coverage level.

### Potential Supplier Monitoring Priorities

**Tianjin OEM Supplies**
- Highest supplier spend contribution: 12.90%.
- Reliability score: 3.
- Recorded lead time: 28 days.

**Hangzhou OEM Supplies**
- Highest observed late-delivery rate: 15.80%.
- Recorded lead time: 26 days.
- Supplier spend contribution: 12.58%.

**Other suppliers requiring reliability monitoring**
- Ningbo Distributor Supplies: reliability score of 3.
- Qingdao Distributor Supplies: reliability score of 3.

These suppliers are monitoring priorities based on the available indicators, not confirmed critical suppliers.

## Supporting Files

| File | Description |
|---|---|
| `supplier_spend_analysis.csv` | Supplier-wise procurement spend, contribution, and ranking |
| `supplier_concentration_metrics.csv` | Supplier concentration measures and HHI |
| `supplier_delivery_performance.csv` | Supplier-wise received order and delivery performance |
| `category_supplier_diversification.csv` | Supplier coverage and diversification by product category |
| `branch_supplier_diversification.csv` | Supplier coverage and concentration by branch |
| `supplier_risk_assessment.csv` | Supplier risk indicators and monitoring priorities |
| `report.md` | Detailed analytical report, methodology, findings, and limitations |

## Data Handling and Assumptions

- Received purchase orders are used for the primary procurement spend analysis.
- Cancelled purchase orders are excluded from received procurement spend calculations.
- Delivery performance is calculated using unique received purchase orders rather than individual purchase order lines.
- Recorded delivery-status classifications are used for on-time, late, and early comparisons.
- Receipt-date-based delay calculations are considered only where the required date information is available.
- Supplier reliability scores and lead times are interpreted as indicators rather than definitive evidence of supplier risk.
- Supplier coverage does not necessarily establish equal capacity, quality, or substitutability.

## Limitations

- The analysis depends on the completeness and accuracy of the available integrated procurement dataset.
- Spend concentration alone cannot establish operational supplier criticality.
- Supplier reliability scores are used as provided in the source data.
- Multiple suppliers serving the same category or branch does not guarantee that they are interchangeable.
- Information about supplier contracts, production capacity, inventory buffers, and alternative sourcing would improve the risk assessment.
- The unusually even supplier spend distribution and supplier coverage should be validated against actual procurement records before making operational decisions.
- Category-level concentration findings should be interpreted using verified category-wise calculations.

## Conclusion

The supplier risk and diversification analysis indicates that procurement spend is relatively evenly distributed across the eight suppliers.

No major single-supplier spend dependency is identified in the available dataset. Supplier coverage across branches and product categories also indicates a diversified supplier structure.

However, supplier reliability scores, delivery performance, and longer lead times remain important areas for continued monitoring.

The analysis provides a structured basis for understanding supplier dependency, identifying potential risk indicators, and supporting more resilient procurement decisions.
