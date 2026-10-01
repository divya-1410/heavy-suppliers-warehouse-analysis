## Finding 1: Missing Received Dates

**Table:** `purchase_orders_header`

**Column:** `received_date`

**Total records:** 24,000

**Missing values:** 2,370

**Missing percentage:** 9.88%

### Observation

All 2,370 records with a missing `received_date` have a
`po_status` of `Cancelled`.

### Cleaning Decision

The missing values will be retained because they represent
structural missingness. A cancelled purchase order was not
received, so a received date is not applicable.

No date imputation will be performed.
