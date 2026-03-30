# Individual-Homework-2
**README: Explaining the COMPAS Replacement Model**


**Purpose of the Analysis**

This assignment builds an explainability pipeline for a logistic regression model trained as a replacement for the COMPAS recidivism risk scoring system. The goal is to analyze whether the replacement model exhibits racial bias by applying three explanation methods — SHAP, LIME, and DiCE counterfactuals — and to evaluate what each method reveals about model behavior across racial groups.


**Python Libraries Used**

- `pandas` : data loading, filtering, and manipulation
- `numpy` : numerical computations
- `matplotlib` — data visualization
- `scikit-learn` : logistic regression model, train/test split, label encoding
- `shap` : SHAP beeswarm and waterfall plots
- `lime` : local explanation of individual predictions
- `dice-ml` : counterfactual generation


**Instructions for Reproducing the Results**
1. Open the notebook in Google Colab
2. Run all cells from top to bottom using **Runtime → Run All**
3. The dataset loads automatically from the ProPublica GitHub repository — no file uploads needed

**Workflow**
1. **Load and filter data** — The COMPAS dataset is pulled directly from a URL and filtered using the same criteria as the original ProPublica analysis
2. **Train model** : A logistic regression model is trained to predict whether a defendant receives a high COMPAS score
3. **Identify four individuals** : The highest and lowest risk Black and White defendants are selected from the test set
4. **SHAP analysis** : A beeswarm summary plot and waterfall plots are produced for all four individuals
5. **LIME analysis** : Local explanations are generated for each individual and compared against SHAP attributions
6. **DiCE counterfactuals** : Minimal feature changes required to flip each prediction are reported, with immutable features flagged
7. **Governance memo** : Findings are summarized in a 300-word memo addressed to a hypothetical court auditor

**Notes**
- Cells must be run in order — each cell depends on variables defined above it
- Results may vary slightly between runs due to LIME's random sampling process
