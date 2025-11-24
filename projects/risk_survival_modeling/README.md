Risk Survival Modeling
======================

**Prompt:** Showcase a credit-risk style workflow (data cleaning, exploratory diagnostics, baseline classifier) using an interpretable dataset.

Why Titanic?
------------
The Kaggle "Titanic 1M" synthetic dataset mirrors the statistical properties of the famous passenger manifest while providing enough rows to behave like a production-sized credit dataset. It is ideal for demonstrating survival probability modeling without dealing with NDAs.

Workflow
--------
1. **Exploration + Data Contract** (`notebooks/data_inspection.ipynb`)
	- Loads the CSV, documents schema, inspects nulls, and confirms that string columns are encoded as expected.
2. **Modeling Pipeline** (`notebooks/survival_model.ipynb`)
	- Cleans `Age` and `Embarked`, drops high-missing fields (Cabin), one-hot encodes categorical features, and fits a logistic regression classifier.
	- Evaluates holdout accuracy (~80%) and prints coefficients so you can articulate driver importance (e.g., `Sex_male` negative impact on survival odds).

Interview Soundbites
--------------------
- **Feature pragmatism:** Demonstrates when it is appropriate to drop leaking columns (Cabin) versus impute (Age, Embarked).
- **Model governance:** Highlights why a simple, explainable baseline is a good first checkpoint before moving to tree-based models.
- **Portability:** The same notebook pattern can be copied into default-rate modeling, churn scoring, or underwriting triage.

Files
-----
- `data/titanic_1M.csv`
- `notebooks/data_inspection.ipynb`
- `notebooks/survival_model.ipynb`

Next Steps
----------
- Track additional metrics (ROC-AUC, precision/recall) and plot calibration curves.
- Introduce class-weighting or SMOTE if the positive class becomes imbalanced in future experiments.
- Replace logistic regression with gradient boosting to compare lift under stronger models.
