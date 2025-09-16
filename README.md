# Causal Inference in Practice: A Methodological Approach to Immigration and Crime

*An econometric project applying quasi-experimental methods to estimate the causal effect of state-level immigration policies on violent crime rates in the United States.*

---

## 🎯 Research Question & Motivation

This project investigates a central question in social science: What is the causal effect of a major immigration policy on crime rates?

Moving beyond simple correlation is notoriously difficult due to numerous confounding variables (e.g., economic conditions, policing strategies, demographic shifts). The core challenge of this analysis is to isolate the true causal impact of the policy from these other factors. To achieve this, the project employs a rigorous quasi-experimental research design.

## 📊 Data & Methodology

The analysis utilizes a state-level panel dataset covering all 50 U.S. states from 2005 to 2012, sourced from the **Correlates of State Policy Project** and the economic research database at **Michigan State University**.

The primary analytical tool is a **Two-Way Fixed-Effects (TWFE)** regression model. This powerful panel data method allows us to control for two critical types of unobserved confounders:
1.  **State Fixed Effects:** Accounts for any time-invariant characteristics of a state (e.g., culture, geography, historical legal frameworks).
2.  **Year Fixed Effects:** Accounts for any shocks or trends common to all states in a given year (e.g., a national recession, changes in federal law).

The model takes the following general form:

`CrimeRate_st = β * Policy_st + Controls_it + StateEffects_i + YearEffects_t + ε_it`

The goal is to obtain a robust estimate of the coefficient `β`, which represents the causal effect of the policy.

## 🛡️ Rigorous Robustness Checks

To ensure the validity of the causal claims, a series of robustness checks were designed and implemented, following best practices in modern econometrics:

* **Clustered Standard Errors:** Standard errors are clustered at the state level to account for potential serial correlation within states over time, leading to more conservative and reliable inference.

* **Event Study Design:** An event study model is specified to test the crucial **parallel trends assumption**. This also allows for the examination of dynamic, year-by-year effects of the policy both before and after its implementation.

* **Placebo Tests:** Placebo tests are designed to ensure that any potential findings are not driven by chance or spurious correlation.

## 🛠️ Project Scope & Skills Demonstrated

This repository contains the code and methodology to conduct a complete, end-to-end causal inference study. The focus is on showcasing the technical approach to answering a complex social science question with modern quantitative tools.

Key skills demonstrated in this project include:
* **Research Design:** Formulating a testable hypothesis and employing a quasi-experimental research design (TWFE).
* **Panel Data Modeling:** Implementing and interpreting fixed-effects regression models.
* **Causal Validation:** Applying advanced techniques like event studies and placebo tests to validate causal claims.
* **Reproducible Research:** Structuring code and data to ensure the analysis is transparent and reproducible.

## 📦 Tools & Libraries Used

* **Language:** R / Python
* **Core Packages:**
    * **R:** `plm`, `fixest` (for fixed effects models), `dplyr`, `ggplot2`
    * **Python:** `statsmodels`, `linearmodels`, `pandas`, `plotnine`
