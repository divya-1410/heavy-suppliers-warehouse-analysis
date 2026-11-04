# Heavy Suppliers Warehouse Analysis

## Project Overview

The **Heavy Suppliers Warehouse Analysis** is a collaborative 12-week Data Analytics and Business Intelligence project focused on analysing warehouse operations and business processes using multiple interconnected datasets.

The project explores purchasing, sales, inventory, suppliers, products, warehouse operations, invoices, payments, and related business activities.

The objective is to transform raw operational data into structured, validated, and meaningful insights that can support better business understanding and decision-making.

## Project Objectives

- Explore and understand the available warehouse datasets.
- Perform data profiling and data quality assessment.
- Identify primary keys, foreign keys, and relationships between datasets.
- Clean, prepare, and integrate relevant datasets.
- Validate data consistency and document discrepancies.
- Develop meaningful business and operational KPIs.
- Analyse purchasing, sales, inventory, and warehouse performance.
- Create dashboards and visualisations to communicate findings.
- Maintain structured weekly documentation and project deliverables.

## Team Members

- Divya Gupta
- Peter Joy Edet
- Mohamed Risleen Afrina

## Tools and Technologies

The project uses the following tools and formats across its analytical workflow:

- **Python** – Data processing, analysis, and calculations.
- **Power BI** – Dashboard development and data visualisation.
- **CSV** – Structured datasets and analytical outputs.
- **Excel / Spreadsheet tools** – Data inspection, validation, and reporting.
- **GitHub** – Version control, collaboration, and project documentation.

## Weekly Project Progress

### Week 01 – Dataset Exploration and Profiling

- Explored the available warehouse datasets.
- Examined table structures and column information.
- Analysed data types and dataset characteristics.
- Identified potential primary and foreign keys.
- Investigated relationships between tables.
- Performed initial data quality assessments.

**Deliverable:** Initial dataset exploration and profiling documentation.

[View Week 01](./week-01/)

### Week 02 – Data Integration

- Worked on integrating relevant datasets.
- Prepared integrated purchase order, sales order, and stock inventory datasets.
- Organised the integrated outputs for subsequent analysis.
- Examined missing values and data consistency during integration.

**Integrated datasets:**
- `purchase_orders_integrated.csv`
- `sales_orders_integrated.csv`
- `stock_inventory_integrated.csv`

**Important finding:** Missing `received_date` values in the examined purchase order records were associated with cancelled purchase orders and delivery status marked as `Not Received`. These were treated as conditionally valid missing values rather than being arbitrarily filled or removed.

**Deliverable:** Integrated datasets and data integration documentation.

[View Week 02](./week-02/)

### Week 03 – Data Validation and Documentation

- Continued work on integrated datasets.
- Performed validation checks on the prepared data.
- Documented data inconsistencies and validation observations.
- Prepared data dictionaries to explain dataset fields.
- Organised validation reports and supporting documentation.
- Carried forward unresolved discrepancies for subsequent review.

**Deliverables:**
- Integrated datasets.
- Validation reports and summary.
- Data dictionary.
- Validation workbook.
- Week 03 sprint notes.

[View Week 03](./week-03/)

### Week 04 – Data Review and Follow-up

- Continued the follow-up of discrepancies and validation items identified during earlier integration activities.
- Maintained weekly project documentation and sprint records.
- Organised the work and outstanding observations for subsequent analytical stages.

The Week 04 sprint notes are maintained in the repository as supporting project documentation.

[View Week 04](./week-04/)

### Week 05 – Inventory Analysis and Dashboard Development

Focused on examining inventory-related information and developing analytical outputs to understand stock conditions and inventory performance.

Activities included:

- Inventory analysis and preparation of supporting outputs.
- Stock health assessment and related indicators.
- Inventory valuation analysis.
- Inventory turnover analysis.
- Preparation of multiple analytical CSV outputs.
- Development and organisation of dashboard materials.
- Documentation of assumptions and provisional findings.

**Deliverables:**
- Inventory analysis workbook.
- Eight analytical CSV outputs.
- Dashboard materials.
- Week 05 README and sprint notes.

**Data note:** Stock-health, valuation, and turnover results were treated as provisional pending further validation.

[View Week 05](./week-05/)

### Week 06 – Warehouse Operations and Efficiency

Focused on warehouse capacity, space utilisation, inventory distribution, throughput, and operational efficiency across six branches.

**Warehouse Capacity Analysis**

Recorded warehouse capacity across six branches:

| Branch | Capacity (sq. ft.) |
|---|---:|
| Delhi Central | 45,230 |
| Pune Distribution | 38,750 |
| Chennai South Hub | 41,890 |
| Hyderabad Logistics | 36,210 |
| Kolkata East Depot | 29,880 |
| Ahmedabad West Hub | 34,120 |
| **Total** | **226,080** |

Delhi Central recorded the highest capacity, while Kolkata East Depot recorded the lowest.

**Inventory and Product Analysis**

- Analysed 180 inventory records covering 30 products across six branches.
- Found no duplicate product–branch combinations.
- Identified that all 180 records had `current_stock` greater than `max_stock`, requiring further source-data validation.
- Examined dimensions for all 30 products.
- Calculated individual geometric volume estimates ranging from 0.000256 m³ to 0.728 m³.

**Space Utilisation Finding**

Actual warehouse space utilisation could not be calculated because occupied floor area, usable storage volume, storage configuration, and reliable stock measurements were unavailable.

The limitation was documented instead of reporting unsupported utilisation percentages.

**Throughput and Operational Efficiency**

The available movement analysis reported:

| Movement Type | Transactions | Quantity |
|---|---:|---:|
| Inbound | 127,611 | 20,397,795 |
| Outbound | 107,165 | 1,124,832 |
| Adjustments | 2,454 | — |

Combined inbound and outbound quantity: **21,522,627**.

Additional analysis included:
- Branch-wise throughput comparisons.
- Monthly and yearly throughput trends.
- Product-wise movement summaries.
- Product–branch activity comparisons.
- Warehouse operational profiles.

Chennai South Hub recorded the highest branch throughput at 3,692,804, while Ahmedabad West Hub recorded the lowest at 3,539,666.

**Data Limitations**

The available stock ledger contained 998 transactions, but covered only one product at one branch. Therefore, it could not independently validate movement across all products and warehouses.

The dashboard transaction KPI cards also require reconciliation with the CSV transaction summaries before their figures can be treated as fully consistent.

**Deliverables:**
- Capacity and space utilisation report.
- Branch capacity summary.
- Inventory validation results.
- Product dimension summary.
- Throughput and movement summaries.
- Warehouse operational profile.
- Product–branch activity analysis.
- Power BI dashboard and screenshot.
- Week 06 documentation.

[View Week 06](./Week-06/)

## Project Repository Structure

```text
heavy-suppliers-warehouse-analysis/
│
├── cleaned_data/
│
├── power-bi/
│
├── week-01/
├── week-02/
├── week-03/
├── week-04/
├── week-05/
├── Week-06/
│
├── README.md
└── .gitattributes
```

The weekly folders contain their respective analysis files, datasets, reports, dashboards, and supporting documentation.

## Overall Project Progress

Across the first six weeks, the project has progressed through:

1. Dataset exploration and profiling.
2. Data integration.
3. Data validation and documentation.
4. Follow-up of data quality and integration observations.
5. Inventory analysis and dashboard development.
6. Warehouse capacity, space utilisation, and throughput analysis.

The work emphasises data validation, transparent assumptions, reproducible analysis, and documentation of limitations.

## Documentation and Collaboration

GitHub is used to maintain weekly deliverables, organise datasets, document analytical findings, and track project progress.

Sprint notes and weekly documentation support collaboration and help maintain continuity across the 12-week project.

---

**Project:** Heavy Suppliers Warehouse Analysis  
**Duration:** 12 Weeks  
**Current Progress:** Week 06  
**Repository:** [GitHub – Heavy Suppliers Warehouse Analysis](https://github.com/divya-1410/heavy-suppliers-warehouse-analysis)
