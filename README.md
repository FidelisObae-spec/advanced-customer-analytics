# Customer Analytics & Predictive Modeling

## Project status

This repository is currently a project brief and design blueprint. It does not yet contain a transaction dataset, SQL pipeline, notebook, dashboard, or runnable ETL code. The sections below describe the planned first version rather than completed functionality.

## Goal

Build a small, reproducible analytics project that turns clearly labeled sample transaction data into customer-level revenue and recency summaries. The first version should make its assumptions visible and avoid presenting a prototype as a production system.

## Planned structure

```text
├── data/
│   └── sample_transactions.csv       # Synthetic, documented sample data
├── sql-queries/
│   └── customer_lifetime_value.sql   # Customer-level revenue and order summary
├── notebooks/
│   └── .gitkeep                      # Exploratory analysis
├── dashboards/
│   └── .gitkeep                      # Future visualizations
└── README.md
```

## Proposed transaction fields

| Field | Type | Meaning |
| :--- | :--- | :--- |
| `transaction_id` | Text | Unique transaction identifier |
| `customer_id` | Text | Stable customer identifier |
| `transaction_date` | Timestamp | Time of purchase |
| `amount` | Decimal | Positive transaction amount |
| `device_type` | Text | Purchase channel, such as desktop or mobile |

The sample dataset and SQL dialect have not been selected yet. Any future sample rows should be synthetic and labeled as such; no real customer data belongs in this repository.

## Planned first analysis

1. Validate required columns, timestamps, and positive amounts.
2. Aggregate order count, total revenue, and average order value by customer.
3. Add recency based on the most recent transaction in the sample.
4. Document thresholds and limitations before adding any customer segments or churn estimates.

## Next steps

- Add a small synthetic CSV and a reproducible validation step.
- Choose and document a SQL engine, then add the customer summary query.
- Add tests and a notebook only after the first query has a clear expected result.

Until those files exist, clone the repository to read this project brief; there is no executable pipeline to run yet.
