# Fill Rate SQL Template

## Formula

Fill Rate =
Delivered Quantity / Ordered Quantity

## Required Business Concepts

- Ordered Quantity
- Delivered Quantity

## SQL Template

```sql
SELECT
ROUND(
SUM({DELIVERED_QTY}) * 100.0 /
SUM({ORDERED_QTY}),
2
) AS fill_rate
FROM {DELIVERY_TABLE};
```

## Output

fill_rate

## Interpretation

Higher Fill Rate indicates better inventory availability and customer service performance.
