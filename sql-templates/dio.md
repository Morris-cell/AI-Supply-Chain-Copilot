# Days Inventory Outstanding (DIO)

## Formula

DIO = (Average Inventory / COGS) × 365

## Required Business Concepts

* Cost of Goods Sold
* Inventory Value

## SQL Template

SELECT
AVG({INVENTORY_VALUE}) /
SUM({COGS}) * 365
AS dio
FROM {INVENTORY_TABLE};

## Output

dio

## Interpretation

Lower:

* Better inventory efficiency
* Faster cash conversion

Higher:

* Inventory accumulation
* Potential overstocking
