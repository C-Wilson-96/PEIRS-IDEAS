# PEIRS-IDEAS — Patient Engagement in Research Scale Enhanced by Inclusion, Diversity, Equity, Acceptance, and Safety (PEIRS-IDEAS) Scoring (Standalone Function)

[![License: MIT](https://img.shields.io/badge/License-MIT-green.svg)](LICENSE)  
**Status:** pre-CRAN • simple R script for scoring PEIRS

This repository provides a single R function, `calculate_peirs_score()`, to score the **Patients Engaged in Research Scale (PEIRS) - IDEAS**.  
It returns per-respondent **raw totals**, **items answered**, a **standardized 0–100 score**, and a **response status** flag. A custom `summary()` method prints describe‑style statistics (n, mean, SD, min, quartiles, max).

---

## Quick Start (two ways)

### A) Use directly from GitHub


```r
# Load the function straight from this repo (no installation needed)
source("https://raw.githubusercontent.com/C-Wilson-96/PEIRS-IDEAS/main/calculate_peirs_score.R")

# Example: score a data frame 'dat' with PEIRS items as columns
scores <- calculate_peirs_score(dat)
summary(scores)
```

### B) Use locally
```r
# Download calculate_peirs_score.R from this repo, then:
source("calculate_peirs_score.R")

scores <- calculate_peirs_score(dat)
summary(scores)
```

---

## Data Requirements

- One row = one respondent.
- Columns named with PEIRS item IDs (defaults):  
  `PR_IDEAS_1, PR_IDEAS_2, PR_IDEAS_3, PR_IDEAS_4, PR_IDEAS_5, PR_IDEAS_6, PR_IDEAS_7,
  CC_IDEAS_1, CC_IDEAS_2, CC_IDEAS_3, CC_IDEAS_4,
  T_IDEAS_1, T_IDEAS_2, T_IDEAS_3, T_IDEAS_4, T_IDEAS_5, T_IDEAS_6, T_IDEAS_7,
  SU_IDEAS_1, SU_IDEAS_2, SU_IDEAS_3,
  FV_IDEAS_1, FV_IDEAS_2, FV_IDEAS_3,
  BE_IDEAS_1, BE_IDEAS_2, BE_IDEAS_3`.  
- Responses typically on **Likert 1–5**. Non-numeric columns are coerced to numeric; failures become `NA`.

---

## Minimal Reproducible Example

```r
# Simulate toy data with the default 23 items
set.seed(123)
items <- c("PR_IDEAS_1","PR_IDEAS_2","PR_IDEAS_3","PR_IDEAS_4","PR_IDEAS_5",
           "PR_IDEAS_6","PR_IDEAS_7",
           "CC_IDEAS_1","CC_IDEAS_2","CC_IDEAS_3","CC_IDEAS_4",
           "T_IDEAS_1","T_IDEAS_2","T_IDEAS_3","T_IDEAS_4","T_IDEAS_5",
           "T_IDEAS_6","T_IDEAS_7",
           "SU_IDEAS_1","SU_IDEAS_2","SU_IDEAS_3",
           "FV_IDEAS_1","FV_IDEAS_2","FV_IDEAS_3",
           "BE_IDEAS_1","BE_IDEAS_2","BE_IDEAS_3")

dat <- as.data.frame(matrix(sample(1:5, 50*length(items), replace=TRUE), nrow=50))
names(dat) <- items

# Load the scorer
# source("calculate_peirs_score.R")   # if local
# or source("https://raw.githubusercontent.com/quantlover/PEIR-IDEAS/main/calculate_peirs_score.R")

scores <- calculate_peirs_score(dat)
head(scores, 3)
summary(scores)
```

---

## Interpreting `PEIRS_standardized` (0–100)

- **≥ 70%** → High engagement  
- **< 70%** → Low engagement  

Notes:
- The standardized score adjusts for the number of items answered; it is comparable across respondents when using the same item set.
- Use `Response_Status` to flag incomplete responses (default rule: < 10 items answered ⇒ “Too few items”).

---

## Common Options

```r
# Allow partial item sets (compute with present items, warn about missing)
scores <- calculate_peirs_score(dat, strict = FALSE)

# Custom minimum answered threshold
scores <- calculate_peirs_score(dat, min_items_required = 12)

# Non-standard Likert range (e.g., 0–10 mapped to 0–4)
scores <- calculate_peirs_score(dat, scale_from = c(0,10), scale_to = c(0,4))
```

---

## License

Released under the **MIT License**. See the [LICENSE](LICENSE) file.

---

## Suggested Citations

- Hamilton CB, Hoens AM, McQuitty S, McKinnon AM, English K, Backman CL, et al. Development and pre-testing of the Patient Engagement In Research Scale (PEIRS) to assess the quality of engagement from a patient perspective. PLoS One. 2018;13(11):e0206588. doi: https://doi.org10.1371/journal.pone.0206588.  
- **PEIR-IDEAS** (pre-CRAN). “calculate_peirs_score(): Scoring the Patients Engaged in Research Scale (PEIRS) - IDEAS in R.” GitHub: quantlover/PEIR-IDEAS, 2025.
