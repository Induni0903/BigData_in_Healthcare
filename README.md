
# Breast Cancer Metastasis: Survival Analysis & Gene Expression Modeling
## Big Data in Healthcare | Master’s Degree Project (R)
This project explores the clinical and genomic drivers of breast cancer metastasis in a cohort of 144 women with lymph node involvement. By leveraging Survival Analysis and High-Dimensional Penalized Regression, this study builds predictive models to estimate the risk of metastasis or death.

## Project Overview
Breast cancer metastasis significantly impacts survival rates. This project aims to bridge the gap between traditional clinical indicators and modern gene expression profiling to improve prognostic accuracy.

Key Objectives:

* Survival Modeling: Utilizing Cox Proportional Hazards models to evaluate clinical risk.

* Genomic Integration: Screening 70 prognostic genes using univariate and penalized methods.

* Predictive Analytics: Developing augmented models that combine clinical and genetic markers for 1-year risk prediction.

## The Dataset
The dataset contains longitudinal and molecular data for 144 patients:

* Time-to-Event: Follow-up time (months) and event indicator (metastasis/death).

* Clinical Features: Tumor diameter, lymph node involvement, Estrogen Receptor (ER) status, tumor grading, and patient age.

* Genomic Features: Expression levels of 70 potentially prognostic genes.

## Analytical Pipeline
1. Descriptive & Univariate Analysis
* Summarized clinical characteristics and inherent patterns.
* Performed Univariate Cox Proportional Hazards models to assess the individual impact of variables like tumor size and age on patient outcomes.

2. Model Diagnostics & Validation
* Functional Form Assessment: Evaluated the linearity of continuous variables (e.g., age).
* PH Assumption: Verified the Proportional Hazards assumption using Schoenfeld residuals to ensure model validity.

3. High-Dimensional Gene Analysis
* Multiple Testing Correction: Conducted univariate Cox models for all 70 genes, applying the Benjamini-Hochberg (FDR) method to control for false discoveries.
* LASSO Penalized Regression: Implemented a Penalized Cox Model (L1 regularization) to perform variable selection among the high-dimensional gene expression data.

4. Model Augmentation & Risk Prediction
* Basic Model: Clinical variables only.
* Augmented Model: Integrated clinical data with LASSO-selected gene expression features.
* Risk Scoring: Estimated the probability of an event at a 1-year fixed time-point for specific patient profiles.

## Technical Stack
* Language: R
* Libraries: * survival: Core survival analysis and Cox models.
* survminer: Visualization of Kaplan-Meier curves and diagnostics.
* glmnet: LASSO and penalized regression.

## Key Insights
* Clinical Drivers: Identified specific tumor grades and lymph node counts as primary clinical risk factors.
* Genomic Signatures: Isolated a subset of genes that significantly improve the model’s C-index (predictive accuracy) compared to clinical data alone.
* Predictive Power: The augmented model demonstrated a more granular risk stratification for patients at the 12-month mark.

tidyverse: Data manipulation and visualization.
