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
