# Data Profiling Report

## 1. Dataset Overview

### Objective

The objective of this analysis is to understand the structure, quality,
and relationships within the Heavy Suppliers Warehouse dataset.

The profiling includes analysis of:

- Table structures
- Columns and data types
- Row counts
- Primary and foreign keys
- Relationships between tables
- Missing values
- Data distributions
- Data quality observations

### Dataset Scope

The complete dataset contains 12 CSV tables:

1. `branches`
2. `customers`
3. `products`
4. `inventory_master`
5. `invoices`
6. `payments`
7. `purchase_orders_header`
8. `purchase_orders_lines`
9. `sales_orders_header`
10. `sales_orders_lines`
11. `stock_ledger`
12. `suppliers`

### Detailed Profiling Scope

For detailed profiling, the following six tables are being analyzed:

1. `branches`
2. `customers`
3. `products`
4. `inventory_master`
5. `invoices`
6. `payments`

---

## 2. Dataset Table Overview

| Table | Rows | Columns | Business Purpose |
|---|---:|---:|---|
| `branches` | 6 | 13 | Branch and warehouse information |
| `customers` | 500 | 15 | Customer master information |
| `products` | 30 | 23 | Product master information |
| `inventory_master` | 180 | 8 | Product inventory by branch |
| `invoices` | 18,033 | 10 | Customer invoice transactions |
| `payments` | 19,257 | 5 | Payments against invoices |
| `purchase_orders_header` | 24,000 | 10 | Purchase order information |
| `purchase_orders_lines` | 155,495 | 9 | Items within purchase orders |
| `sales_orders_header` | 20,000 | 11 | Sales order information |
| `sales_orders_lines` | 130,402 | 9 | Items within sales orders |
| `stock_ledger` | 237,230 | 9 | Stock movement records |
| `suppliers` | 8 | 12 | Supplier master information |

---

## 2.1 Detailed Table Structures

### 1. `branches`

**Rows:** 6  
**Columns:** 13

| Column | Description |
|---|---|
| `branch_id` | Unique branch identifier |
| `branch_name` | Name of the branch |
| `city` | Branch city |
| `state` | Branch state |
| `region` | Geographic region |
| `warehouse_type` | Type of warehouse |
| `warehouse_capacity` | Warehouse storage capacity |
| `service_center_available` | Service center availability |
| `manager_id` | Branch manager identifier |
| `total_employees` | Number of employees |
| `avg_monthly_revenue` | Average monthly revenue |
| `monthly_operational_cost` | Monthly operating cost |
| `market_demand_index` | Market demand indicator |

**Key observation:**  
`branch_id` is unique and can serve as the primary key.

---

### 2. `customers`

**Rows:** 500  
**Columns:** 15

| Column | Description |
|---|---|
| `customer_id` | Unique customer identifier |
| `customer_type` | Type of customer |
| `industry_sector` | Customer industry |
| `city` | Customer city |
| `state` | Customer state |
| `pincode` | Customer postal code |
| `region` | Geographic region |
| `branch_id` | Associated branch |
| `credit_limit` | Customer credit limit |
| `current_balance` | Current outstanding balance |
| `payment_terms` | Payment terms |
| `customer_since` | Customer relationship start date |
| `last_purchase` | Date of last purchase |
| `total_purchases` | Total purchase value |
| `customer_rating` | Customer rating |

**Key observation:**  
`customer_id` is unique and can serve as the primary key.

`branch_id` is a foreign-key candidate referencing `branches.branch_id`.

---

### 3. `products`

**Rows:** 30  
**Columns:** 23

| Column | Description |
|---|---|
| `product_id` | Unique product identifier |
| `product_name` | Product name |
| `category` | Product category |
| `machine_type` | Compatible machine type |
| `brand` | Product brand |
| `model_compatibility` | Compatible models |
| `unit_cost` | Product cost |
| `unit_price` | Selling price |
| `margin_percentage` | Profit margin percentage |
| `gst_rate` | GST rate |
| `weight_kg` | Product weight |
| `dimensions_cm` | Product dimensions |
| `material_type` | Material used |
| `warranty_months` | Warranty duration |
| `reorder_level` | Reorder threshold |
| `safety_stock` | Safety stock quantity |
| `max_stock_level` | Maximum stock level |
| `lead_time_days` | Supplier lead time |
| `criticality_level` | Product criticality |
| `usage_frequency` | Product usage frequency |
| `uom` | Unit of measurement |
| `last_purchase_price` | Most recent purchase price |
| `last_purchase_date` | Most recent purchase date |

**Key observation:**  
`product_id` is unique and can serve as the primary key.

---

### 4. `inventory_master`

**Rows:** 180  
**Columns:** 8

| Column | Description |
|---|---|
| `product_id` | Product identifier |
| `branch_id` | Branch identifier |
| `opening_stock` | Opening inventory quantity |
| `reorder_level` | Reorder threshold |
| `safety_stock` | Safety stock quantity |
| `max_stock` | Maximum stock level |
| `current_stock` | Current inventory quantity |
| `warehouse_bin` | Warehouse storage location |

**Key observation:**  
The combination of `product_id` and `branch_id` is unique and can serve as a composite primary key.

The table represents inventory for products across branches.

---

### 5. `invoices`

**Rows:** 18,033  
**Columns:** 10

| Column | Description |
|---|---|
| `invoice_id` | Invoice identifier |
| `so_id` | Sales order identifier |
| `customer_id` | Customer identifier |
| `branch_id` | Branch identifier |
| `invoice_date` | Invoice date |
| `due_date` | Payment due date |
| `total_order_value` | Total order value |
| `total_gst_amount` | GST amount |
| `grand_total` | Total invoice amount |
| `payment_status` | Invoice payment status |

**Key observation:**  
`invoice_id` is not unique in the current dataset and therefore cannot be treated as a unique primary key without further investigation.

---

### 6. `payments`

**Rows:** 19,257  
**Columns:** 5

| Column | Description |
|---|---|
| `payment_id` | Payment identifier |
| `invoice_id` | Related invoice identifier |
| `payment_date` | Date of payment |
| `payment_amount` | Amount paid |
| `payment_method` | Payment method |

**Key observation:**  
`payment_id` is not unique in the current dataset and requires further investigation.

`invoice_id` can occur multiple times because an invoice may have multiple payment records.

---

## 2.2 Initial Profiling Observations

- The dataset contains 12 interconnected tables covering branches,
  customers, products, inventory, purchasing, sales, invoicing,
  payments, suppliers, and stock movements.
- The six detailed tables contain master data, inventory data,
  invoice transactions, and payment transactions.
- Primary-key candidates were identified for most master tables.
- `inventory_master` uses a composite key consisting of
  `product_id` and `branch_id`.
- Repeated identifier values were observed in `invoices` and `payments`
  and require further investigation.
- Missing-value analysis identified a meaningful missing-data pattern
  in `purchase_orders_header.received_date`.
- Raw data will be preserved and no records will be removed without
  evidence of a genuine data-quality issue.

---

## 3. Duplicate and Key Analysis

### Overview

Duplicate complete rows and duplicate identifier values were checked separately.

No complete duplicate rows were identified in the detailed profiling tables.

However, duplicate identifier values were found in the `invoices` and
`payments` tables and require further investigation before any cleaning action is taken.

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

### Investigation of Repeated Invoice IDs

Repeated `invoice_id` values were investigated by comparing the
corresponding transaction records.

The investigation showed that repeated invoice IDs can occur across
different sales orders, customers, branches, and invoice dates.

For example, `INV-341709` appears in multiple records with different
`so_id`, `customer_id`, `branch_id`, and `invoice_date` values.

Therefore, these records are not exact duplicate rows.

### Cleaning Decision

The records will not be deleted because they contain different
business information.

However, `invoice_id` cannot be considered a unique primary key in
its current form. The identifier duplication will be retained and
flagged for further investigation during data validation.

### Payment ID

The `payments` table contains 19,257 records and 19,055 unique
`payment_id` values. Therefore, `payment_id` is not currently unique.

### Investigation of Repeated Payment IDs

Repeated `payment_id` values were investigated by comparing the
corresponding payment records.

The investigation showed that repeated payment IDs can occur across
different invoices, payment dates, payment amounts, and payment methods.

For example, `PAY-361416` appears in multiple records with different
`invoice_id`, `payment_date`, `payment_amount`, and `payment_method`
values.

Therefore, these records are not exact duplicate rows.

### Cleaning Decision

The records will not be deleted because they contain different
payment information.

However, `payment_id` cannot be considered a unique primary key in
its current form. The repeated identifier will be retained and
flagged for further investigation during data validation.

---

## 4. Missing Value Analysis

### Overview

Missing values were checked across all 12 CSV tables in the dataset.

All tables were found to contain complete values except for
`purchase_orders_header.received_date`.

### Finding: Missing Received Dates

**Table:** `purchase_orders_header`

**Column:** `received_date`

**Total records:** 24,000

**Missing values:** 2,370

**Missing percentage:** 9.88%

### Observation

All 2,370 records with a missing `received_date` have a
`po_status` of `Cancelled`.

This indicates that the missing values are related to the business
status of the purchase order.

### Cleaning Decision

The missing values will be retained because they represent
structural missingness.

A cancelled purchase order was not received, so a received date is
not applicable.

No date imputation will be performed.

---

## 5. Data Quality Principles

The following principles will be followed during the cleaning stage:

1. Raw data will remain unchanged.
2. Data quality issues will be identified before modification.
3. Cleaning decisions will be documented.
4. Values will not be deleted or replaced without a justified reason.
5. Valid business records will not be removed simply because an
   identifier is repeated.
6. Structural missing values will not be artificially filled.
7. Cleaned datasets will be maintained separately from the raw datasets.
8. All major cleaning decisions will be documented for reproducibility.

---

## 6. Preliminary Relationship Map

The following relationships have been identified or proposed from the
table structures and profiling results.

| Parent Table | Parent Key | Child Table | Child Key | Relationship |
|---|---|---|---|---|
| `branches` | `branch_id` | `customers` | `branch_id` | 1:N |
| `branches` | `branch_id` | `inventory_master` | `branch_id` | 1:N |
| `products` | `product_id` | `inventory_master` | `product_id` | 1:N |
| `branches` | `branch_id` | `invoices` | `branch_id` | 1:N |
| `customers` | `customer_id` | `invoices` | `customer_id` | 1:N |
| `invoices` | `invoice_id` | `payments` | `invoice_id` | 1:N |

### Relationship Notes

- `inventory_master` connects products and branches.
- A product can exist across multiple branches.
- A branch can store multiple products.
- Customers are associated with branches.
- Invoices are associated with customers and branches.
- Payments are associated with invoices.
- Because repeated `invoice_id` values were observed, the invoice-to-payment
  relationship requires additional validation before treating
  `invoice_id` as a unique parent key.

---

## 7. Preliminary Data Quality Findings

The following findings have been identified during initial profiling:

| Issue | Table | Column | Status |
|---|---|---|---|
| Repeated identifier | `invoices` | `invoice_id` | Requires investigation |
| Repeated identifier | `payments` | `payment_id` | Requires investigation |
| Structural missing values | `purchase_orders_header` | `received_date` | Valid missingness |
| Complete duplicate rows | Detailed tables | All | None identified |

These findings will be investigated further during data validation
and cleaning.

---

## 8. Next Steps

The next stages of the data preparation process are:

1. Complete investigation of repeated `payment_id` values.
2. Validate primary-key and foreign-key relationships.
3. Check data types and date fields.
4. Analyze categorical value distributions.
5. Analyze numerical distributions and potential outliers.
6. Check for invalid or inconsistent values.
7. Investigate inventory and financial anomalies.
8. Document all confirmed data-quality issues.
9. Create cleaned datasets separately from the raw data.
10. Validate the cleaned datasets before analysis.
