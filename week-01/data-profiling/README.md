## 3. Duplicate and Key Analysis

### Overview

Duplicate complete rows and duplicate identifier values were checked separately.
No complete duplicate rows were identified in the detailed profiling tables.

However, duplicate identifier values were found in the `invoices` and `payments`
tables and require further investigation before any cleaning action is taken.

| Table | Key Finding |
|---|---|
| `branches` | `branch_id` is unique |
| `customers` | `customer_id` is unique |
| `products` | `product_id` is unique |
| `inventory_master` | `product_id + branch_id` is a unique combination |
| `invoices` | `invoice_id` contains repeated values |
| `payments` | `payment_id` contains repeated values |

### Invoice ID

The `invoices` table contains 18,033 records and 17,836 unique
`invoice_id` values. Therefore, `invoice_id` is not currently unique.

### Payment ID

The `payments` table contains 19,257 records and 19,055 unique
`payment_id` values. Therefore, `payment_id` is not currently unique.

These repeated identifiers will be investigated further before determining
whether they represent data-quality issues or valid business records.
