# Week 02 — Data Integration, Feature Engineering & KPI Development

## Sprint Goal
Integrate the cleaned Week 1 datasets, create analytical features, validate the outputs, and document an initial KPI framework and dashboard.

## Team Deliverables

### Data Integration and Feature Engineering — Member 2
Prepared the following integrated datasets:
- `data-integration/purchase_orders_integrated.csv`
- `data-integration/sales_orders_integrated.csv`
- `data-integration/stock_inventory_integrated.csv`

The integration combines related purchase, sales, supplier, customer, product, branch, inventory and stock-ledger data. See the integration and feature-engineering reports for join strategy and documented features.

### Data Dictionary, KPI Development and Dashboard — Member 3
- `documentation/CadetX_Week_2_Analytics_Documentation.docx`
- `notebooks/Cadetx_Week_2_Project_KPIs_Validation.ipynb`
- [Open the Power BI dashboard](https://app.powerbi.com/view?r=eyJrIjoiN2I4YTQ1NzYtOWVkNi00ZTMyLWFjMGUtNTE0MmQ2YmU2MTYxIiwidCI6ImYzZmVjNjFkLTQzMDQtNGZkNC04YzRlLWJmM2VmZDBiNTNlYiJ9)

The shared dashboard contains six pages covering the supply-chain overview, sales/product performance, procurement/supplier performance, branch/warehouse performance, inventory/stock health, and customer performance.

## Data Quality Decisions
- 15,418 missing `received_date` values in the purchase dataset were checked; all correspond to Cancelled POs and are labelled `Not Received`. Keep these dates missing and do not classify these cancelled POs as `Late`.
- Use distinct `po_id` and `so_id` counts for purchase-order and sales-order metrics because integrated tables are line-level.
- `current_stock` may repeat across product-branch movement rows. Do not sum it directly; aggregate at the product-branch snapshot level.
- Stock-status conclusions require confirmation of source thresholds and units. The dashboard's all-overstocked display should be treated as a validation item, not an established business conclusion.

## Validation Caveats
The analytics documentation reports that selected Python KPI values correspond to Power BI. However, the documented `Units Purchased` value equals Procurement Spend, so that measure should be confirmed before being treated as validated. Inventory status and snapshot measures also require careful grain and threshold checks.

## Sprint Notes
See [`Sprint_Notes.docx`](Sprint_Notes.docx) for team responsibilities, integration and feature work, data-quality decisions, KPI/dashboard documentation, limitations, and submission checklist.

