Sports Operations Analytics
===========================

**Prompt:** Use a familiar sports dataset to illustrate how you would build an operations intelligence asset—one that could just as easily be applied to logistics or network optimization.

Data
----
- `data/IPL_Matches_2008_2022.csv` – Match-level context (venue, toss, result, margin, player of the match).
- `data/IPL_Ball_by_Ball_2008_2022.csv` – Delivery-level telemetry for more granular strategy questions.

Notebook Tour
-------------
- `notebooks/ipl_data_pipeline.ipynb`
	- Loads both datasets, inspects schema mismatches, and documents missing-value treatment (e.g., unknown venues, SuperOver flags).
	- Produces a quick win-share leaderboard—useful when talking through talent allocation, salary caps, or scheduling decisions.

Business Relevance
------------------
- The same mechanics (ingest, join, rank, visualize) can power operations reviews for airlines, telcos, or fulfillment centers.
- Demonstrates how to translate a seemingly niche domain into a framework for resource allocation and efficiency storytelling.

Next Experiments
----------------
- Merge the ball-by-ball data with matches to analyze powerplay efficiency or death-overs tactics.
- Convert insights into KPI scorecards that track franchise health (net run rate, win streaks, roster stability).
- Showcase feature engineering ideas (form streaks, venue-adjusted performance) that would transfer back to finance use cases.
