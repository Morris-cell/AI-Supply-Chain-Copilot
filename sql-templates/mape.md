# MAPE SQL Template

## Formula

MAPE =

AVG(
ABS(
(Forecast Quantity - Actual Demand Quantity)
/
Actual Demand Quantity
)
)
× 100

## Required Business Concepts

- Forecast Quantity
- Actual Demand Quantity

## SQL Template

```sql
SELECT
ROUND(
AVG(
ABS(
({FORECAST_QTY} - {ACTUAL_QTY}) * 1.0
/
NULLIF({ACTUAL_QTY},0)
)
) * 100,
2
) AS mape_percentage
FROM {FORECAST_TABLE};
```

## Output

mape_percentage

## Interpretation

Lower MAPE indicates better forecasting performance.

Note

NULLIF({ACTUAL_QTY},0) prevents division-by-zero errors. Rows where Actual Demand Quantity is zero will return NULL for the percentage calculation and are ignored by AVG in most SQL databases. You should define a business rule for zero-demand cases (for example, exclude them or use an alternative metric).
