# Causal Inference in Practice: The Impact of Immigration Policy on Crime Rates

*An econometric study by Ruihang Han applying quasi-experimental methods to estimate the causal effect of immigration policy on crime in the United States.*

---

## 🎯 Research Question & The Identification Challenge

This project investigates a central question in social science: What is the causal effect of a major immigration policy on crime rates?

Moving beyond simple correlation is notoriously difficult due to numerous confounding variables (e.g., economic conditions, policing strategies, demographic shifts). The core challenge of this analysis is to isolate the true causal impact of the policy from these other factors. To achieve this, the project employs a rigorous quasi-experimental research design.

## 📊 Data & Methodology

The analysis leverages a **state-year panel dataset** compiled from [请在此处注明你的数据来源, e.g., FBI UCR, US Census Bureau].

The primary analytical tool is a **Two-Way Fixed Effects (TWFE)** regression model. This powerful panel data method allows us to control for two critical types of unobserved confounders:
1.  **State Fixed Effects:** Accounts for any time-invariant characteristics of a state (e.g., culture, geography, historical legal frameworks).
2.  **Year Fixed Effects:** Accounts for any shocks or trends common to all states in a given year (e.g., a national recession, changes in federal law).

The model takes the following general form:

`CrimeRate_st = β * Policy_st + α_s + δ_t + ε_st`

Where `α_s` represents state fixed effects and `δ_t` represents year fixed effects. The coefficient of interest is `β`, which captures the estimated causal effect of the policy.

## 🛡️ Rigorous Robustness Checks

To ensure the validity of the causal claims, a series of robustness checks were performed, following best practices in modern econometrics:

* **Clustered Standard Errors:** Standard errors were clustered at the state level to account for potential serial correlation within states over time, leading to more conservative and reliable inference.

* **Event Study Design:** An event study model was estimated to test the crucial **parallel trends assumption**. This also allows for the examination of dynamic, year-by-year effects of the policy both before and after its implementation. The absence of pre-treatment effects is strong evidence for the validity of the research design.

* **Placebo Tests:** [请在此处简要描述你做的安慰剂检验, e.g., A placebo test was conducted by assigning the policy to a random set of untreated states to ensure that the main result was not driven by chance.]

## 📈 Results & Findings

[**请在此处插入你的关键发现。** 例如: "The primary finding from the TWFE model indicates that the policy led to a statistically significant [increase/decrease] of X% in property crime rates, with no significant effect on violent crime. The event study plot below shows no evidence of pre-existing trends in the years leading up to the policy change, strengthening the causal interpretation of the result."]

**Event Study Plot:**
![Event Study Plot]([INSERT YOUR EVENT STUDY PLOT IMAGE HERE])
*Caption: Year-by-year effects of the policy on crime rates. The vertical line indicates the year of policy implementation. Confidence intervals are shown in gray.*

## 📦 Tools & Libraries Used

* **Language:** R / Python
* **Core Packages:**
    * **R:** `plm`, `fixest` (for fixed effects models), `dplyr`, `ggplot2`
    * **Python:** `statsmodels`, `linearmodels`, `pandas`, `plotnine`

---

This project demonstrates a complete workflow for a rigorous, end-to-end causal inference study, from research design and data modeling to robustness checking and interpretation.
