# Diabetes-and-Depression-Study
(currently working on daily ) 
## Overview
This project analyzes relationships between diabetes, depression (PHQ‑9), BMI, and demographic factors using publicly available NHANES data. The goal is to explore how chronic disease, mental health, and social determinants intersect, using statistical tests and visualizations to highlight disparities and associations.
The repository includes:
- Python scripts for data cleaning, feature engineering, merging, and statistical testing
- Tableau‑ready cleaned dataset
- Visualizations (boxplots, scatterplots)
- A structured workflow for reproducible analysis

Data Sources
NHANES datasets used:
- DEMO_L.xpt — demographics
- DIQ_L.xpt — diabetes questionnaire
- DPQ_L.xpt — PHQ‑9 depression questionnaire
- BMX_L.xpt — body measurements (BMI)
All datasets were merged using the participant ID SEQN.

## Key Variables
Depression (PHQ‑9)
- Computed as the sum of items DPQ010–DPQ090
- Range: 0–27
- Binary depression indicator: PHQ‑9 ≥ 10 → Depressed
Diabetes
- Based on DIQ010 (“Has a doctor told you that you have diabetes?”)
- Recoded: 1 = Diabetes, 0 = No diabetes
BMI
- From BMXBMI
- Continuous measure of body mass index
Demographics
- Age
- Gender
- Race/Ethnicity
- Income‑to‑poverty ratio (INDFMPIR)
- Income grouped into Low / Middle / High

## Methods
Data Cleaning
- Replaced NHANES special missing codes (7, 9, 77, 99, etc.) with NaN
- Merged datasets on SEQN
- Removed rows with missing values
Feature Engineering
- Computed PHQ‑9 total score + binary depression variable
- Recoded diabetes status
- Created income groups from INDFMPIR
Analysis
- Descriptive statistics
- Tableau dashboards for sample characteristics
- Group comparisons by diabetes status and demographics
- Mann‑Whitney U test for non‑parametric comparison of depression scores

## Key Findings
- Individuals with diabetes show higher depression scores and more high‑end outliers.
- BMI is positively associated with depression scores.
- Income, gender, and race/ethnicity show clear disparities in depression burden.
- Mann‑Whitney U test indicates a statistically significant difference in depression scores between diabetics and non‑diabetics.

