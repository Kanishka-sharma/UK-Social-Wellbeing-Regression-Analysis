# Predicting Local Satisfaction in England  
### A Data-Driven Exploration of Social Wellbeing Using Multivariate Regression  

---

## Overview

This project applies **statistical modeling and visual analytics** to understand which social factors most influence residents’ satisfaction across regions of **England**.  
Using **multiple linear regression (MLR)** and region-level analysis, the study quantifies how perceptions of **influence**, **community cohesion**, **belonging**, and **drug use** shape overall satisfaction.

The work demonstrates end-to-end data analysis - from preprocessing and descriptive exploration to model evaluation and interpretation - presented in a clear, reproducible R workflow.

---

## Objectives

1. Identify key community-level factors predicting local satisfaction.  
2. Assess how these relationships differ across English regions.  
3. Evaluate model validity using robust statistical diagnostics.  
4. Present findings through interpretable visuals and concise narratives.

---

## Data Summary

**Dataset:** `UKContentment.csv`  
**Source:** UK social wellbeing survey (simulated/aggregated data for analysis purposes)  
**Observations:** 1,000 local authorities across multiple English regions  

| Variable | Description |
|-----------|-------------|
| `Influence` | Residents’ perceived influence on local decisions |
| `GetOnWell` | Cohesion -
how well people from different backgrounds get along |
| `Belong` | Sense of belonging to the community |
| `DrugUse` | Perceived local drug problem (higher = worse) |
| `Overallpoint` | Overall satisfaction score |
| `Area` | Region of England |

---

## Methodology

### 1. **Exploratory Data Analysis**
- Computed descriptive statistics and visualized distributions.  
- Identified variable correlations and checked for potential multicollinearity.

### 2. **Model Development**
Fitted a **multiple linear regression** model:

\[
Overallpoint \sim Influence + GetOnWell + Belong + DrugUse
\]

Diagnostics included:
- Normality of residuals (Q–Q plot)  
- Homoscedasticity (Residual vs Fitted)  
- Multicollinearity (VIF)  
- Model fit metrics (R², Adjusted R², F-statistic)

### 3. **Regional Modeling**
- Applied the same model separately for each region.  
- Visualized coefficients to reveal spatial heterogeneity in predictors.

---

## Key Findings

### National Level
- **Community Cohesion (`GetOnWell`)** and **Belonging (`Belong`)** are the strongest positive predictors.  
- **Drug Use (`DrugUse`)** has a significant negative effect nationwide.  
- The model explains approximately **85% of the variance** in satisfaction (R² ≈ 0.85).

### Regional Differences
- **London:** Strongest positive influence from `GetOnWell`; weaker or slightly negative effect from `Belong` and `Influence`.  
- **Yorkshire and The Humber:** Largest negative effect from `DrugUse`.  
- Results emphasize **region-specific dynamics**, suggesting that the drivers of satisfaction vary geographically.

---

## Visual Highlights

| Visualization | Purpose |
|----------------|----------|
| **Descriptive Tables** | Summarize key indicators |
| **Diagnostic Plots** | Validate regression assumptions |
| **Faceted Coefficient Plot** | Show regional variability in predictors |
| **Grouped Comparison Plot** | Compare factor strength across regions |

> *“Data reveals that community cohesion is not just influential - it’s the foundation of satisfaction.”*

---

## Technical Stack

| Purpose | R Packages |
|----------|-------------|
| Data Handling | `tidyverse`, `data.table`, `readr` |
| Modeling | `broom`, `car` |
| Visualization | `ggplot2`, `ggpubr` |
| Reporting | `knitr`, `kableExtra`, `gt` |
| Reproducibility | `set.seed()`, optional `renv` |

---

## Results Summary

- The analysis integrates **statistical rigor** with **effective storytelling**.  
- Model assumptions were validated and visual diagnostics confirmed a robust fit.  
- Regional modeling enhanced interpretability and practical insight.  

---

## Skills Demonstrated

- **Statistical modeling:** Linear regression, diagnostics, multicollinearity assessment  
- **Data visualization:** ggplot2 for regional and diagnostic insights  
- **Reproducible analysis:** Clean, modular R code following tidy principles  
- **Interpretation & communication:** Translating complex results into actionable insights  

---

## Takeaway

This project showcases practical expertise in **data analysis, modeling, and visualization** using R - framed around a real-world social context.  
It demonstrates the ability to move from **raw data to interpretable, policy-relevant insights**, a key skill for modern data science roles.
