# Industry Intelligence Layer

## Overview

The **Industry Intelligence Layer** provides industry-specific knowledge for the AI Supply Chain Copilot.

While KPI definitions remain consistent across industries, the interpretation of KPI values, operational priorities, acceptable performance thresholds, and recommended corrective actions vary significantly by industry.

This layer enables the AI engine to adapt its reasoning according to the business context before performing KPI diagnosis.

The Industry Intelligence Layer is positioned above the Knowledge Base and below the AI Rule Engine.

```
User Question
        │
        ▼
Identify Industry
        │
        ▼
Load Industry Intelligence
        │
        ▼
Load KPI Framework
        │
        ▼
Generate SQL
        │
        ▼
Compare with Industry Benchmark
        │
        ▼
Root Cause Analysis
        │
        ▼
Generate Recommendation
```

---

# Design Principles

The Industry Intelligence Layer follows six design principles.

## 1. Industry Independence

Each industry is maintained independently.

No assumptions should be shared across industries unless explicitly defined.

Adding a new industry must not require modification of existing industries.

---

## 2. Standardized Schema

Every industry must follow exactly the same document structure.

This allows the AI engine to retrieve knowledge consistently without requiring industry-specific parsing logic.

---

## 3. AI-Oriented Knowledge

The documents are designed for AI reasoning rather than human reading.

Each section answers a specific reasoning question.

Example:

Industry Profile

↓

"What makes this industry's supply chain unique?"

Benchmark

↓

"Is this KPI good or bad?"

Seasonality

↓

"Is the KPI affected by seasonal demand?"

Common Root Causes

↓

"What is the most probable explanation?"

---

## 4. Separation of Responsibilities

Each Markdown document has only one responsibility.

| Document                     | Responsibility                        |
| ---------------------------- | ------------------------------------- |
| industry-profile.md          | Industry characteristics              |
| benchmark.md                 | KPI benchmark values                  |
| seasonality.md               | Seasonal demand patterns              |
| common-root-causes.md        | Industry-specific diagnosis knowledge |
| analysis-rules.md *(future)* | AI reasoning rules                    |

---

## 5. Reusable Knowledge

Industry knowledge must never reference:

* ERP vendors
* Database platforms
* Companies
* Regions
* Internal projects

The knowledge should remain reusable across organizations.

---

## 6. Enterprise Maintainability

Every document should be independently maintainable.

Updating one benchmark or one industry profile should not require changes elsewhere.

---

# Directory Structure

```
industry/

README.md

automotive-ev/

    industry-profile.md

    benchmark.md

    seasonality.md

    common-root-causes.md

smartphone/

    industry-profile.md

    benchmark.md

    seasonality.md

    common-root-causes.md
```

Future industries can be added using the same structure.

```
industry/

semiconductor/

pharmaceutical/

consumer-electronics/

fmcg/

apparel/

industrial-equipment/
```

---

# Industry Knowledge Schema

Every industry must implement the following four knowledge modules.

---

# Module 1

industry-profile.md

## Purpose

Describe the overall characteristics of the industry's supply chain.

This document provides business context for AI reasoning.

## Standard Sections

### 1. Industry Overview

Business description

Industry maturity

Typical business model

---

### 2. Product Characteristics

Product lifecycle

SKU complexity

Product customization

Technology evolution

---

### 3. Demand Characteristics

Demand stability

Promotion sensitivity

Seasonality

Forecast difficulty

---

### 4. Manufacturing Characteristics

Manufacturing model

Production strategy

Capacity constraints

Lead time characteristics

---

### 5. Procurement Characteristics

Supplier dependency

Strategic materials

Global sourcing

Single-source risks

---

### 6. Inventory Strategy

Inventory philosophy

Safety stock policy

Inventory visibility

Inventory optimization goals

---

### 7. Logistics Characteristics

Distribution model

Warehouse strategy

Transportation characteristics

Customer service expectations

---

### 8. Supply Chain Risks

Demand risks

Supply risks

Manufacturing risks

Transportation risks

Regulatory risks

---

### 9. KPI Priorities

Most important KPIs

Secondary KPIs

Typical management focus

---

### 10. AI Analysis Guidance

How AI should interpret this industry.

Special considerations.

Typical investigation priorities.

---

# Module 2

benchmark.md

## Purpose

Define industry-specific KPI standards.

AI uses this document to evaluate KPI performance.

Each KPI must follow the same structure.

## Standard Template

KPI Name

Business Meaning

Business Objective

Excellent

Target

Warning

Critical

Business Interpretation

Typical Causes

Suggested Next Analysis

Monitoring Frequency

Data Refresh Frequency

Owner

---

# Module 3

seasonality.md

## Purpose

Describe predictable business cycles.

AI should check this document before identifying abnormal KPI behavior.

## Standard Sections

Annual Demand Pattern

Monthly Characteristics

Quarterly Characteristics

Peak Season

Low Season

Major Business Events

Product Launch Cycle

Promotional Calendar

Risk Periods

AI Interpretation Rules

---

# Module 4

common-root-causes.md

## Purpose

Provide industry-specific diagnostic knowledge.

The AI Rule Engine uses this document after KPI evaluation.

## Standard Structure

KPI

↓

Possible Symptoms

↓

Likely Root Causes

↓

Supporting Evidence

↓

Recommended Investigation

↓

Recommended Actions

Each KPI may contain multiple diagnosis trees.

---

# Future Module

analysis-rules.md

This document will be introduced in the Rule Engine phase.

It defines:

• KPI trigger conditions

• AI reasoning logic

• Cross-KPI dependency

• Escalation rules

• Investigation sequence

---

# AI Loading Strategy

When a user asks a supply chain question, the AI engine should load documents in the following order.

```
Industry Profile

↓

Benchmark

↓

Seasonality

↓

KPI Framework

↓

SQL Template

↓

Analysis Playbook

↓

Common Root Causes

↓

Case Studies
```

This loading order ensures that business context is established before KPI interpretation and root cause analysis.

---

# Version

Current Version

v1.0

Status

Industry Intelligence Layer Specification

Applicable Industries

* Automotive EV
* Smartphone

Future Expansion

Unlimited
