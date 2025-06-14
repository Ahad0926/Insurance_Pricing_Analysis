# Insurance Pricing Adequacy Analysis

This project investigates whether insurance policies are appropriately priced using a **frequency–severity modeling framework**. We combine statistical modeling with actuarial reasoning to estimate **pure premiums** and assess **pricing misalignment** across policy types.

---

## Project Structure

- `Insurance Pricing Analysis.ipynb` – Full Jupyter notebook analysis.
- `Insurance Pricing Analysis.pdf` – Static notebook PDF.
- `Summary Paper.pdf` – Formal summary of methodology and findings.
- `figures/` – Visuals and model outputs used in the reports.
- `data/` – Kaggle datasets.

---

## Objectives

- Evaluate **pricing adequacy** of insurance products.
- Model:
  - **Claim frequency** with Poisson regression.
  - **Claim severity** with Gamma regression.
- Derive **pure premiums** (frequency × severity).
- Detect **underpriced or overpriced** policies.
- Segment insights by policy type for targeted recommendations.

---

## Data Sources

- [Kaggle: Insurance Claims and Policy Data](https://www.kaggle.com/datasets/ravalsmit/insurance-claims-and-policy-data)
  - `data_synthetic.csv` – Main dataset for frequency modeling and metadata.
  - `insurance_dataset.csv` – Supplementary data for severity modeling.

---

## Tools & Techniques

- Python (Pandas, NumPy, Seaborn, Matplotlib)
- `statsmodels` GLM framework (Poisson and Gamma)
- Feature engineering:
  - Tenure calculation
  - Premium-to-income ratio
  - Credit score binning
- Model diagnostics:
  - Residual plots
  - P-value heatmaps
  - Normalized RMSE metrics

---

## Key Findings

- **All major policy types** exhibit underpricing, especially among low-tenure and low-credit-score segments.
- Gamma regression (severity) shows strong predictive power (pseudo R² ≈ 0.796, RMSE ≈ 7.4%).
- Poisson model (frequency) reveals moderate error (RMSE ≈ 35%)—expected due to low-variance count data.
- Total underpricing across the portfolio is **visually and quantitatively assessed**.

---

## Business Recommendations

- **Reprice all products** based on modeled pure premiums, not just select segments.
- **Flag low-credit, low-tenure customers** for pricing reassessment or additional underwriting.
- Future work should include **cross-validation** and **risk margin buffers** for production use.

---
