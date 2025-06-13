# Insurance Pricing Adequacy Analysis

This project investigates whether insurance policies are appropriately priced using a **frequency-severity modeling framework**. We combine statistical modeling with actuarial reasoning to analyze policyholder data and estimate **pure premiums**, then compare these to actual premiums to detect underpricing or overpricing patterns.

---

## Project Structure

- `Report.ipynb` – Complete analysis in an executable Jupyter notebook.
- `Report.pdf` – Static LaTeX version of the notebook, ready for presentation.
- `Summary_Paper.pdf` – Academic-style overview of methods, models, and findings.
- `figures/` – Contains all visualizations used in the reports.
- `data/` – Contains cleaned input datasets (or links to Kaggle).
- `requirements.txt` – (Optional) Library versions for reproducibility.

---

## Objectives

- **Quantify pricing misalignment** in insurance policies.
- Model:
  - **Claim frequency** using Poisson regression.
  - **Claim severity** using Gamma regression.
- Estimate **pure premium** as frequency × severity.
- Identify policies that are **underpriced or overpriced**.
- Offer actionable insights based on product-line segmentation.

---

## Data Sources

- [Insurance Claims and Policy Data (Kaggle)](https://www.kaggle.com/datasets/ravalsmit/insurance-claims-and-policy-data)
  - `data_synthetic.csv`: Full synthetic policyholder and claims dataset.
  - `insurance_dataset.csv`: Supplementary severity data (used for Gamma regression).

---

##  Tools & Techniques

- Python, Pandas, NumPy
- `statsmodels` (Poisson & Gamma GLMs)
- Data visualization: Seaborn, Matplotlib
- Feature engineering: tenure, premium-to-income ratio, credit categories
- Model interpretation with residuals and p-value heatmaps

---

## Key Findings

- Majority of policy types are **underpriced**, especially in segments with low credit scores or low tenure.
- Gamma regression for severity achieves a strong pseudo R² (~0.79), indicating good predictive power.
- Poisson model shows limitations (as expected) in claim frequency, with low R².
- Aggregate **portfolio loss** due to underpricing is quantified and visualized.

---

## Business Recommendations

- **Reprice underperforming products** based on pure premium estimates.
- **Adjust premium structure** for low-tenure, low-credit-score customers.
- Consider cross-validation and confidence intervals in future modeling to assess risk margins.
