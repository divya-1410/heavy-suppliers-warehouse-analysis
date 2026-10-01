## Missing Value Handling

### `purchase_orders_header.received_date`

- Total records: 24,000
- Missing values: 2,370
- Missing percentage: 9.88%
- Status of all missing records: `Cancelled`

### Observation

All 2,370 records with a missing `received_date` have a
`po_status` of `Cancelled`.

This indicates structural missingness rather than a data-entry error.
A cancelled purchase order was not received, so a received date is not applicable.

### Cleaning Decision

The missing values will be retained as NULL.

No imputation or row deletion will be performed.

## Complete Dataset Validation

The complete dataset contains 12 tables. After the profiling and cleaning process, all 12 tables were validated.

| Table | Rows | Columns | Missing Values | Duplicate Rows |
|---|---:|---:|---:|---:|
| branches | 6 | 14 | 0 | 0 |
| customers | 500 | 15 | 0 | 0 |
| products | 30 | 23 | 0 | 0 |
| inventory_master | 180 | 8 | 0 | 0 |
| invoices | 18,033 | 10 | 0 | 0 |
| payments | 19,257 | 5 | 0 | 0 |
| purchase_orders_header | 24,000 | 10 | 2,370 | 0 |
| purchase_orders_lines | 155,495 | 9 | 0 | 0 |
| sales_orders_header | 20,000 | 11 | 0 | 0 |
| sales_orders_lines | 130,402 | 9 | 0 | 0 |
| stock_ledger | 237,230 | 9 | 0 | 0 |
| suppliers | 8 | 12 | 0 | 0 |

### Validation Result

- No complete duplicate rows were found across any of the 12 tables.
- The only missing values are the 2,370 `received_date` values in `purchase_orders_header`.
- These missing values correspond entirely to cancelled purchase orders and were intentionally retained.
- No rows were removed during cleaning.
- Row counts were preserved for all six detailed tables.
- The cleaned datasets were exported to the `cleaned_data` directory.
