# Week 03 — Foundation Completion and Data Validation

## Project Overview

**Project:** Heavy Suppliers, Inventory & Warehouse Analytics  
**Programme:** CadetX  
**Phase:** Phase 1 — Foundation & Exploration  
**Sprint:** Week 03

Week 03 focuses on validating the cleaned datasets from Week 01 and the integrated datasets developed during Week 02. The objective is to assess data quality, verify dataset relationships, review inventory calculations, and check the logic behind key business metrics.

## Objectives

- Validate dataset structures, column names, data types, and row counts.
- Identify missing values, duplicate records, and inconsistent data.
- Check primary keys, join keys, and relationships between datasets.
- Review purchase-order statuses, received dates, and delivery classifications.
- Validate sales-order identifiers, quantities, and aggregation logic.
- Examine inventory balances at the Product–Branch level.
- Review data dictionary definitions and KPI calculation methods.
- Document validation findings and issues requiring further investigation.

## Datasets Covered

### 1. Purchase Orders
- Validate purchase-order and line-level records.
- Review order statuses and received dates.
- Check supplier, product, and branch relationships.
- Review delivery classifications and distinguish unique purchase orders from line-item counts.

### 2. Sales Orders
- Validate sales-order identifiers and line-level records.
- Check missing values, duplicate rows, and quantity fields.
- Review product and branch relationships.
- Verify aggregation logic used for sales KPIs.

### 3. Stock and Inventory
- Review Product–Branch combinations.
- Examine opening stock, stock movements, running balances, and current stock.
- Identify differences between current stock and calculated balances.
- Document inventory observations requiring clarification.

### 4. Data Dictionary and KPIs
- Review column definitions and business meanings.
- Validate distinct purchase-order and sales-order counts.
- Review the Units Purchased calculation.
- Verify Procurement Spend calculations and avoid double-counting repeated header-level values.

## Validation Reports

The following reports document the Week 3 data-quality checks:

| File | Purpose |
|---|---|
| `01_dataset_structure_report.csv` | Dataset dimensions and structure |
| `02_column_and_missing_report.csv` | Column-level information and missing-value checks |
| `03_missing_values_report.csv` | Missing-value analysis |
| `04_duplicate_rows_report.csv` | Duplicate-row checks |
| `05_initial_issue_log.csv` | Initial data-quality issues and observations |
| `Week_3_Validation_Summary.md` | Summary of validation checks, findings, and limitations |

The data dictionary and validation workbook provides supporting documentation for field definitions and KPI review.

## Key Validation Findings

The initial working report recorded the following results. These figures should be checked against the corresponding integrated datasets before being used in final business reporting.

| Check | Recorded Result |
|---|---:|
| Integrated purchase-order line rows | 155,495 |
| Received line rows | 139,977 |
| Cancelled line rows | 15,418 |
| Early delivery classifications | 6,259 |
| On-time delivery classifications | 112,736 |
| Late delivery classifications | 21,082 |
| Product–Branch pairs with stock-balance differences | 14 of 180 |

### Important Data-Quality Observations

- The received and cancelled line counts total 155,395, which is 100 fewer than the recorded 155,495 integrated rows.
- Delivery classifications total 140,077, which is 100 more than the recorded received-line count.
- The current-stock and final running-balance comparison identified differences in 14 of 180 Product–Branch pairs.
- The current-stock averages and reported data-dictionary corrections require further review.

These observations should be investigated using consistent filters, the same dataset version, and the appropriate business rules. Cancelled orders without received dates should not automatically be classified as data errors.

## Repository Structure

```text
week-03/
├── README.md
├── Sprint_Notes_Week-03.docx
├── data-integrated/
│   ├── purchase_orders_integrated_03.csv
│   ├── sales_orders_integrated_03.csv
│   └── stock_inventory_integrated_03.csv
├── validation/
│   ├── 01_dataset_structure_report.csv
│   ├── 02_column_and_missing_report.csv
│   ├── 03_missing_values_report.csv
│   ├── 04_duplicate_rows_report.csv
│   ├── 05_initial_issue_log.csv
│   └── Week_3_Validation_Summary.md
└── data-dictionary/
    └── DATA DICTIONARY & VALIDATION WORKBOOK.docx
```

*Folder and file names should match the actual names used in the repository.*

## Expected Outcomes

- Documented data-quality checks across cleaned and integrated datasets.
- Validation evidence for missing values, duplicates, and dataset structures.
- Initial review of purchase-order, sales-order, and inventory logic.
- Recorded data-quality observations for follow-up.
- Supporting documentation for data dictionary and KPI definitions.
- A more reliable foundation for subsequent analytics and dashboard development.

## Week 3 Summary

Week 3 establishes a structured validation layer for the Heavy Suppliers, Inventory & Warehouse Analytics project. The reports and supporting documentation help identify data-quality concerns, examine integration consistency, and improve the reliability of downstream KPIs and dashboards.
