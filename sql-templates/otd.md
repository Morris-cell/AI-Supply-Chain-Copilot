# On-Time Delivery SQL Template

## Formula

OTD = On-Time Deliveries / Total Deliveries

## Required Business Concepts

- Requested Delivery Date
- Actual Delivery Date

## SQL Template

```sql
SELECT
ROUND(
SUM(
CASE
WHEN {ACTUAL_DELIVERY_DATE} <= {REQUESTED_DELIVERY_DATE}
THEN 1
ELSE 0
END
) * 100.0 / COUNT(*),2) AS otd_percentage
FROM {DELIVERY_TABLE};
```

## Output

otd_percentage

## Interpretation

Higher OTD indicates better delivery punctuality.
