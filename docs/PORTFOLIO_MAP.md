# Portfolio Map

This repository collects hands-on analytics work that supports applications for roles in economics, finance, and data-driven strategy. Use this map as the single source of truth for how each project is positioned and which business questions it answers.

## Navigation Snapshot

| Domain | Project | Focus | Data Assets | Notebook(s) |
| --- | --- | --- | --- | --- |
| Macro & Public Policy | [Macro Health Resilience](../projects/macro_health_resilience) | Quantify the trajectory of COVID-19 cases to evaluate policy timing and health-system pressure. | `data/owid-covid-data.csv` | `notebooks/macro_health_resilience.ipynb` |
| Venture & Capital Allocation | [Venture Finance India](../projects/venture_finance_india) | Diagnose deal flow, ticket sizes, and investor appetite within Indian startup funding rounds. | `data/startup_funding.csv` | `notebooks/venture_finance_pipeline.ipynb` |
| Consumer Finance & Loyalty | [Consumer Value Analytics](../projects/consumer_value_analytics) | Clean messy point-of-sale data, surface growth pockets, and cluster customers for retention. | `data/dirty_retail_sales.csv` | `notebooks/retail_data_cleaning.ipynb`, `notebooks/customer_segmentation.ipynb` |
| Risk & Survival Modeling | [Risk Survival Modeling](../projects/risk_survival_modeling) | Reframe the Titanic dataset as a binary survival/risk exercise to mirror credit default modeling. | `data/titanic_1M.csv` | `notebooks/data_inspection.ipynb`, `notebooks/survival_model.ipynb` |
| Operations & Benchmarking | [Sports Operations Analytics](../projects/sports_operations_analytics) | Model resource allocation and competitive advantage using IPL historical match logs. | `data/IPL_Matches_2008_2022.csv`, `data/IPL_Ball_by_Ball_2008_2022.csv` | `notebooks/ipl_data_pipeline.ipynb` |

## Storytelling Pillars

1. **Economic intuition first** – Each README leads with the commercial question (policy timing, deal sourcing, consumer value, loss-given-default proxies, or operational leverage).
2. **Transparent workflow** – Every project surfaces raw data, cleaning logic, modeling steps, and takeaways so hiring managers can audit assumptions quickly.
3. **Re-usable building blocks** – Notebook names, directory structure, and dataset notes are standardized to reduce review friction.

## Suggested Talking Points

- Explain how `Macro Health Resilience` links pandemic trajectories to fiscal or healthcare capacity planning.
- Use `Venture Finance India` to discuss capital efficiency, dry powder deployment, and geographic theses.
- Highlight `Consumer Value Analytics` to demonstrate lifecycle value (LTV) thinking and marketing ROI discipline.
- Position `Risk Survival Modeling` as a sandbox for credit-scoring logic (logistic regression, feature engineering, validation).
- Reference `Sports Operations Analytics` when showcasing domain-agnostic modeling discipline and storytelling.

## Next Additions

- Add lightweight Streamlit dashboards that can be demoed live during interviews.
- Capture experiment tracking or model cards for each notebook run.
- Introduce a `Makefile` or task runner for automated data refreshes.
