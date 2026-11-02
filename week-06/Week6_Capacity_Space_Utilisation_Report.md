# Week 6 – Capacity and Space Utilisation Analysis

## 1. Objective
Assess the available warehouse-capacity and inventory fields, compare branch capacity, and determine whether a defensible space-utilisation measure can be calculated.

## 2. Branch capacity comparison
The branch-capacity figures supplied for the project are recorded in square feet. Total listed capacity is **226,080 sq ft** across six branches.

| Branch | Branch ID | Capacity (sq ft) |
|---|---|---:|
| Delhi Central | DEL001 | 45,230 |
| Chennai South Hub | CHN001 | 41,890 |
| Pune Distribution | PUN001 | 38,750 |
| Hyderabad Logistics | HYD001 | 36,210 |
| Ahmedabad West Hub | AHM001 | 34,120 |
| Kolkata East Depot | KOL001 | 29,880 |

The largest listed capacity is Delhi Central; the smallest is Kolkata East Depot. This is a comparison of **available floor-area capacity only**, not a comparison of occupied space or utilisation.

## 3. Inventory data validation
- Inventory master contains **180 rows**, **30 distinct products**, and **6 branches** (30 product-branch records per branch).
- No duplicate `(product_id, branch_id)` combinations were found.
- The `current_stock` field ranges from **88,853 to 121,013**, while `max_stock` ranges from **131 to 582**.
- **All 180 of 180 records (100%) have `current_stock > max_stock`.** The scale difference strongly suggests a field mapping, source-data, or unit/encoding problem. These current-stock values are not safe to use as physical quantities until corrected.
- `warehouse_bin` contains location-like codes (for example, C15, D16, A11); these are identifiers, not measurements of occupied area.

## 4. Product dimensions
- Product master contains **30 distinct products**.
- All **30/30** `dimensions_cm` values follow a three-dimension pattern and can be converted to a per-item geometric volume.
- Per-item calculated volume ranges from **0.000256 m³ to 0.728 m³**.
- Examples: P002 (10×8×8 cm) = 0.00064 m³; P015 (160×70×65 cm) = 0.728 m³.

These are dimension-derived item-volume estimates, not confirmed packaging or storage volumes. Because valid on-hand quantities are unavailable, aggregate inventory volume by branch cannot be reliably calculated.

## 5. Stock-ledger coverage limitation
The available stock-ledger extract contains **998 transactions**, but all rows relate to only **P001 at AHM001**, covering **2019-01-03 to 2023-09-11**. It therefore does not cover the 180 product-branch combinations in the inventory master. The latest ledger balance in this extract is 79,061 for P001/AHM001 and does not reconcile with the inventory-master current-stock value (106,714). This comparison is not a full reconciliation because the extract is limited to one product-branch pair and the snapshot dates are not established as aligned.

## 6. Can space utilisation be calculated?
**No—not defensibly from the available fields.** The branch capacity measure is floor area in square feet, whereas product dimensions provide per-item volume in cubic metres. The dataset does not provide occupied floor area, usable storage height/volume, rack or pallet dimensions, aisle allocation, stacking rules, packaging dimensions, or verified on-hand quantities.

A valid floor-area utilisation formula would require:

`Floor-area utilisation (%) = occupied storage floor area / usable warehouse floor area × 100`

A valid volumetric utilisation formula would require:

`Volumetric utilisation (%) = occupied inventory volume / usable storage volume × 100`

Neither numerator nor the necessary compatible denominator is available. Do not report a percentage by dividing item volume by square-foot capacity.

## 7. Findings and recommendations
1. Delhi Central has the highest listed floor-area capacity (45,230 sq ft); Kolkata East Depot has the lowest (29,880 sq ft).
2. The inventory master has complete product-branch coverage in row count (30 products × 6 branches), but its current-stock values fail a basic max-stock validation in every row.
3. Product dimensions are available for all 30 products, allowing per-item volume estimates only.
4. The supplied ledger extract is limited to P001/AHM001 and cannot validate branch-wide inventory balances.
5. Actual warehouse space utilisation should be marked **Not Calculable – Insufficient/Invalid Data**, rather than estimated or fabricated.

### Data required to complete utilisation analysis
- Correct, verified on-hand quantity for each product at each branch, with explicit units of measure.
- Confirmation that `max_stock` and `current_stock` columns are mapped correctly.
- Packaging dimensions or standard storage-unit dimensions.
- Usable storage height or rack/pallet capacity, occupied floor area, aisle/operational exclusions, and stacking constraints.
- Complete stock-ledger history for all product-branch combinations and a defined inventory snapshot date.

## 8. Scope note
The branch capacity comparison uses the six branch-capacity values previously supplied for this project. The attached inventory, product, and stock-ledger extracts were independently parsed and checked for this analysis. The analysis does not alter the source datasets.
