# Week 06: Warehouse Operations and Efficiency

## Overview

Week 06 focuses on analysing warehouse capacity, space utilisation, throughput, and operational efficiency across six warehouse branches.

The analysis combines warehouse capacity information, inventory records, product dimensions, stock movement data, and operational throughput summaries.

## 1. Capacity and Space Utilisation

### Warehouse Capacity Analysis

The recorded warehouse floor capacities are:

| Branch | Branch ID | Capacity (sq. ft.) |
|---|---|---:|
| Delhi Central | DEL001 | 45,230 |
| Pune Distribution | PUN001 | 38,750 |
| Chennai South Hub | CHN001 | 41,890 |
| Hyderabad Logistics | HYD001 | 36,210 |
| Kolkata East Depot | KOL001 | 29,880 |
| Ahmedabad West Hub | AHM001 | 34,120 |
| **Total** | | **226,080** |

**Key findings:**
- Delhi Central has the highest recorded capacity.
- Kolkata East Depot has the lowest recorded capacity.
- Total recorded capacity across the six branches is 226,080 sq. ft.

### Inventory Validation

The inventory master contains 180 records covering 30 products across six branches.

**Key findings:**
- Each branch contains 30 product records.
- No duplicate product–branch combinations were identified.
- All 180 records show `current_stock` greater than `max_stock`, indicating a significant data-quality issue requiring further validation.

### Product Dimension Analysis

Dimensions were available for all 30 products, and individual geometric volume estimates were calculated.

- Estimated item-level volume ranges from 0.000256 m³ to 0.728 m³.
- These estimates represent individual product dimensions, not total occupied warehouse volume.

### Space Utilisation Conclusion

Actual warehouse space utilisation could not be calculated reliably because occupied floor area, usable storage volume, storage height, rack and pallet measurements, and verified stock quantities were unavailable.

Therefore, no unsupported utilisation percentages were reported.

The following measures would be required:

- Floor-area utilisation = Occupied storage floor area / Usable warehouse floor area × 100
- Volumetric utilisation = Occupied inventory volume / Usable storage volume × 100

## 2. Throughput and Operational Efficiency

The warehouse movement data was analysed to understand inbound and outbound activity, branch-level throughput, time-based trends, and product–warehouse activity.

### Overall Movement Findings

| Movement Type | Transactions | Quantity |
|---|---:|---:|
| Inbound | 127,611 | 20,397,795 |
| Outbound | 107,165 | 1,124,832 |
| Adjustments | 2,454 | — |
| **Combined inbound and outbound quantity** | | **21,522,627** |

### Branch-wise Throughput

- Chennai South Hub recorded the highest branch throughput at 3,692,804.
- Ahmedabad West Hub recorded the lowest branch throughput at 3,539,666.
- Branch-wise throughput summaries were prepared to support operational comparisons.

### Additional Analysis

The analysis includes:

- Monthly throughput trends.
- Yearly inbound and outbound movement.
- Product-wise movement summaries.
- Product–branch activity comparisons.
- Warehouse operational profiles.
- Branch-level throughput comparisons.

These outputs help examine differences in warehouse activity and identify areas that may require further operational investigation.

### Data Coverage and Limitations

The available stock ledger contains 998 transactions:
- 501 inbound transactions.
- 486 outbound transactions.
- 11 adjustment transactions.

However, these records cover only product P001 at branch AHM001, limiting their usefulness for validating activity across all products and branches.

The inventory master and stock ledger also show different balances for P001 at AHM001. This requires further investigation, as the snapshot dates and reconciliation scope are not confirmed to be aligned.

## 3. Power BI Dashboard

The Week 06 operational analysis is supported by a Power BI dashboard containing warehouse movement and throughput visualisations.

[View the Week 06 Power BI Dashboard](https://app.powerbi.com/view?r=eyJrIjoiNDYxNWQzODEtNGM1NC00NzEyLTgwNGUtMjU3ZTVjMmI4ZWQ4IiwidCI6ImYzZmVjNjFkLTQzMDQtNGZkNC04YzRlLWJmM2VmZDBiNTNlYiJ9)

## 4. Scrum Master Responsibilities

- Track completion of product, inventory, and warehouse analyses.
- Verify calculations and ensure comparable units and valid source fields are used.
- Ensure assumptions and unavailable data are documented.
- Review whether Phase 2 outputs are ready for subsequent analyses.
- Maintain weekly documentation and repository organisation.
- Coordinate and review team contributions.

## 5. Repository Contents

This folder contains:

- Capacity and space utilisation analysis report.
- Branch capacity summary.
- Inventory validation results.
- Product dimension summary.
- Branch throughput summary.
- Monthly and yearly throughput summaries.
- Product movement summary.
- Product–branch activity analysis.
- Warehouse operational profile.
- Movement summary.
- Power BI dashboard link.

## 6. Overall Conclusion

Week 06 provided an overview of warehouse capacity, inventory data quality, product dimensions, and inbound and outbound throughput across the available datasets.

The analysis identified differences in recorded warehouse capacity and branch throughput, along with important inventory data-quality and coverage limitations.

While the available data supports capacity comparisons and throughput analysis, actual warehouse space utilisation cannot yet be established because occupied-space measurements and reliable inventory quantities are unavailable.

All findings are documented using the available source data, with assumptions and limitations clearly identified.
