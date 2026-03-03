# BMI5111 Capstone – Targeted Social Prescription

This repository contains the full analytical pipeline for a capstone project on **risk-based targeting and policy evaluation** using the Health and Retirement Study (HRS).

The project develops an interpretable rule-based risk score for community-dwelling adults aged ≥65 and evaluates alternative targeting thresholds from a policy perspective.

---

## 📊 Project Overview

The workflow is structured as a reproducible pipeline:

EDA → Cohort construction → Risk scoring → Outcome evaluation → Policy sensitivity analysis

The final framework focuses on **risk stratification and policy-based targeting**, rather than strict causal effect estimation, due to limited overlap in matched designs.

---

## 📁 Repository Structure

### `notebooks/`

| Notebook | Purpose |
|----------|---------|
| 00_eda_data_understanding.ipynb | Data cleaning, harmonisation, and panel construction |
| 01_data_understanding.ipynb | Construction of baseline analytic cohort (age ≥65) |
| 02_feature_engineering_recommendation.ipynb | Risk score development and rule-based recommendation logic |
| 03_evaluation_reporting_age65plus.ipynb | Outcome evaluation (hospitalisation & depressive symptoms) |
| 04_longitudinal_policy_evaluation.ipynb | Policy sensitivity analysis and overlap diagnostics |

---

### `data_processed/`

Contains selected processed outputs used for evaluation and reporting:

- notebook0_clean_panel.csv  
- notebook4_policy_sensitivity.csv  
- notebook4_policy_sensitivity_by_group.csv  
- notebook3_person_level_outcomes.csv  

(Full raw HRS data not included due to licensing restrictions.)

---

### `figures/`
Generated figures used in reporting and analysis.

---

### `paper/`
Manuscript drafts and supporting materials.

---

## 🔬 Methodological Notes

- Risk score constructed from demographic, functional, chronic condition, and depressive symptom indicators.
- Targeting defined by percentile thresholds (e.g., top 30%, 40%).
- Policy evaluation compares outcome differences across thresholds.
- Overlap diagnostics performed before reframing from causal matching to policy contrast.

---

## 📌 Reproducibility

To reproduce the analysis:

1. Obtain HRS RAND data (1992–2022)
2. Place `.dta` file inside `data_raw/`
3. Run notebooks sequentially (00 → 04)

---

## Author

Yu Jun  
MSc Biomedical Informatics  
National University of Singapore