# The Beauty of Safety  
*A Comprehensive Analysis of Chemicals in Cosmetic Products*

## Overview
As public concern grows around the safety of ingredients used in cosmetics and personal care products, this project investigates the presence, frequency, and health implications of hazardous chemicals. Using a government-sourced dataset, we analyze trends in toxic ingredient usage and assess the toxicity levels of various cosmetic products to promote safer consumer choices.

---

## Dataset

- **Source**: [Data.gov – Chemicals in Cosmetics Dataset](https://catalog.data.gov/dataset/chemicals-in-cosmetics-d55bf)
- **Provider**: California Safe Cosmetics Program (CSCP), California Department of Public Health
- **Contents**:
  - 110K+ product records
  - Chemical names and CAS numbers
  - Product names, categories, and manufacturer details
  - Number of reported chemicals per product
  - Reporting and discontinuation dates
  - Toxicity concerns including links to cancer, birth defects, and reproductive risks

---

## Tools & Technologies

- **Language**: R  
- **Libraries**: `tidyverse`, `dplyr`, `ggplot2`, `labelencoder`  
- **Modeling**: Random Forest (classification), LightGBM (regression)  
- **References**: [TOXNET – Toxicology Data Network](https://www.nlm.nih.gov/toxnet/index.html)

---

## Methodology

### 1. Data Cleaning
- Removed duplicate records and columns with excessive missing data
- Dropped irrelevant identifiers and formatted date fields
- Ensured consistency in column names and structure

### 2. Feature Engineering
- Calculated date differences between reporting dates
- Derived chemical toxicity scores based on usage frequency and number of chemicals per product
- Encoded categorical variables for modeling

### 3. Data Visualization
- Plotted top 20 most-used chemicals (e.g., Titanium Dioxide, Silica)
- Visualized annual usage trends of major chemicals
- Explored toxicity score distribution across years and categories

### 4. Predictive Modeling
- **Toxicity Classification**: Used Random Forest to classify products into low, medium, or high toxicity (97% accuracy)
- **Chemical Count Prediction**: Used LightGBM regression to estimate number of harmful chemicals per product (80.2% accuracy)

---

## Key Insights

- **Titanium Dioxide** emerged as the most frequently reported chemical, with known links to cancer.
- **Cocamide DEA** showed a steep decline in usage after regulatory restrictions introduced post-2016.
- A significant percentage of personal care products were found to contain multiple high-risk ingredients.
- Toxicity scores helped classify and visualize product safety levels over time.

---

## Visual Outputs

- Bar charts of top reported chemicals
- Year-wise usage trends of selected hazardous substances
- Histograms and box plots of toxicity scores
- Model evaluation metrics and confusion matrices

---
  
## References

- [Chemicals in Cosmetics Dataset – Data.gov](https://catalog.data.gov/dataset/chemicals-in-cosmetics-d55bf)  
- [TOXNET – Toxicology Data Network](https://www.nlm.nih.gov/toxnet/index.html)  
- [FDA Cosmetics Safety](https://www.fda.gov/cosmetics/cosmetics-laws-regulations)

---



