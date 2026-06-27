# Forecast Accuracy SQL Template

## Formula

Forecast Accuracy =

100 − ABS(Forecast − Actual) / Actual × 100

## Required Business Concepts

- Forecast Quantity
- Actual Demand Quantity

## SQL Template

```sql
SELECT
ROUND(
100 -
(
SUM(
ABS({FORECAST_QTY} - {ACTUAL_QTY})
)
*100.0/
SUM({ACTUAL_QTY})
),
2
) AS forecast_accuracy
FROM {FORECAST_TABLE};
```

## Output

forecast_accuracy

## Interpretation

Higher Forecast Accuracy indicates better demand planning performance.
