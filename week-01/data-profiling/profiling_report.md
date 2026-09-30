# Data Profiling Report

## 1. Dataset Overview

### Objective

The objective of this analysis is to understand the structure, quality, and relationships within the Heavy Suppliers Warehouse dataset.

The profiling includes analysis of:

- Table structures
- Columns and data types
- Row counts
- Primary and foreign keys
- Relationships between tables
- Missing values
- Data distributions
- Data quality issues

### Assigned Tables

For this analysis, the following six tables are being profiled:

1. `branch`
2. `customers`
3. `products`
4. `inventory_master`
5. `invoices`
6. `payments`
   
## 2. Table Structure

### 2.1 Branch

| Attribute | Value |
|---|---|
| Table Name | `branch` |
| Number of Rows | 6 |
| Number of Columns | 13 |
| Purpose | Stores information about warehouse branches and their operational details. |

### 2.2 Customers

| Attribute | Value |
|---|---|
| Table Name | `customers` |
| Number of Rows | 500 |
| Number of Columns | 15 |
| Purpose | Stores customer information, including customer type, industry, location, credit details, purchase history, payment terms, and ratings. |

### 2.3 Products

| Attribute | Value |
|---|---|
| Table Name | `products` |
| Number of Rows | 30 |
| Number of Columns | 23 |
| Purpose | Stores product master information, including product details, pricing, stock levels, lead times, warranty, and usage characteristics. |
