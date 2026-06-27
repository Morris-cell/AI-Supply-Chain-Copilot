# Supplier Defect Rate SQL Template

## Formula

Supplier Defect Rate =
Defective Quantity / Received Quantity

## Required Business Concepts

- Received Quantity
- Defective Quantity

## SQL Template

```sql
SELECT
ROUND(
SUM({DEFECTIVE_QTY}) * 100.0 /
SUM({RECEIVED_QTY}),
2
) AS supplier_defect_rate
FROM {PURCHASE_TABLE};
```

## Output

supplier_defect_rate

## Interpretation

Lower values indicate better supplier quality performance.
