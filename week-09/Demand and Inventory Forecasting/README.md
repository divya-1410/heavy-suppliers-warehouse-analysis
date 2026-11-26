# Week 9: Demand and Inventory Forecasting

## Project Overview

This project focuses on demand forecasting as part of the Week 9 Supplier, Inventory and Warehouse Analysis project. The objective of this analysis was to examine historical product demand, evaluate forecasting models, and generate future demand estimates to support inventory planning and decision-making.

My contribution focused on Part 1: Demand and Inventory Forecasting, involving demand data preparation, exploratory analysis, model development, evaluation, comparison, and forecast generation.

## Objectives

- Analyse historical weekly product demand.
- Explore demand patterns and variability across products.
- Develop and evaluate forecasting models.
- Compare forecasting performance using appropriate error metrics.
- Identify the best-performing forecasting approach based on overall performance.
- Generate future demand forecasts for the 30 products.
- Document forecasting assumptions, limitations, and planning implications.

## Dataset Overview

The dataset contained weekly demand records for 30 products.

| Attribute | Description |
|---|---|
| Number of products | 30 |
| Historical observations | 9,420 product-week records |
| Observation period | December 2018 – December 2024 |
| Forecast horizon | 13 weeks |
| Forecasted products | 30 |

The historical dataset was structured at the product-week level to support time-based forecasting and model evaluation.

## Data Preparation

The historical demand dataset was reviewed and prepared for forecasting.

The preparation process included:

- Reviewing the dataset structure and variables.
- Checking the completeness of product-level weekly observations.
- Ensuring consistency in the weekly time series structure.
- Preparing the data for chronological training and testing.
- Validating forecast outputs and model comparison results.

## Train-Test Split

A chronological split was used to preserve the time-based nature of the data and avoid randomly distributing observations across training and testing sets.

| Dataset | Period | Observations |
|---|---|---:|
| Training | 31 December 2018 – 30 September 2024 | 9,030 |
| Testing | 7 October 2024 – 30 December 2024 | 390 |

The testing period contained 13 weeks of observations across 30 products.

## Forecasting Models

Four forecasting approaches were evaluated:

1. **Naive Forecast** – Uses the most recent observed demand as the forecast for future periods.
2. **Moving Average** – Uses the average of previous observations to estimate future demand.
3. **Seasonal Naive** – Uses demand from a corresponding previous seasonal period as the forecast.
4. **Exponential Smoothing** – Applies exponential weighting to historical observations to generate forecasts.

## Evaluation Metrics

The models were evaluated using the following metrics:

- **MAE (Mean Absolute Error):** Measures the average absolute difference between actual and forecasted demand.
- **RMSE (Root Mean Squared Error):** Measures forecast error while giving greater weight to larger errors.
- **WAPE (Weighted Absolute Percentage Error):** Measures forecast error relative to total actual demand.

Lower values indicate better forecasting performance.

## Model Performance Comparison

| Model | MAE | RMSE | Pooled WAPE |
|---|---:|---:|---:|
| Naive | 55.1410 | 67.9049 | 47.0940% |
| Moving Average | 48.3042 | 60.2073 | 41.2549% |
| Seasonal Naive | 52.9872 | 65.4387 | 45.2545% |
| Exponential Smoothing | 46.8581 | 58.1185 | 40.0199% |

### Key Findings

- Exponential Smoothing achieved the lowest MAE, RMSE, and pooled WAPE among the four models evaluated.
- Moving Average also demonstrated relatively strong forecasting performance.
- Seasonal Naive performed better than Naive in the overall model comparison.
- The performance differences between Exponential Smoothing and Moving Average were relatively modest.

Based on the overall evaluation results, Exponential Smoothing was selected for generating the future demand forecasts.

## Product-Level Model Performance

The best-performing model varied across products when evaluated using product-level WAPE.

| Model | Number of Products |
|---|---:|
| Moving Average | 12 |
| Exponential Smoothing | 8 |
| Naive | 6 |
| Seasonal Naive | 4 |

Although Exponential Smoothing performed best overall, Moving Average achieved the lowest WAPE for the largest number of individual products.

This demonstrates that forecasting performance was not uniform across products.

## Forecast Bias Analysis

Forecast bias was examined to understand whether the models tended to overforecast or underforecast demand.

All four models demonstrated a positive mean bias, indicating a general tendency toward overforecasting within the evaluation period.

| Model | Mean Bias |
|---|---:|
| Naive | 12.8795 |
| Moving Average | 18.2265 |
| Seasonal Naive | 7.8282 |
| Exponential Smoothing | 11.2200 |

Seasonal Naive recorded the lowest mean bias, while Moving Average recorded the highest.

This indicates that the model with the lowest overall forecast error was not necessarily the model with the lowest bias.

## Future Demand Forecasts

Exponential Smoothing was used to generate future demand forecasts for all 30 products over a 13-week horizon.

The forecast period covered 6 January 2025 to 31 March 2025.

The forecast outputs included:

- Weekly forecasted demand for each product.
- Average forecasted weekly demand per product.
- Total forecasted demand across the 13-week horizon.
- Product-level forecast summaries.

The forecasts were generated to provide demand estimates that could support inventory planning and operational decision-making.

## Demand Planning Implications

The forecasting results provide a basis for understanding expected product demand and supporting inventory planning.

The forecasts may help with:

- Demand estimation for future periods.
- Inventory planning and replenishment discussions.
- Identifying differences in expected demand across products.
- Supporting operational planning and resource allocation.

However, forecasts alone do not determine optimal stock levels or reorder quantities. Additional information such as supplier lead times, inventory availability, safety stock requirements, stockout history, and replenishment constraints would be required.

## Assumptions and Limitations

- The analysis was based on historical weekly demand data.
- The evaluation used a single chronological holdout period.
- The forecasts were generated for a 13-week horizon.
- Forecast performance may vary across individual products.
- The models demonstrated a general tendency toward overforecasting.
- The analysis did not incorporate external variables such as promotional activities, pricing changes, market conditions, or other demand drivers.
- Forecast uncertainty was not formally quantified.
- The forecast outputs represent estimates and should not be interpreted as guaranteed future demand.

## Conclusion

The analysis evaluated four forecasting approaches using historical weekly demand data for 30 products.

Exponential Smoothing achieved the best overall performance based on MAE, RMSE, and pooled WAPE and was subsequently used to generate the future demand forecasts.

The analysis also demonstrated that forecasting performance varied across products and that model selection at the aggregate level may not necessarily reflect the best-performing model for every individual product.

This work strengthened my understanding of time-series forecasting, model evaluation, forecast error analysis, and the role of predictive analytics in inventory planning.

## Files and Outputs

The forecasting analysis produced the following supporting outputs:

- `weekly_product_demand.csv`
- `forecast_model_comparison.csv`
- `product_level_model_comparison.csv`
- `week9_pooled_wape_comparison.csv`
- `week9_forecast_bias_analysis.csv`
- `week9_product_demand_profile.csv`
- `week9_best_model_per_product.csv`
- `week9_model_error_summary.csv`
- `week9_forecast_error_analysis.csv`
- `week9_demand_planning_comparison.csv`
- `week9_future_demand_forecasts.csv`
- `week9_future_forecast_summary.csv`

*Project:* Heavy Suppliers Warehouse Analysis  
*Week:* 09  
*Part:* 01 – Demand and Inventory Forecasting  
*Contributor:* Joy Peter
