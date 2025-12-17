# Statistical Tests: Distribution Tables Reference

A guide to which distribution tables can be used for various parametric and non-parametric statistical tests, based on sample size.

## Non-Parametric Tests Using Multiple Tables

### Kruskal-Wallis Test

| Sample Size Condition | Distribution Table Used | Degrees of Freedom |
|----------------------|------------------------|-------------------|
| Small samples (n < 5 per group OR k < 3 groups) | Kruskal-Wallis tables | - |
| Large samples (n ≥ 5 per group AND k ≥ 3 groups) | Chi-square (χ²) distribution | df = k - 1 |

**Note:** The H statistic approximates the chi-square distribution for larger samples.

---

### Friedman Test

| Sample Size Condition | Distribution Table Used | Degrees of Freedom |
|----------------------|------------------------|-------------------|
| Small samples (n < 10 or k < 4) | Friedman tables | - |
| Large samples (n ≥ 10 and k ≥ 4) | Chi-square (χ²) distribution | df = k - 1 |

**Note:** Used for repeated measures or matched groups with 3+ conditions.

---

### Mann-Whitney U Test

| Sample Size Condition | Distribution Table Used | Notes |
|----------------------|------------------------|-------|
| Small samples (n₁, n₂ ≤ 20) | Mann-Whitney U tables | Exact distribution |
| Large samples (n₁, n₂ > 20) | Normal (z) distribution | Use z-test approximation with continuity correction |

**Note:** Non-parametric alternative to independent samples t-test.

---

### Wilcoxon Signed-Rank Test

| Sample Size Condition | Distribution Table Used | Notes |
|----------------------|------------------------|-------|
| Small samples (n ≤ 25-30) | Wilcoxon signed-rank tables | Exact distribution |
| Large samples (n > 25-30) | Normal (z) distribution | Use z-test approximation |

**Note:** Non-parametric alternative to paired samples t-test.

---

### Spearman's Rank Correlation (ρ)

| Sample Size Condition | Distribution Table Used | Notes |
|----------------------|------------------------|-------|
| Small samples (n < 30) | Spearman's rho tables | Exact critical values |
| Large samples (n ≥ 30) | t-distribution via transformation | t = ρ√[(n-2)/(1-ρ²)], df = n - 2 |

**Note:** Non-parametric alternative to Pearson correlation.

---

## Parametric Tests

### Independent Samples t-test

| Sample Size Condition | Distribution Table Used | Degrees of Freedom |
|----------------------|------------------------|-------------------|
| All sample sizes | t-distribution | df = n₁ + n₂ - 2 (pooled variance) |
| All sample sizes | t-distribution | df = Welch-Satterthwaite formula (unequal variances) |

**Note:** Only uses t-distribution tables.

---

### Paired Samples t-test

| Sample Size Condition | Distribution Table Used | Degrees of Freedom |
|----------------------|------------------------|-------------------|
| All sample sizes | t-distribution | df = n - 1 |

**Note:** Only uses t-distribution tables.

---

### One-Way ANOVA (F-test)

| Sample Size Condition | Distribution Table Used | Degrees of Freedom |
|----------------------|------------------------|-------------------|
| All sample sizes | F-distribution | df₁ = k - 1, df₂ = N - k |

**Special relationship:** When df₁ = 1, F = t². You could theoretically use t-tables, but F-tables are standard practice.

---

### Chi-Square Test of Independence

| Sample Size Condition | Distribution Table Used | Degrees of Freedom |
|----------------------|------------------------|-------------------|
| Expected frequency ≥ 5 in all cells | Chi-square (χ²) distribution | df = (r - 1)(c - 1) |

**Note:** Only uses chi-square distribution tables. For smaller expected frequencies, consider Fisher's exact test.

---

### Pearson Correlation Coefficient (r)

| Sample Size Condition | Distribution Table Used | Degrees of Freedom |
|----------------------|------------------------|-------------------|
| All sample sizes | t-distribution via transformation | t = r√[(n-2)/(1-r²)], df = n - 2 |
| All sample sizes | Pearson correlation tables | df = n - 2 |

**Note:** Can use either correlation tables or convert to t-statistic.

---

## Quick Reference Summary

### Tests Using Multiple Distribution Tables
- **Kruskal-Wallis**: Kruskal-Wallis tables (small n) → Chi-square (large n)
- **Friedman**: Friedman tables (small n) → Chi-square (large n)
- **Mann-Whitney U**: U tables (small n) → Normal/z (large n)
- **Wilcoxon Signed-Rank**: Wilcoxon tables (small n) → Normal/z (large n)
- **Spearman's ρ**: Spearman tables (small n) → t-distribution (large n)

### Tests Using Single Distribution Table
- **t-tests**: t-distribution only
- **ANOVA**: F-distribution only
- **Chi-square independence**: Chi-square distribution only
- **Pearson's r**: t-distribution or correlation tables

---

## General Guidelines

1. **Small Sample Sizes**: Use exact distribution tables specific to the test
2. **Large Sample Sizes**: Many non-parametric tests approximate well-known distributions (chi-square, normal)
3. **Asymptotic Approximations**: The larger the sample, the better the approximation to chi-square or normal distributions
4. **Always Check Assumptions**: Ensure your sample size meets the threshold for using approximation methods


**Last Updated:** December 2025  
**License:** The Evil Math Cat  
**Contributions:** Gimme me cat food damn it.
