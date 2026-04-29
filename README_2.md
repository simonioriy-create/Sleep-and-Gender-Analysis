# 😴 Sleep & Gender Analysis

> Exploring the relationship between gender and sleep quality using a dataset of 15,000 individuals.

**Authors:** Ashley Cruz · Hanh Le · Simon Yoshizaki · Koa Choeynim

---

## 📖 Overview

In an ever-advancing digital world where screens dictate our lives, this project investigates how gender relates to sleep quality — and whether the average person is truly getting good rest. Using demographic, screen time, and lifestyle data from Kaggle, we analyzed sleep quality scores across male, female, and other gender identities.

---

## 📊 Dataset

**Source:** [Sleep, Screen Time and Stress Analysis — Kaggle](https://www.kaggle.com/datasets/jayjoshi37/sleep-screen-time-and-stress-analysis)

| Feature | Description |
|---|---|
| Records | 15,000 participants |
| `Sleep_Quality_Score` | Numeric score from 1 (very poor) to 10 (very good) |
| `Gender` | Male, Female, Other |
| Other fields | Screen time behavior, caffeine intake, physical activity, demographics |

---

## 🔬 Methods

### Categorical Analysis — Chi-Square Test
**Question:** Is sleep quality distributed the same across genders?

- **H₀:** p_male = p_female
- **Hₐ:** p_male ≠ p_female
- **Test:** Chi-square (df = 2)

| Gender | n | Mean | Median | SD |
|---|---|---|---|---|
| Female | 7,181 | 6.268 | 6.25 | 1.703 |
| Male | 7,234 | 6.223 | 6.23 | 1.728 |

**Result:** χ² = 4372.172, p ≈ 0 → **Reject H₀**

While statistically significant, the difference between groups (~0.05 points) is negligible in real-world terms.

---

### Numerical Analysis — One-Sample t-Test
**Question:** Is the average sleep quality score significantly greater than neutral (5)?

- **H₀:** μ = 5
- **Hₐ:** μ > 5
- **Test:** One-tailed, one-sample t-test (df = 14,999)

| Statistic | Value |
|---|---|
| n | 15,000 |
| Mean | 6.246 |
| Median | 6.250 |
| Std. Deviation | 1.71 |
| IQR | 2.50 |
| Min | 1 |
| Max | 10 |

**t = 89.05, p ≈ 0 → Reject H₀**

The average sleep quality is significantly above neutral, suggesting participants trend toward better sleep.

---

## 📈 Key Findings

- 🔵 **Gender has minimal real-world impact on sleep quality** — despite a statistically significant chi-square result, the mean difference (~0.05 points) is negligible.
- 🟢 **Most participants report above-average sleep** — the mean (6.246) and median (6.25) are both comfortably above the neutral score of 5.
- 🔴 **9 lower-end outliers** were identified (scores ≈ 1), representing a very small group with extremely poor sleep.
- 📊 Sleep quality scores were roughly **normally distributed**, with ~55% of participants in the "Moderate" category (4–7) and ~35% in the "High" category (≥7).

---

## 🛠️ Tools & Languages

![R](https://img.shields.io/badge/R-276DC3?style=flat&logo=r&logoColor=white)
![ggplot2](https://img.shields.io/badge/ggplot2-tidyverse-blue?style=flat)
![Kaggle](https://img.shields.io/badge/Dataset-Kaggle-20BEFF?style=flat&logo=kaggle&logoColor=white)

- **Language:** R
- **Libraries:** `ggplot2`, `dplyr`, `tidyr`, `scales`
- **Statistical Tests:** Chi-square goodness-of-fit, one-sample t-test

---

## 📚 References

- "Sleep, Screen Time and Stress Analysis." *Kaggle*, [link](https://www.kaggle.com/datasets/jayjoshi37/sleep-screen-time-and-stress-analysis). Accessed 8 April 2026.
- "Sleep Deprivation." *National Heart, Lung, and Blood Institute*, [link](https://www.nhlbi.nih.gov/health/sleep-deprivation). Accessed 13 April 2026.
