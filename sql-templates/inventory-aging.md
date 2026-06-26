# Inventory Aging SQL Template

## Formula

Inventory Age = Current Date - Receipt Date

## Required Business Concepts

* Inventory Receipt Date
* Inventory Value

## SQL Template

SELECT
sku_id,
warehouse,
DATEDIFF(CURDATE(), {RECEIPT_DATE}) AS inventory_age_days,
{INVENTORY_VALUE}
FROM {INVENTORY_TABLE};

## Aging Bucket Example

0–30 Days

31–60 Days

61–90 Days

91–180 Days

Over 180 Days
