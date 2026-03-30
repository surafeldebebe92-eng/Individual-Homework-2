# Individual-Homework-2
**README: Explaining the COMPAS Replacement Model**

---

**Purpose of the Analysis**

This assignment builds an explainability pipeline for a logistic regression model trained as a replacement for the COMPAS recidivism risk scoring system. The goal is to analyze whether the replacement model exhibits racial bias by applying three explanation methods — SHAP, LIME, and DiCE counterfactuals — and to evaluate what each method reveals about model behavior across racial groups.

---

**Python Libraries Used**

- `pandas` — data loading, filtering, and manipulation
- `numpy` — numerical computations
- `matplotlib` — data visualization
- `scikit-learn` — logistic regression model, train/test split, label encoding
- `shap` — SHAP beeswarm and waterfall plots
- `lime` — local explanation of individual predictions
- `dice-ml` — counterfactual generation

---

**Instructions for Reproducing the Results**

1. Open the notebook in Google Colab
2. Run all cells from top to bottom using **Runtime → Run All**
3. The dataset loads automatically from the ProPublica GitHub repository — no file uploads needed

**Workflow**

1. **Load and filter data** — The COMPAS dataset is pulled directly from a URL and filtered using the same criteria as the original ProPublica analysis
2. **Train model** — A logistic regression model is trained to predict whether a defendant receives a high COMPAS score
3. **Identify four individuals** — The highest and lowest risk Black and White defendants are selected from the test set
4. **SHAP analysis** — A beeswarm summary plot and waterfall plots are produced for all four individuals
5. **LIME analysis** — Local explanations are generated for each individual and compared against SHAP attributions
6. **DiCE counterfactuals** — Minimal feature changes required to flip each prediction are reported, with immutable features flagged
7. **Governance memo** — Findings are summarized in a 300-word memo addressed to a hypothetical court auditor

**Notes**

- Cells must be run in order — each cell depends on variables defined above it
- An internet connection is required to load the dataset
- Results may vary slightly between runs due to LIME's random sampling process

---

**AI Acknowledgement**

For this assignment, I used Claude to help write and structure the Python code for computing SHAP values, running LIME explanations, and generating DiCE counterfactuals. The AI helped me understand how each method works and how to correctly set up the explainers in Google Colab. I also used AI to support parts of my coding process to make sure there were no errors. When errors came up during testing, I used the AI to help me understand what the mistake was, why it occurred, and how to correct it. For the written components — including the LIME vs SHAP comparison and the governance memo — I used AI to help structure and refine my responses, while engaging with all results and drawing my own conclusions.
