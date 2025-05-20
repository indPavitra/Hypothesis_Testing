# Drug Safety Clinical Trial Analysis

This project analyzes a clinical trial dataset comparing two groups — **Drug** and **Placebo** — to explore safety outcomes and demographic differences using statistical tests and visualizations.

---

## Dataset

The dataset `drug_safety.csv` includes:
- `trx`: Treatment group (`Drug` or `Placebo`)
- `adverse_effects`: Whether the patient experienced side effects (`Yes` or `No`)
- `num_effects`: Number of effects experienced
- `age`: Age of the patient

---

## Objectives

- Compare the proportion of patients with adverse effects between Drug and Placebo groups.
- Check if the number of effects is associated with the treatment type.
- Analyze whether age distribution differs between the two groups.

---

## Key Statistical Methods

| Test | Purpose | Package |
|------|---------|---------|
| **Z-test for proportions** | To check if the % of adverse effects is significantly different between groups | `statsmodels` |
| **Chi-Square Test** | To determine if the number of effects is associated with the treatment group | `pingouin` |
| **Normality Test (Shapiro)** | To test if age data is normally distributed | `pingouin` |
| **Mann-Whitney U Test** | To compare age distributions between the two groups (non-parametric) | `pingouin` |

---

## Visualizations

- **Histogram** of patient age distributions by treatment group using `seaborn`.

---

## Project Steps

1. Load and explore the dataset.
2. Analyze adverse effect rates per group.
3. Perform a **proportions Z-test** on the adverse effect counts.
4. Use **Chi-squared test** to check independence between `num_effects` and `trx`.
5. Plot age distribution using `histplot`.
6. Run a **normality test** for age.
7. Perform a **Mann-Whitney U test** to compare age distributions.

---

## NOTES:
All statistical tests use a significance level of α = 0.05.
Mann-Whitney U test was used instead of t-test due to non-normal age distribution.
