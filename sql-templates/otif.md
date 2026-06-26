# OTIF SQL Template

## Formula

OTIF = On Time and In Full Orders / Total Orders

## Required Business Concepts

* Requested Delivery Date
* Actual Delivery Date
* Ordered Quantity
* Delivered Quantity

## SQL Template

```sql
SELECT
ROUND(
SUM(
CASE
WHEN {ACTUAL_DELIVERY_DATE} <= {REQUESTED_DELIVERY_DATE}
AND {DELIVERED_QTY} >= {ORDERED_QTY}
THEN 1
ELSE 0
END
) * 100.0 / COUNT(*),2) AS otif_percentage
FROM {DELIVERY_TABLE};
```

## Output

otif_percentage
