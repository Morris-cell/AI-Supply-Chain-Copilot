# Delivery Lead Time SQL Template

## Formula

Delivery Lead Time = Actual Delivery Date − Order Date

## Required Business Concepts

- Order Date
- Actual Delivery Date

## SQL Template (Average Delivery Lead Time)

```sql
SELECT
AVG(DATEDIFF(
{ACTUAL_DELIVERY_DATE},
{ORDER_DATE}
)) AS avg_delivery_lead_time
FROM {DELIVERY_TABLE};
```

## SQL Template (By Carrier)

```sql
SELECT
carrier,
AVG(DATEDIFF(
{ACTUAL_DELIVERY_DATE},
{ORDER_DATE}
)) AS avg_delivery_lead_time
FROM {DELIVERY_TABLE}
GROUP BY carrier;
```

## SQL Template (By Region)

```sql
SELECT
region,
AVG(DATEDIFF(
{ACTUAL_DELIVERY_DATE},
{ORDER_DATE}
)) AS avg_delivery_lead_time
FROM {DELIVERY_TABLE}
GROUP BY region;
```

## Output

- avg_delivery_lead_time
