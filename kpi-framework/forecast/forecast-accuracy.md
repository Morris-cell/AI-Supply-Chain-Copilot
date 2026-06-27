# Forecast Accuracy

## Definition

Measures how closely forecasted demand matches actual demand over a specific period.

## Business Purpose

Evaluate the accuracy of demand planning to support procurement, inventory management, production planning, and customer service.

## Formula

Forecast Accuracy =

100% − (|Forecast Quantity − Actual Quantity| / Actual Quantity × 100%)

Alternative

Forecast Accuracy =

1 − (ABS(Forecast − Actual) / Actual)

The calculation method should be standardized across the organization.

## Required Business Concepts

### Mandatory

- Forecast Quantity
- Actual Demand Quantity

### Optional Dimensions

- Product
- Product Category
- Customer
- Region
- Sales Channel
- Forecast Version
- Forecast Period
- Business Unit

## Interpretation

Higher Forecast Accuracy indicates:

- Reliable demand planning
- Better inventory optimization
- Lower stockout risk
- Lower excess inventory

Lower Forecast Accuracy indicates:

- Poor demand prediction
- Overstock or stockout
- Higher inventory costs
- Reduced customer service level

## Root Causes

1. Seasonality not considered
2. Promotion effects ignored
3. New product uncertainty
4. Poor historical data quality
5. Demand volatility
6. Forecast process inconsistency

## Improvement Actions

1. Improve statistical forecasting models
2. Incorporate promotional plans
3. Enhance Sales & Operations Planning (S&OP)
4. Increase collaboration between Sales and Supply Chain
5. Continuously monitor forecast performance

## Related KPIs

- Forecast Bias
- MAPE
- Inventory Turnover
- DIO
- Fill Rate
- OTIF
- Supplier Lead Time

## Analysis Dependencies

### Previous Analysis

- Historical Demand
- Sales Trend
- Promotion Planning

### Current Analysis

Evaluate the accuracy of demand forecasts and identify forecasting gaps.

### Next Analysis

If Forecast Accuracy decreases:

- Analyze Forecast Bias
- Analyze MAPE
- Review Inventory Turnover
- Review Fill Rate
- Review Procurement Planning

### Trigger Conditions

Proceed when:

- Forecast Accuracy falls below target
- Stockouts increase
- Excess inventory increases
- Demand volatility increases
