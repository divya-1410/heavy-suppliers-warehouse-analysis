# Week 01

## Overview

Week 1 focused on understanding the Heavy Suppliers Warehouse dataset, profiling its structure and quality, validating relationships and business rules, and preparing cleaned datasets for further analysis.

## Dataset Overview

The complete dataset contains **12 related tables** covering branches, customers, products, inventory, purchasing, sales, invoices, payments, suppliers, and stock movements.

### Tables Analyzed

| Table | Rows | Columns |
|---|---:|---:|
| branches | 6 | 13 |
| customers | 500 | 15 |
| products | 30 | 23 |
| inventory_master | 180 | 8 |
| invoices | 18,033 | 10 |
| payments | 19,257 | 5 |
| purchase_orders_header | 24,000 | 10 |
| purchase_orders_lines | 155,495 | 9 |
| sales_orders_header | 20,000 | 11 |
| sales_orders_lines | 130,402 | 9 |
| stock_ledger | 237,230 | 9 |
| suppliers | 8 | 12 |

## Week 1 Activities

### 1. Data Profiling

- Examined the structure and dimensions of all 12 tables.
- Identified primary key and composite key candidates.
- Investigated repeated identifiers in invoices and payments.
- Checked for complete duplicate rows.
- Examined missing values.
- Validated foreign-key relationships.
- Checked date consistency.
- Validated financial and inventory-related values.
- Reviewed data types and formatting.

Detailed findings are documented in [`data-profiling/profiling_report.md`](data-profiling/profiling_report.md).

### 2. Data Quality Findings

- No complete duplicate rows were found across the 12 tables.
- Foreign-key validation for the investigated relationships found no unmatched records.
- No confirmed date inconsistencies requiring correction were identified.
- Invoice financial calculations showed no meaningful differences greater than ₹0.01.
- `purchase_orders_header.received_date` contains 2,370 missing values (9.88%). All correspond to cancelled purchase orders, so the missing values were retained as structural missingness.
- `inventory_master.current_stock` is substantially higher than `max_stock` across all 180 records. This was documented as a systematic anomaly and was not modified without further business-rule information.

### 3. Data Cleaning

The cleaning process focused on preserving valid business information while standardizing data where appropriate.

Changes included:

- Added numeric `warehouse_capacity_sqft` derived from `warehouse_capacity`.
- Converted customer `pincode` to text.
- Retained `dimensions_cm` in its consistent `LxWxH` format.
- Removed temporary invoice analysis columns.
- Retained structurally missing `received_date` values for cancelled purchase orders.
- Preserved all original records without unnecessary deletion or imputation.

### 4. Validation

The cleaned datasets were validated to ensure that row counts were preserved and no unintended duplicate records were introduced.

The cleaned versions of all 12 tables are available in the [`cleaned_data`](../cleaned_data) directory.

## Deliverables

- Dataset profiling report
- Data cleaning report
- Cleaned versions of all 12 datasets
- Week 1 documentation

## Next Steps

The next phase will build on the cleaned and validated dataset for further analysis, KPI development, relationship analysis, and business insights.

## Power BI Report

The Power BI report for the Heavy Suppliers Warehouse analysis is available here:

[View Power BI Dashboard](https://app.powerbi.com/view?r=eyJrIjoiMjJkMGNmZTEtYjJiOS00N2E1LThmOGYtMmY1ZDc3ODU5MzVhIiwidCI6ImYzZmVjNjFkLTQzMDQtNGZkNC04YzRlLWJmM2VmZDBiNTNlYiJ9)
