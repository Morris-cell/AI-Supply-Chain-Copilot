# Mean Absolute Percentage Error (MAPE)

## Definition

Measures the average absolute percentage difference between forecasted demand and actual demand.

MAPE is one of the most widely used metrics for evaluating forecast performance because it expresses forecast error as a percentage.

## Business Purpose

Evaluate forecast quality across products, customers, and time periods using a standardized percentage error metric.

## Formula

MAPE =

(1 / n) × Σ ( |Forecast Quantity − Actual Demand Quantity| / Actual Demand Quantity ) × 100%

Where:

- n = Number of Forecast Records

## Required Business Concepts

### Mandatory

- Forecast Quantity
- Actual Demand Quantity

### Optional Dimensions

- Product
- Product Category
- Customer
- Region
- Forecast Version
- Forecast Period
- Business Unit

## Interpretation

Lower MAPE indicates:

- More accurate forecasts
- Better inventory planning
- Better procurement planning
- Lower inventory costs

Higher MAPE indicates:

- Poor forecast quality
- Increased planning uncertainty
- Higher inventory risk
- Greater stockout or overstock risk

Typical Reference Values

- <10% → Excellent
- 10–20% → Good
- 20–30% → Acceptable
- >30% → Poor

(Targets should be defined according to industry and product characteristics.)

## Root Causes

1. Demand volatility
2. Seasonal demand changes
3. Promotional activities
4. New product introduction
5. Poor historical data quality
6. Forecast model limitations

## Improvement Actions

1. Improve forecasting models
2. Segment products by demand pattern
3. Incorporate promotion plans
4. Improve demand sensing
5. Continuously monitor forecast performance

## Related KPIs

- Forecast Accuracy
- Forecast Bias
- Inventory Turnover
- DIO
- Fill Rate
- OTIF

## Analysis Dependencies

### Previous Analysis

- Forecast Accuracy
- Forecast Bias

### Current Analysis

Evaluate the average magnitude of forecasting errors.

### Next Analysis

If MAPE exceeds target:

- Review Forecast Accuracy
- Review Forecast Bias
- Analyze Demand Volatility
- Analyze Product Segmentation
- Review Inventory Performance

### Trigger Conditions

Proceed when:

- MAPE exceeds target
- Forecast Accuracy declines
- Forecast Bias remains high
- Inventory issues increase
