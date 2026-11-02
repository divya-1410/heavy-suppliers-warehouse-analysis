# Week 06: Warehouse Operations and Efficiency

## Overview

Week 06 focuses on analysing warehouse operations and efficiency across the six branches of the Heavy Suppliers dataset.

The work is divided into two parts:

- **Part 1:** Capacity and Space Utilisation
- **Part 2:** Throughput and Operational Efficiency

The week also includes Scrum Master responsibilities involving progress tracking, data validation, documentation, and coordination of team contributions.

---

## Part 1: Capacity and Space Utilisation

### Objectives

- Analyse warehouse capacity and available utilisation-related fields.
- Compare warehouse capacity across branches.
- Examine product dimensions and inventory distribution.
- Identify data limitations affecting space utilisation calculations.

### Analysis and Findings

- Analysed warehouse capacity information for six branches.
- Total recorded warehouse floor capacity: **226,080 sq. ft.**
- Delhi Central has the highest recorded capacity, while Kolkata East Depot has the lowest.
- Examined product dimensions and calculated item-level geometric volume estimates.
- Validated inventory records and identified a data-quality issue: all 180 inventory records show `current_stock` greater than `max_stock`.

### Space Utilisation Status

Actual space utilisation could not be calculated reliably because occupied floor area and usable storage volume measurements were unavailable.

Product dimensions alone are insufficient to calculate warehouse utilisation. Verified stock quantities, storage configurations, and occupied-space measurements are also required.

### Data Limitations

- Occupied warehouse floor area is unavailable.
- Usable storage volume and storage height are unavailable.
- Rack, pallet, aisle, and stacking measurements are unavailable.
- Inventory stock values require further validation.
- Available stock ledger data covers only one product at one branch.

---

## Part 2: Throughput and Operational Efficiency

<mark>Pending teammate's analysis and contribution.</mark>

This section will document:

- Inbound and outbound movement analysis.
- Branch-wise and time-based warehouse activity comparisons.
- Potential operational bottlenecks.
- Product–warehouse alignment.
- Warehouse performance indicators and comparative visualisations, where supported by the available data.

---

## Scrum Master Responsibilities

- Track completion of product, inventory, and warehouse analyses.
- Verify calculations and ensure comparable units and valid source fields are used.
- Ensure assumptions and unavailable data are documented.
- Review Phase 2 outputs for readiness for subsequent analyses.
- Maintain weekly documentation and repository organisation.
- Coordinate and review both team members' contributions.

---

## Repository Contents

The Week 06 folder will contain:

- Capacity and space utilisation analysis report.
- Branch capacity summary.
- Inventory validation results.
- Product dimension summary.
- Throughput and operational efficiency analysis.
- Supporting datasets and visualisations, where applicable.

*The repository contents and this documentation will be updated as the remaining Week 06 work is completed.*

---

## Conclusion

Week 06 aims to evaluate warehouse capacity, inventory distribution, movement activity, and operational efficiency using the available project data.

All findings will be documented with appropriate validation, assumptions, and data limitations. No unavailable measurements or unsupported performance results will be presented as actual findings.
