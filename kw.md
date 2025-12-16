# Kruskal-Wallis Test Example

## Introduction
The **Kruskal-Wallis Test** is a non-parametric alternative to one-way ANOVA. It is used to determine whether there are statistically significant differences between the medians of three or more independent groups.

## Data (Step 1)

| Russia       | Romania      | China        |
|--------------|--------------|--------------|
| 8.2          | 10.2         | 13.5         |
| 10.3         | 9.1          | 8.4          |
| 9.1          | 13.9         | 9.6          |
| 12.6         | 14.5         | 13.8         |
| 11.4         | 9.1          | 17.4         |
| 13.2         | 16.4         | 15.3         |

- Group sizes: n₁ = 6 (Russia), n₂ = 6 (Romania), n₃ = 6 (China)  
- Total N = 18

## Hypotheses (Step 2)
- **H₀**: The population medians of the three countries are equal.  
- **H₁**: At least one population median differs (two-tailed test).

## Step 3: Rank all observations from smallest to largest (ties receive average ranks)

| Value | Country  | Rank  | Notes                              |
|-------|----------|-------|------------------------------------|
| 8.2   | Russia   | 1     |                                    |
| 8.4   | China    | 2     |                                    |
| 9.1   | Russia   | 4     | Tie: three 9.1 values → ranks 3,4,5 → average = 4 |
| 9.1   | Romania  | 4     |                                    |
| 9.1   | Romania  | 4     |                                    |
| 9.6   | China    | 6     |                                    |
| 10.2  | Romania  | 7     |                                    |
| 10.3  | Russia   | 8     |                                    |
| 11.4  | Russia   | 9     |                                    |
| 12.6  | Russia   | 10    |                                    |
| 13.2  | Russia   | 11    |                                    |
| 13.5  | China    | 12    |                                    |
| 13.8  | China    | 13    |                                    |
| 13.9  | Romania  | 14    |                                    |
| 14.5  | Romania  | 15    |                                    |
| 15.3  | China    | 16    |                                    |
| 16.4  | Romania  | 17    |                                    |
| 17.4  | China    | 18    |                                    |

## Step 4: Add ranks to the original table and compute group rank sums

| Russia | Rank | Romania | Rank | China | Rank |
|--------|------|---------|------|-------|------|
| 8.2    | 1    | 10.2    | 7    | 13.5  | 12   |
| 10.3   | 8    | 9.1     | 4    | 8.4   | 2    |
| 9.1    | 4    | 13.9    | 14   | 9.6   | 6    |
| 12.6   | 10   | 14.5    | 15   | 13.8  | 13   |
| 11.4   | 9    | 9.1     | 4    | 17.4  | 18   |
| 13.2   | 11   | 16.4    | 17   | 15.3  | 16   |

- **R₁ (Russia)**    = 1 + 8 + 4 + 10 + 9 + 11 = **43**  
- **R₂ (Romania)**   = 7 + 4 + 14 + 15 + 4 + 17 = **61**  
- **R₃ (China)**     = 12 + 2 + 6 + 13 + 18 + 16 = **67**

## Step 5: Calculate the Kruskal-Wallis statistic H

$$
H = \frac{12}{N(N+1)} \sum_{i=1}^{k} \frac{R_i^2}{n_i} - 3(N+1)
$$

Plugging in the values:

$$
H = \frac{12}{18 \times 19} \left( \frac{43^2}{6} + \frac{61^2}{6} + \frac{67^2}{6} \right) - 3(19) = 1.82
$$

**H ≈ 1.82**

Degrees of freedom: df = k − 1 = 3 − 1 = **2**

## Step 6: Critical value and decision

From the χ² table (df = 2, α = 0.05):  
**Critical value = 5.991**

Since **H = 1.82 < 5.991**, we **fail to reject H₀**.

Note: As alternative, you can also use the Kruskal Wallis TAble where n₁=n₂=n₃ at 5% significance level = 5.801
**Critical value = 5.881**

Since **H = 1.82 < 5.881**, we **fail to reject H₀**.

## Conclusion
At the 5% significance level, there is **no evidence** of a statistically significant difference between the distributions (or medians) of the three countries.

**Kruskal-Wallis test result**: H = 1.82, df = 2, p > 0.05 → **not significant**.

