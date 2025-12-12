# Wilcoxon Signed-Rank Test Example

## Introduction
The **Wilcoxon Signed-Rank Test** is a non-parametric statistical test used to compare two related samples (e.g., before and after measurements) to determine whether their population mean ranks differ significantly. It is appropriate when the data are paired and the differences are not necessarily normally distributed.

In this example, we have 5 paired observations:

| Subject | Before | After |
|---------|--------|-------|
| 1       | 1      | 2     |
| 2       | 6      | 3     |
| 3       | 8      | 10    |
| 4       | 9      | 3     |
| 5       | 10     | 5     |

## Hypotheses
- **Null hypothesis (H₀)**: There is no difference in the median between the before and after measurements (the median of the differences is zero).  
- **Alternative hypothesis (H₁)**: There is a difference in the median between the before and after measurements (two-tailed test).

## Step-by-Step Calculation

### Step 1: Compute the differences (Before − After)

| Subject | Before | After |
|---------|--------|-------|
| 1       | 1      | 2     |
| 2       | 6      | 3     |
| 3       | 8      | 10    |
| 4       | 9      | 3     |
| 5       | 10     | 5     |

### Step 2: Absolute differences

| Absolute difference \|d\| |
|----------------------------|
| 1                          |
| 3                          |
| 2                          |
| 6                          |
| 5                          |

### Step 3: Assign signed ranks from smallest to largest.

| Absolute difference \|d\| | Rank (from smallest to largest) |
|----------------------------|---------------------------------|
| 1                          | 1                               |
| 3                          | 3                               |
| 2                          | 2                               |
| 6                          | 5                               |
| 5                          | 4                               |

### Step 4: Sum of positive and negative ranks

- Sum of negative ranks (w⁻): 1 + 2 = **3**
- Sum of positive ranks (w⁺): 3 + 5 + 4 = **12**  


### Step 5: Test statistic W
For a two-tailed test, we take the smaller of the two sums:  
**W = min(w⁺, w⁻) = min(12, 3) = 3**

### Step 6: Critical value and decision

- Sample size n = 5 (number of non-zero differences)  
- Significance level α = 0.05 (two-tailed)  
- From the Wilcoxon Signed-Rank critical value table for n = 5, two-tailed, α = 0.05:  
  **Critical value W_cv = 0** (the smallest value that would lead to rejection)

Since W = 3 > 0, we **fail to reject the null hypothesis** at α = 0.05.

### Conclusion
There is not enough evidence to conclude that there is a significant difference between the before and after measurements (p > 0.05).


**Final result**: The change is not statistically significant (W = 3, n = 5, α = 0.05).


