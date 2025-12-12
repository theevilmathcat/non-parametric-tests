# Non-Parametric Tests

This is a collection of practical guides to commonly used non-parametric statistical tests.

This repository provides concise, example-driven explanations (in Markdown) of three fundamental non-parametric hypothesis tests:

- **Mann-Whitney U Test** (`mwu.md`) – Compare two independent groups (alternative to independent t-test)
- **Kruskal-Wallis Test** (`kw.md`) – Compare three or more independent groups (alternative to one-way ANOVA)
- **Wilcoxon Signed-Rank Test** (`wilcox.md`) – Compare two related/paired samples (alternative to paired t-test)

Ideal for students, researchers, data analysts, and anyone who need a quick but solid reference without heavy theory overload.

## Contents

| File             | Test                        | Use Case                                 | Parametric Equivalent      |
|------------------|-----------------------------|-------------------------------------------|----------------------------|
| [mwu.md](mwu.md)         | Mann-Whitney U              | Two independent samples                   | Independent t-test         |
| [kw.md](kw.md)           | Kruskal-Wallis H            | Three or more independent samples         | One-way ANOVA              |
| [wilcox.md](wilcox.md)       | Wilcoxon Signed-Rank        | Two related/paired samples                | Paired t-test              |

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

## Quick Start Examples

```python
# Python - Mann-Whitney U
from scipy.stats import mannwhitneyu
stat, p = mannwhitneyu(group1, group2)
print(f"U = {stat}, p = {p:.4f}")
