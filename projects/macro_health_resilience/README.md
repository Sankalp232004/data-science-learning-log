Macro Health Resilience
=======================

**Prompt:** How can a policy or strategy team quantify when health-system strain will peak so that fiscal and medical responses can be sequenced correctly?

This project turns the Our World in Data COVID-19 feed into a macro surveillance notebook that can be reused for any country. The goal is to summarize caseload trajectories, identify inflection points, and tie those patterns to economic resilience talking points.

Data
----
- Source: [Our World in Data](https://ourworldindata.org/coronavirus)
- File: `data/owid-covid-data.csv`
- Coverage: 350k+ rows, 67 variables, daily cadence across countries and continents.

Policy Questions Addressed
--------------------------
1. When did the rate of change in confirmed cases accelerate or plateau for a chosen market (India in the base notebook)?
2. How do data-quality gaps (testing, excess mortality, hospital utilization) affect confidence levels in downstream scenario planning?
3. What lag structure between cases and deaths should be assumed when forecasting ICU or fiscal needs?

Workflow Highlights
-------------------
- **Data hygiene:** Inspects null density, coerces `date` fields to `datetime`, and fills unavoidable gaps cautiously (e.g., zeros for `total_cases`).
- **Country lens:** Filters to the market of interest and keeps the pipeline modular so analysts can swap countries or regions without rewriting code.
- **Signal extraction:** Builds a clean line chart plus intermediate series that can be fed into nowcasting or simple growth-rate comparisons.

Files
-----
- `notebooks/macro_health_resilience.ipynb` – Master notebook covering ingestion, cleaning, EDA, and ready-to-present visuals.
- `data/owid-covid-data.csv` – Locally cached OWID data pull (refresh as needed).

Next Steps
----------
- Layer hospital-capacity or fiscal-stimulus datasets to link public-health metrics with GDP drawdowns.
- Add scenario toggles (optimistic/base/pessimistic) driven by rolling growth rates.
- Export the key charts to a lightweight briefing deck or dashboard.

