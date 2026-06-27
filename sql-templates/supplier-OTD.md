# Supplier On-Time Delivery SQL Template

## Formula

Supplier OTD =
On-Time Purchase Orders / Total Purchase Orders

## Required Business Concepts

- Promised Delivery Date
- Goods Receipt Date

## SQL Template

```sql
SELECT
ROUND(
SUM(
CASE
WHEN {GOODS_RECEIPT_DATE} <= {PROMISED_DELIVERY_DATE}
THEN 1
ELSE 0
END
) * 100.0 / COUNT(*),2) AS supplier_otd_percentage
FROM {PURCHASE_TABLE};
```

## Output

supplier_otd_percentage

## Interpretation

Higher values indicate more reliable supplier delivery performance.
