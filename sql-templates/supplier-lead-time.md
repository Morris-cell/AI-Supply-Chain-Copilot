# Supplier Lead Time SQL Template

## Formula

Supplier Lead Time =
Goods Receipt Date − Purchase Order Date

## Required Business Concepts

- Purchase Order Date
- Goods Receipt Date

## SQL Template

```sql
SELECT
AVG(
DATEDIFF(
{GOODS_RECEIPT_DATE},
{PURCHASE_ORDER_DATE}
)
) AS supplier_lead_time_days
FROM {PURCHASE_TABLE};
```

## Output

supplier_lead_time_days

## Interpretation

Lower values indicate faster supplier response.
