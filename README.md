# Impact of Policymaking on UPI Growth in India

## Overview

This project investigates how government and regulatory interventions influenced the growth of Unified Payments Interface (UPI) adoption in India between 2016 and 2026. Using statistical modeling, hypothesis testing, and time-series analysis, the study evaluates the measurable impact of major policy decisions on transaction growth.

## Dataset

- **Sources:** RBI, NPCI, Government policy releases, and public policy bulletins
- **Time Period:** April 2016 – March 2026
- **Observations:** 120 monthly records

### Variables

#### UPI Metrics
- Transaction Volume (Millions)
- Transaction Value (INR Crores)

#### Policy Indicators
- Demonetization (2016)
- COVID-19 Lockdown (2020)
- Zero MDR (2020)
- UPI Lite Launch (2022)
- Credit Card on UPI (2022)
- Tighter Limits (2025)

#### Derived Features
- Average Ticket Size
- Month-over-Month Growth (Volume & Value)

## Methodology

### Data Preparation

- Standardized date and unit formats
- Processed missing values
- Constructed growth-based features
- Created binary indicators for major policy interventions

### Exploratory Data Analysis

- Distribution analysis of transaction volume and value
- Correlation analysis between key variables
- Structural break identification around major policy events
- Outlier and normality assessment

### Statistical Analysis

- Multiple Linear Regression (MLR)
- t-tests for coefficient significance
- F-test for overall model significance
- Variance Inflation Factor (VIF) analysis
- Wilcoxon Rank Sum Test
- Moving Average (MA3, MA6) trend analysis

## Results

### Regression Performance

- **R² = 0.872**
- **Adjusted R² = 0.865**

### Key Findings

- Credit Card on UPI and Tighter Limits were statistically significant drivers of transaction growth.
- Demonetization, Zero MDR, COVID Lockdown, and Average Ticket Size were not significant predictors in the final model.
- VIF analysis revealed multicollinearity between Zero MDR and COVID Lockdown; the model was refined by removing Zero MDR.
- Wilcoxon Rank Sum Test (**p = 2.41 × 10⁻⁶**) confirmed a significant difference between pre-2020 and post-2020 UPI growth.
- Moving-average analysis identified 2020 as a structural turning point in adoption.

## Key Insights

- UPI growth is strongly influenced by targeted policy interventions.
- High-frequency, low-value transactions drive the ecosystem more than ticket size.
- Later policy measures had a greater measurable impact than early interventions.
- UPI has evolved into a core component of India's digital financial infrastructure.

## Tools Used

- R
- RStudio
- tidyverse
- ggplot2
- dplyr

## Report & Source Files

The repository contains the full project report and the corresponding R code embedded within the LaTeX source files used to generate the report. As the project was developed using an RStudio–LaTeX workflow, a separate standalone `.R` file is not included.
