# Non-Parametric Tests

This is a collection of practical guides to commonly used non-parametric statistical tests.

This repository provides concise, example-driven explanations (in Markdown) of **six fundamental non-parametric hypothesis tests**:

* **Mann-Whitney U Test** (`mwu.md`) – Compare two independent groups (alternative to independent t-test)
* **Kruskal-Wallis Test** (`kw.md`) – Compare three or more independent groups (alternative to one-way ANOVA)
* **Wilcoxon Signed-Rank Test** (`wilcox.md`) – Compare two related/paired samples (alternative to paired t-test)
* **Friedman Test** (`friedman.md`) – Compare three or more related/paired samples (alternative to repeated-measures ANOVA)
* **McNemar Test** (`mcnemar.md`) – Test for changes in paired nominal (binary) outcomes (2×2 contingency table)
* **Spearman Rank Correlation** (`spearman.md`) – Assess monotonic association between two variables (alternative to Pearson correlation)

Ideal for anyone who needs a quick but solid reference without heavy theory overload.

## Contents

| File                       | Test                      | Use Case                                     | Parametric Equivalent       |
| -------------------------- | ------------------------- | -------------------------------------------- | --------------------------- |
| [mwu.md](mwu.md)           | Mann-Whitney U            | Two independent samples                      | Independent t-test          |
| [kw.md](kw.md)             | Kruskal-Wallis H          | Three or more independent samples            | One-way ANOVA               |
| [wilcox.md](wilcox.md)     | Wilcoxon Signed-Rank      | Two related/paired samples                   | Paired t-test               |
| [friedman.md](friedman.md) | Friedman Test             | Three or more related/paired samples         | Repeated-measures ANOVA     |
| [mcnemar.md](mcnemar.md)   | McNemar Test              | Paired nominal data (2×2 contingency table)  | Cochran's Q / Marginal test |
| [spearman.md](spearman.md) | Spearman Rank Correlation | Rank-based association between two variables | Pearson correlation         |



Each file includes:
- Explains when to use the test
- States assumptions (and how non-parametric tests relax them)
- Shows hypotheses (H₀ and H₁)
- Provides step-by-step interpretation of results
- Includes Python (scipy/statsmodels) and R examples
- Shows how to report results in papers/reports

## Why Non-Parametric Tests?

Use these when your data:
- Is not normally distributed
- Contains outliers
- Is ordinal (ranks, Likert scales, etc.)
- Has unequal variances between groups
- Sample size is small

