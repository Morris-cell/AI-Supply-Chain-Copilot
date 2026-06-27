# Forecast Bias SQL Template

## Formula

Forecast Bias (%) =
((Forecast Quantity − Actual Demand Quantity)
/ Actual Demand Quantity) × 100

## Required Business Concepts

- Forecast Quantity
- Actual Demand Quantity

## SQL Template

```sql
SELECT
ROUND(
(
SUM({FORECAST_QTY}) -
SUM({ACTUAL_QTY})
)
*100.0/
SUM({ACTUAL_QTY}),
2
) AS forecast_bias_percentage
FROM {FORECAST_TABLE};
```

## Output

forecast_bias_percentage

## Interpretation

Positive values indicate over-forecasting.

Negative values indicate under-forecasting.
