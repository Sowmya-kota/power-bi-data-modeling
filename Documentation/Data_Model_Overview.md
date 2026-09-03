# Data Model Overview

## Model Architecture

The project uses a dimensional modeling approach designed to provide a scalable and analytics-ready semantic model.

The final model separates descriptive business entities into dimension tables and measurable business events into fact tables.

## Dimension Tables

- `dim_date` — Date and time analysis
- `dim_product` — Product attributes and categorization
- `dim_customer` — Customer information
- `dim_campaign` — Campaign attributes
- `dim_geo` — Geographic information
- `dim_orders_flags` — Order-related flags and classifications

## Fact Tables

- `fact_sales` — Sales transactions and revenue analysis
- `fact_order_fulfillment` — Order fulfillment and delivery performance
- `fact_inventory` — Inventory and product quantity analysis
- `fact_campaign_spend` — Campaign spending
- `fact_promotion_coverage` — Promotion coverage analysis
- `fact_sales_targets` — Sales target and performance comparison

## Supporting Tables

- `security` — User access information used for Row-Level Security
- Measures table — Centralized analytical measures

## Key Modeling Principles

- Fact tables are designed around measurable business events
- Dimension tables provide reusable descriptive attributes
- Relationships support consistent filter propagation
- A dedicated Date Dimension supports time-based analysis
- Reusable DAX measures centralize business logic
- Row-Level Security controls data access based on user scope
