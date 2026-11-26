# Forecasting Results

## 1. Overview

This folder contains the forecasting model outputs, comparison results, forecast evaluation metrics, and future demand estimates generated as part of Week 09 – Part 1: Demand and Inventory Forecasting.

The objective is to compare forecasting approaches, evaluate their performance, understand forecast errors, and generate future product demand estimates to support inventory planning.

## 2. Objectives

- Compare different forecasting models.
- Evaluate forecasting performance at pooled and product levels.
- Analyse forecast bias and prediction errors.
- Identify the best-performing model for individual products.
- Examine demand-planning implications.
- Generate future demand forecasts.

## 3. Files Included

| File | Description |
|---|---|
| `forecast_model_comparison.csv` | Comparison of forecasting models |
| `product_level_model_comparison.csv` | Model performance comparison at product level |
| `week9_pooled_wape_comparison.csv` | Comparison using pooled WAPE |
| `week9_forecast_bias_analysis.csv` | Analysis of forecast bias |
| `week9_best_model_per_product.csv` | Best-performing model identified for each product |
| `week9_model_error_summary.csv` | Summary of model forecasting errors |
| `week9_forecast_error_analysis.csv` | Detailed forecast error analysis |
| `week9_demand_planning_comparison.csv` | Comparison supporting demand-planning decisions |
| `week9_future_demand_forecasts.csv` | Future demand forecast outputs |
| `week9_future_forecast_summary.csv` | Summary of future demand forecasts |

## 4. Analysis Areas

### 4.1 Forecast Model Comparison
Comparison of forecasting models using the available evaluation results.

### 4.2 Product-Level Model Evaluation
Examination of model performance across individual products.

### 4.3 Forecast Accuracy and Bias
Evaluation of forecast errors and potential overestimation or underestimation of demand.

### 4.4 Best Model Selection
Identification of the best-performing forecasting model for each product based on the analysis criteria.

### 4.5 Future Demand Forecasting
Generation and examination of future demand estimates for planning purposes.

## 5. Key Findings

*To be updated using the actual model comparison and forecasting results.*

This section should include:
- Best-performing forecasting models.
- Forecast accuracy observations.
- Important bias and error patterns.
- Product-level forecasting insights.
- Future demand estimates.

## 6. Assumptions and Limitations

- Forecasting results depend on historical data availability, model assumptions, demand variability, and the evaluation approach used.
- Model performance was assessed using one chronological holdout period rather than repeated rolling-origin validation.
- Forecast uncertainty was not formally quantified using prediction intervals or probabilistic forecasting.
- Forecast accuracy varied by product, and no single model was best for all products.
- All models showed positive mean bias in the evaluation period.
- The 13-week forecast horizon was selected for the exercise and was not established as the optimal operational planning horizon.
- The forecast did not incorporate external explanatory variables, supplier lead times, inventory constraints or formal stockout modelling.
- The future forecast dates (January–March 2025) are based on the historical data cutoff and should not be interpreted as current forecasts.


## 7. Conclusion

The outputs in this folder provide the results of model comparison, forecast evaluation, and future demand estimation. These results support the broader objective of improving inventory planning through data-driven demand forecasting.

**Project:** Heavy Suppliers Warehouse Analysis  
**Week:** 09  
**Part:** 01 – Demand and Inventory Forecasting  
**Contributor:** Joy Peter
