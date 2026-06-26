# Inventory Aging

## Definition

Measures how long inventory has remained in stock by classifying inventory into different age buckets.

## Business Purpose

Identify slow-moving and obsolete inventory to support inventory optimization and reduce carrying costs.

## Business Questions

* How much inventory is aging?
* Which products are becoming obsolete?
* Which warehouses have excessive old inventory?

## Calculation Logic

Inventory Age = Current Date - Inventory Receipt Date

Inventory is classified into predefined aging buckets.

## Typical Aging Buckets

* 0–30 Days
* 31–60 Days
* 61–90 Days
* 91–180 Days
* Over 180 Days

## Required Business Concepts

* Inventory Receipt Date
* Inventory Value
* Current Date

## Interpretation

Higher percentage of aged inventory indicates:

* Slow-moving inventory
* Excess inventory
* Higher carrying cost
* Higher obsolescence risk

Lower percentage of aged inventory indicates:

* Healthy inventory movement
* Better working capital utilization

## Root Causes

1. Forecast Error
2. Demand Decline
3. Excess Purchasing
4. Product Obsolescence
5. Product Lifecycle Changes

## Improvement Actions

1. Liquidate obsolete inventory
2. Reduce purchase quantities
3. Improve demand forecasting
4. Review safety stock policy
5. Improve product lifecycle management

## Related KPIs

* Inventory Turnover
* DIO
* Fill Rate
* Forecast Accuracy
* Stockout Rate

## Analysis Dependencies

### Previous Analysis

* Inventory Turnover
* DIO

### Current Analysis

Identify aged inventory and obsolete stock.

### Next Analysis

If aged inventory is high:

* Identify affected SKUs
* Analyze Sales History
* Review Product Lifecycle
* Review Procurement Decisions

### Trigger Conditions

Proceed when:

* Inventory older than 90 days exceeds target
* Inventory older than 180 days increases
