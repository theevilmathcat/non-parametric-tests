# Friedman Test – Weightlifting Example (Non-parametric repeated measures)

## When do we use the Friedman test?
We use the Friedman test when we have:
- One group of lifters (same athletes)
- Measured 3 or more times (repeated measures)
- The data is **not normally distributed** (or is ordinal)
- We want to know if there is a significant difference between the conditions

### Weightlifting Example
We tested 12 powerlifters’ **1RM back squat (kg)** under 3 different conditions:
- Normal day (no music, normal rest)
- With hype music
- After consuming 400 mg caffeine

Data (in kg):

| Lifter | Normal | Hype Music | Caffeine |
|--------|--------|------------|----------|
| 1      | 180    | 185        | 190      |
| 2      | 160    | 165        | 170      |
| 3      | 200    | 205        | 210      |
| 4      | 140    | 145        | 145      |
| 5      | 185    | 190        | 195      |
| 6      | 175    | 180        | 185      |
| 7      | 155    | 160        | 165      |
| 8      | 205    | 210        | 215      |
| 9      | 165    | 165        | 170      |
| 10     | 190    | 195        | 200      |
| 11     | 150    | 155        | 160      |
| 12     | 170    | 175        | 180      |

### Minitab Steps
1. Stat → Nonparametrics → Friedman
2. Select "Response" = the three columns (or stacked format)
3. Treatment = Condition (Normal / Music / Caffeine)
4. Block = Lifter
5. Click OK

### Example Minitab Output (simulated)
Friedman Test: Response versus Treatment, Lifter
S = 19.50  DF = 2  P-Value = 0.000
Median   Sum of Ranks
Normal      170.0        15.0
Hype Music  175.0        24.0
Caffeine    180.0        33.0
Grand median = 175.0


### Conclusion
There is a **statistically significant difference** (p < 0.001) in 1RM squat performance between the three conditions. Caffeine produced the highest median lift, followed by hype music, then normal conditions.

Post-hoc pairwise comparisons (Wilcoxon signed-rank with Bonferroni correction) can be done to see exactly which pairs differ.

