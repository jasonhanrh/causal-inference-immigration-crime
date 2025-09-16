# The Impact of Restrictive Immigration Policies on Violent Crime: A Fixed-Effects Analysis

*An econometric study by Ruihang Han analyzing the causal effect of state-level restrictive immigration laws on violent crime rates in the United States from 2005 to 2012. The full research paper can be found [here](immigration_crime.pdf).*

---

## 🎯 Research Question & Motivation

[cite_start]The relationship between immigration policy and crime rates is a subject of intense public and academic debate[cite: 497]. [cite_start]While many studies have focused on the socio-economic impacts of immigration, the specific causal effect of the *quantity* of restrictive state-level laws on public safety remains under-examined[cite: 500, 508].

[cite_start]This project addresses a critical gap in the literature by asking: **Does an increase in the number of restrictive immigration laws enacted by a state lead to a causal change in its violent crime rate?** [cite: 522]

To answer this, the study moves beyond simple correlations by employing a quasi-experimental design to control for the vast unobserved differences between states.

## 📊 Data & Methodology

[cite_start]The analysis leverages a state-level panel dataset covering all 50 U.S. states from 2005 to 2012, sourced from the **Correlates of State Policy Project**[cite: 532, 533].

[cite_start]The core of the study is a **Two-Way Fixed-Effects (TWFE)** regression model, which is specified as follows[cite: 618, 621]:

`ViolentCrimeRate_it = β * RestrictiveLaws_it + Controls_it + StateEffects_i + YearEffects_t + ε_it`

This model is designed to isolate the causal effect of interest (`β`) by:
1.  [cite_start]**Controlling for State Fixed Effects (`StateEffects_i`):** This accounts for all time-invariant differences between states, such as unique cultural, historical, or institutional factors that might affect crime rates[cite: 628, 629].
2.  [cite_start]**Controlling for Year Fixed Effects (`YearEffects_t`):** This accounts for national trends or shocks that affect all states in a given year, such as a nationwide recession or changes in federal policy[cite: 631, 632].
3.  [cite_start]**Including Covariates (`Controls_it`):** The model includes a rich set of time-varying controls, such as unemployment rates, poverty rates, income inequality (Gini coefficient), and gun control laws, to account for other potential drivers of crime[cite: 538, 652, 654, 671].
4.  [cite_start]**Testing Interaction Effects:** The analysis also explores whether the impact of restrictive laws is moderated by socio-economic conditions, such as poverty and unemployment levels[cite: 680, 682].

## 📈 Key Findings & Visualizations

The study's findings are robust across multiple model specifications and challenge common narratives about immigration and crime.

### 1. No Significant Causal Effect of Restrictive Laws on Crime

[cite_start]The central finding of this research is that **the annual count of restrictive immigration laws has no statistically significant effect on violent crime rates**[cite: 854]. [cite_start]The coefficient for this variable is small and not statistically different from zero across all fixed-effects models[cite: 721]. [cite_start]This suggests that enacting such laws is an ineffective strategy for reducing violent crime[cite: 770].

### 2. States with More Restrictive Laws Have Higher Crime Rates (Correlation, not Causation)

[cite_start]While the laws themselves do not appear to be the cause, states that enact high numbers of restrictive laws consistently exhibit higher violent crime rates than states with fewer such laws[cite: 761, 857]. [cite_start]The fixed-effects model accurately predicts this persistent gap, suggesting that deeper, pre-existing structural factors—rather than the immigration laws themselves—are the primary drivers of crime rates in these states[cite: 766, 769].

![Predicted vs. Actual Crime Rates by Law Group]([INSERT FIGURE 3 IMAGE HERE])
[cite_start]*Caption: The model accurately predicts the persistent gap in crime rates between states with high vs. low numbers of restrictive laws, suggesting the laws themselves are not the driving factor of the trend. [cite: 758, 763]*

### 3. Political Governance is a Stronger Correlate of Crime Rates

The analysis reveals a significant difference based on the political party governing a state.
* [cite_start]**Democrat-governed states consistently have lower violent crime rates**[cite: 799, 860].
* [cite_start]**Republican-governed states, which tend to enact more restrictive laws, consistently have higher violent crime rates**[cite: 797].

[cite_start]This suggests that broader governance styles and policy priorities (e.g., social investments vs. punitive enforcement) are more strongly associated with public safety outcomes than the specific number of immigration laws[cite: 846, 847].

![Predicted vs. Actual Crime Rates by Political Party]([INSERT FIGURE 4 IMAGE HERE])
[cite_start]*Caption: A persistent gap in violent crime rates is observed between states governed by different political parties. [cite: 776]*

## 💡 Conclusion & Policy Implications

[cite_start]The evidence from this study suggests that state-level restrictive immigration policies are not an effective tool for reducing violent crime[cite: 855]. [cite_start]The findings indicate that violent crime trends are more deeply rooted in broader socio-economic conditions and governance styles[cite: 862]. [cite_start]Therefore, policies aimed at enhancing public safety should likely focus on addressing these underlying structural issues rather than on punitive immigration measures[cite: 865, 868].

## 📦 Tools & Libraries Used

* **Language:** R / Python
* **Core Packages:**
    * **R:** `plm`, `fixest` (for fixed effects models), `dplyr`, `ggplot2`
    * **Python:** `statsmodels`, `linearmodels`, `pandas`, `plotnine`

---

This project demonstrates an end-to-end workflow for a rigorous, quasi-experimental research study, from literature review and research design to advanced econometric modeling and policy-relevant interpretation.
