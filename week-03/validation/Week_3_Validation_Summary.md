# Week 3 — Foundation Completion and Validation

## Objective
Review Week 1 cleaned datasets and Week 2 integrated datasets. Validate dataset structures, data quality, join keys, purchase-order delivery classifications, and inventory data.

## Files reviewed by the automated checks

| Dataset file | Rows | Columns | Duplicate full rows |
|---|---:|---:|---:|
| branches.csv | 6 | 14 | 0 |
| inventory_master.csv | 180 | 8 | 0 |
| customers.csv | 500 | 15 | 0 |
| products.csv | 30 | 23 | 0 |
| payments.csv | 19257 | 5 | 0 |
| invoices.csv | 18033 | 10 | 0 |
| suppliers.csv | 8 | 12 | 0 |
| sales_orders_header.csv | 20000 | 11 | 0 |
| purchase_orders_header.csv | 24000 | 10 | 0 |
| sales_orders_lines.csv | 130402 | 9 | 0 |
| purchase_orders_lines.csv | 155495 | 9 | 0 |
| stock_ledger.csv | 237230 | 9 | 0 |

## Validation outputs

- `01_dataset_structure_report.csv`
- `02_column_and_missing_report.csv`
- `03_missing_values_report.csv`
- `04_duplicate_rows_report.csv`
- `05_initial_issue_log.csv`

## Important limitations

Automated checks identify items for review; they do not prove that every missing value or duplicate is an error. Purchase-order classifications and inventory calculations must be checked against the project business rules. No unsupported data corrections were applied by these checks.

## Pending manual review

- Confirm purchase-order delivery classification findings.
- Confirm Sales Order integration keys and relationships.
- Confirm Product–Branch inventory rules and calculations.
- Review each issue and record the final resolution or reason for leaving it unchanged.
