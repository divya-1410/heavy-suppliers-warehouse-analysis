# WEEK 08 — Customer Analytics and Segmentation

## Project Overview

Week 08 focuses on analysing customer purchasing behaviour, customer segmentation, historical customer value, repeat purchasing patterns, retention and potential customer risk.

The objective is to understand how customers interact with the business, identify valuable customer groups, evaluate purchasing frequency and examine customer retention patterns using historical sales data.

The week's analysis combines customer purchase behaviour and RFM segmentation with customer value, repeat purchase and cohort retention analysis.

## Objectives

- Analyse customer purchasing behaviour using completed sales orders.
- Evaluate customer purchase frequency and monetary contribution.
- Apply Recency, Frequency and Monetary (RFM) analysis to segment customers.
- Identify high-value customers using historical purchase value.
- Examine repeat purchase behaviour and customer retention.
- Analyse customer cohorts based on their first purchase month.
- Identify potential at-risk customers using documented behavioural indicators.
- Present findings through interactive dashboards and supporting visualisations.

## Dataset Overview

The analysis uses the integrated sales and customer datasets.

| Dataset Metric | Value |
|---|---:|
| Sales line records | 130,402 |
| Distinct sales orders | 20,000 |
| Total customers | 500 |
| Analysis period | 2019–2024 |

Sales records were aggregated to the order level before calculating customer-level metrics to avoid counting multiple product lines as separate orders.

## Methodology

### 1. Data Validation and Order Analysis

- Checked missing values, duplicate records, customer identifiers, order identifiers and date fields.
- Validated order-level monetary calculations.
- Reconciled aggregated line-level values with reported order totals.
- Analysed delivered and cancelled orders separately.
- Excluded cancelled orders from completed-purchase frequency and monetary calculations.

### 2. Customer Purchase Behaviour and RFM Segmentation

Customer purchasing behaviour was analysed using completed orders.

The RFM framework was applied using:

- **Recency:** Days since the customer's latest delivered order.
- **Frequency:** Number of delivered orders placed by the customer.
- **Monetary:** Total pre-GST purchase value of delivered orders.

Customers received scores from 1 to 5 for each RFM dimension and were classified into seven customer segments.

### 3. Customer Value and Retention Analysis

- Calculated historical customer value and average customer value.
- Identified high-value customers using the 80th percentile threshold.
- Measured repeat purchasing using distinct order counts.
- Examined customer retention through monthly cohort analysis.
- Identified potential at-risk customers using twice the median historical purchase interval as the risk threshold.
- Compared historical customer value across customer types.

## Key Findings

### Order and Purchase Analysis

| Metric | Result |
|---|---:|
| Total distinct orders | 20,000 |
| Delivered orders | 18,033 (90.17%) |
| Cancelled orders | 1,967 (9.84%) |
| Customers with completed purchases | 500 |
| Completed pre-GST purchase value | 22,958,987,430 |

### RFM Customer Segmentation

The analysis classified customers into seven behavioural segments.

| Customer Segment | Customers | Percentage |
|---|---:|---:|
| At Risk - Low Recency | 118 | 23.6% |
| Hibernating Customers | 82 | 16.4% |
| Potential Loyalists | 70 | 14.0% |
| Champions | 68 | 13.6% |
| Loyal Customers | 67 | 13.4% |
| Other Customers | 58 | 11.6% |
| Recent Customers | 37 | 7.4% |

The At Risk - Low Recency segment represents customers with relatively low recency scores despite having made purchases frequently in the past. This is a behavioural indicator and does not independently confirm churn.

### Customer Value and Retention

| Metric | Result |
|---|---:|
| Total customers | 500 |
| Historical customer value | 22,958,987,430 |
| Average customer value | 45,917,974.86 |
| High-value customers | 100 |
| Repeat customers | 500 |
| One-time customers | 0 |
| Repeat purchase rate | 100% |
| Potential at-risk customers | 134 (26.8%) |

The potential at-risk indicator is based on the customer's historical purchase interval and is a heuristic rather than confirmed churn.

## Customer Type Analysis

Customer purchasing value was also compared across five customer types:

- Corporate
- Dealer
- Fleet Owner
- Government
- Retail

The analysis compared customer counts, total purchase value, average purchase value and order frequency across these groups.

The customer-type consistency validation identified one consistent customer type for each of the 500 customers in the supplied report.

## Dashboards and Visualisations

Week 08 includes interactive dashboards and supporting visualisations for customer purchase behaviour, RFM segmentation, customer value and retention.

**Published Power BI Dashboard:**

[Open the Week 08 Power BI Dashboard](https://app.powerbi.com/view?r=eyJrIjoiMzJkYjZhOGQtYmVmNC00NDJmLWIxYjgtYjk4ZDAxNjA0NTU4IiwidCI6ImYzZmVjNjFkLTQzMDQtNGZkNC04YzRlLWJmM2VmZDBiNTNlYiJ9)

Supporting visual materials include:
- Power BI dashboard screenshots.
- Purchase value by customer type.
- Order status distribution.
- Customer Value and Retention interactive HTML dashboard.

## Deliverables

The Week 08 submission includes:

- Customer purchase behaviour and RFM analysis workbook and Power BI report.
- Order-level summary and order-status analysis.
- Data validation and monetary reconciliation reports.
- Customer RFM analysis and segment distribution files.
- Customer type analysis and consistency report.
- Customer value and retention analysis CSV.
- Repeat purchase summary.
- Cohort retention analysis.
- Customer type value summary.
- Interactive customer value and retention HTML dashboard.
- Supporting dashboard screenshots and visualisations.
- Documentation of findings.
- Week 08 Sprint Notes.

## Data Limitations and Considerations

- RFM calculations use delivered orders only.
- The RFM reference date is January 1, 2025, based on the latest order date of December 31, 2024.
- RFM classifications depend on the scoring and segmentation rules applied.
- Historical customer value is descriptive and is not predictive Customer Lifetime Value.
- Potential at-risk customers are identified using a purchase-gap heuristic and should not be treated as confirmed churn.
- The RFM At Risk - Low Recency segment and the separate retention-based potential at-risk indicator use different definitions.
- Cohort retention reflects observed historical purchasing behaviour and does not establish the causes of customer retention or loss.

## Conclusion

Week 08 provides a consolidated view of customer purchasing behaviour, customer segmentation, historical value and retention patterns.

The analysis identified 20,000 distinct sales orders and 500 customers, with 18,033 delivered orders. RFM analysis classified customers into seven behavioural segments, while the customer value and retention analysis identified 100 high-value customers and 134 potential at-risk customers using its defined purchase-gap heuristic.

The combined findings provide a foundation for understanding customer purchasing patterns, identifying valuable customer groups and supporting further customer retention analysis.

---

**Phase 3 — Supplier, Customer and Predictive Analytics**

**Week 08 Status: Analysis and documentation completed.**
