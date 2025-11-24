Consumer Value Analytics
========================

**Prompt:** How would you triage messy point-of-sale data, surface growth pockets, and back your retention strategy with segmentation evidence?

Data
----
- Source: Kaggle "Dirty Retail Store Sales" CSV mirrored locally as `data/dirty_retail_sales.csv`.
- Volume: 11k+ transactions with common real-world issues (typos, missing IDs, negative quantities).

Workflow
--------
1. **Data quality bootcamp** (`notebooks/retail_data_cleaning.ipynb`)
	- Standardizes headers, coerces dates, enforces positive quantities/prices, drops unknown customers.
	- Leaves breadcrumbs explaining each cleaning decision (ideal for audit trails).
2. **Insight engine + segmentation** (`notebooks/customer_segmentation.ipynb`)
	- Explores category mix, time-series trends, and customer contribution.
	- Builds a K-Means model on Monetary vs. Frequency features to prove basic lifecycle value segmentation.

Talking Points
--------------
- Cleaning shrinks the dataset by ~8%, preventing inflated revenue claims and forcing trust in the final sample.
- Electronics and clothing dominate revenue, but the seasonal plot shows Q4 spikes—timely for promo planning discussions.
- Customer clusters reveal a high-value micro-segment (Cluster 2) worth tailored retention spend.

Files
-----
- `data/dirty_retail_sales.csv`
- `notebooks/retail_data_cleaning.ipynb`
- `notebooks/customer_segmentation.ipynb`

Future Enhancements
-------------------
- Add RFM (recency-frequency-monetary) or LTV estimates to enrich segmentation.
- Pipe cleaned data into a dashboard template for non-technical GTM stakeholders.
- Introduce uplift modeling to prioritize offers by expected incremental margin.
