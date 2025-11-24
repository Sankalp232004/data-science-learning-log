Venture Finance India
=====================

**Prompt:** Where is capital actually landing within India, and how clean is the underlying deal data that drives those decisions?

This mini-pipeline standardizes a noisy funding tracker so analysts can reason about geography, round types, and investor appetite without spending hours on data hygiene.

Data
----
- Source: Publicly shared Google Sheet (mirrored locally as `data/startup_funding.csv`).
- Coverage: 3k+ disclosed rounds with investment date, amount, city, sector, and funding type.

What This Notebook Delivers
---------------------------
1. **Data readiness** – Normalizes column names, strips whitespace, fixes city aliases (Bangalore/Bengaluru), and tidies funding-type labels.
2. **Missing value audit** – Surfaces null-heavy features (amount, city, sub-vertical) and documents whether to impute or exclude.
3. **City concentration view** – Produces a top-10 city chart that can feed sourcing theses or GTM plans.

How to Use
----------
1. Refresh `data/startup_funding.csv` if you have a newer extract.
2. Open `notebooks/venture_finance_pipeline.ipynb` and run cells sequentially (pure pandas + matplotlib).
3. Repoint `City Location` filters or add grouping logic (sector, investor) to match the conversation you plan to have.

Insights to Highlight in Interviews
-----------------------------------
- Even after cleaning, ~30% of deal amounts are missing, so triangulation with press releases or Traxn-style data is essential.
- Funding concentration in Bengaluru and Delhi NCR suggests follow-on capacity is heavily skewed—useful when discussing fund deployment strategy.
- The text-normalization block is reusable for any inbound lead list or CRM export.

Next Steps
----------
- Enrich the dataset with exchange-rate adjusted USD amounts to enable time-series comparisons.
- Pair the clean output with dashboarding (Metabase/Looker/PowerBI) for partners who prefer visuals over raw notebooks.
