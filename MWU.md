# Mann-Whitney U Test: Complete Step-by-Step Guide

The **Mann-Whitney U test** is a non-parametric statistical test used to compare the difference between **two independent (unpaired) groups**. It determines whether there is a statistically significant difference between the distributions of the two groups **without assuming normal distribution** since parametric assumptions are not satisfied.

## Our Dataset: Russia vs Romania Measurements

| Russia | Romania |
|--------|---------|
| 45     | 48      |
| 39     | 62      |
| 60     |  56     |
| 52     |  37     |
| 43     |  50     |

**Group Sizes:**  
- Russia: n₁ = 5  
- Romania: n₂ = 5  
- Total N = 10

---

### Step 1: Combine, Order, and Rank All Values

#### 1.1 Combine all values
Russia: 45, 39, 60, 52, 43  
Romania: 48, 62, 37, 56, 50  

Combined: 45, 39, 60, 52, 43, 48, 62, 37, 56, 50

#### 1.2 Sort from smallest to largest
37, 39, 43, 45, 48, 50, 52, 56, 60, 62

#### 1.3 Assign ranks

| Value | Original Group | Rank |
|-------|----------------|------|
| 37    | Romania        | 1    |
| 39    | Russia         | 2    |
| 43    | Russia         | 3    |
| 45    | Russia         | 4    |
| 48    | Romania        | 5    |
| 50    | Romania        | 6    |
| 52    | Russia         | 7    |
| 56    | Romania        | 8    |
| 60    | Russia         | 9    |
| 62    | Romania        | 10   |

> *Note: If ties occur, assign the average rank.*

---

### Step 2: Calculate U-Statistics

#### 2.1 Rank sums for each group
Russia ranks: 2 + 3 + 4 + 7 + 9 = **25**  
Romania ranks: 1 + 5 + 6 + 8 + 10 = **30**

#### 2.2 Calculate U-Statistic

```math
U = \min(Russia\_Rank\_Sum, Romania\_Rank\_Sum) = \min(25, 30) = 25
```
**Formula:**
```math
U = 25 - \frac{5(5+1)}{2}
```

```math
U = 25 - \frac{5 \times 6}{2}
```

```math
U = 25 - 15 = 10
```



---

### Step 3: Find Critical Value and Draw Conclusion

- Significance level: **α = 0.05** (5%)
- Test type: **Two-tailed**
- Sample sizes: n₁ = 5, n₂ = 5

**Critical U value** (from Mann-Whitney table, α = 0.05 two-tailed): **2**

#### Decision rule
- Reject H₀ if U ≤ 2
- Fail to reject H₀ if U > 2

#### Result
Our U = **10**  
Critical U = **2**  
**10 > 2** → **Fail to reject H₀**

#### Conclusion
> There is **insufficient evidence** at the 5% significance level to conclude that the distributions of measurements from Russia and Romania are significantly different.

---

### Summary of Results

| Component                      | Value |
|-------------------------------|-------|
| Russia Rank Sum (R₁)          | 25    |
| Romania Rank Sum (R₂)         | 30    |
| U₁ (Russia)                   | 15    |
| U₂ (Romania)                  | 10    |
| Test Statistic U              | **10**    |
| Critical U (α=0.05, two-tailed)| 2     |
| Decision                      | Fail to reject H₀ |

---

### Key Points to Remember

- **Null Hypothesis (H₀):** The two population distributions are equal
- **Alternative Hypothesis (H₁):** The two population distributions are not equal
- **Assumptions:**
  - Two independent samples
  - Data at least ordinal
  - Similar shape of distributions (if interpreting median difference)
- **When to use Mann-Whitney U:**
  - Data not normally distributed
  - Small sample sizes
  - Ordinal data or violation of t-test assumptions
- **Important Notes:**
  - The test compares **distributions**, not just means/medians
  - For n > 20, U approximates a normal distribution (z-test possible)
  - Always verify assumptions before choosing the test

### Common Critical Values (Two-Tailed, α = 0.05)

| n₁ | n₂ | Critical U |
|----|----|------------|
| 5  | 5  | 2          |
| 5  | 6  | 3          |
| 5  | 7  | 4          |
| 6  | 6  | 5          |
| 7  | 7  | 8          |
| 8  | 8  | 13         |


> This example uses hypothetical data for educational purposes only.






