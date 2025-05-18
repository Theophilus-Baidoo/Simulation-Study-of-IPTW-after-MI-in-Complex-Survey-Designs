# Simulation-Study-of-IPTW-after-MI-in-Complex-Survey-Designs


## Study Overview

This simulation study evaluates the performance of **inverse probability of treatment weighting (IPTW)** applied after **multiple imputation (MI)**, in the context of **complex survey data**. 

The simulation accounts for missing data, survey weights, stratification, and clustering. It follows the methodology outlined in:

> Pishgar F, Greifer N, Leyrat C, Stuart EA (2021). "MatchThem: Matching and Weighting after Multiple Imputation." The R Journal*, 13(2), 378–397.  
> [https://journal.r-project.org/archive/2021/RJ-2021-073/RJ-2021-073.pdf](https://journal.r-project.org/archive/2021/RJ-2021-073/RJ-2021-073.pdf)

---

## Simulation Objectives

- Generate 1,000 individuals synthetic survey data with realistic missingness and design structure
- Apply multiple imputation using predictive mean matching
- Estimate IPTW using logistic propensity score models within imputed datasets
- Assess covariate balance before and after weighting using standardized mean differences
- Fit modified Poisson regression models with survey design to estimate risk ratios
- Pool results across imputed datasets using Rubins rules

---

## Variables Simulated

| Variable       | Description                                      |
|----------------|--------------------------------------------------|
| `age`          | Continuous variable (years)                      |
| `sex`          | Binary categorical variable (`Male`, `Female`)  |
| `race`         | Categorical variable (`White`, `Black`, `Hispanic`, `Other`) |
| `income`       | Continuous variable (annual household income)   |
| `bmi`          | Continuous variable (body mass index)           |
| `treatment`    | Binary exposure variable (e.g., intervention group) |
| `outcome`      | Binary outcome variable                         |
| `weight`       | Survey weight                                   |
| `strata`       | Stratification variable                         |
| `psu`          | Primary sampling unit (cluster)                 |

---


