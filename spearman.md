# Spearman Rank Correlation - Weightlifting Example (kg)

## Objective
Determine if there is a monotonic relationship between **training experience (years)** and **best back squat (kg)** in a group of weightlifters using **Spearman's rank correlation** (non-parametric).

## Data
| Lifter | Years Training | Back Squat (kg) |
|--------|----------------|-----------------|
| A      | 1              | 100             |
| B      | 2              | 135             |
| C      | 3              | 140             |
| D      | 4              | 170             |
| E      | 5              | 165             |
| F      | 6              | 190             |
| G      | 8              | 205             |
| H      | 10             | 220             |

## Minitab Steps (Minitab 21 or newer)
1. Open the data in Minitab  
2. Go to **Stat** → **Basic Statistics** → **Correlation**  
3. Select **Years Training** and **Back Squat (kg)**  
4. Under **Method**, choose **Spearman rank correlation**  
5. Click **OK**

## Minitab Output
Spearman rank correlation
Years Training and Back Squat (kg)
N = 8   Missing = 0
Rho = 0.976   P-Value = 0.000

## Spearman Correlation Strength - Decision Rule

| Absolute Value of ρ (Spearman) | Strength of Relationship          |
|-------------------------------|-----------------------------------|
| 0.00 – 0.19                   | Very weak                         |
| 0.20 – 0.39                   | Weak                              |
| 0.40 – 0.59                   | Moderate                          |
| 0.60 – 0.79                   | Strong                            |
| 0.80 – 1.00                   | Very strong                       |

### Applied to our example
ρ = 0.976 → **Very strong** positive monotonic relationship

## Interpretation
- **Spearman ρ = 0.976** → Very strong positive monotonic relationship  
- **P-value = 0.000** → Statistically significant (p < 0.05)  

**Conclusion**: As training experience increases, back squat strength (in kg) almost always increases. The relationship is very strong and highly significant.

## About the monotonic concept. What does "monotonic" mean?

**Monotonic relationship** = As one variable increases, the other variable either:  
- **Consistently goes up** (monotonic increasing) → positive Spearman ρ  
- **Consistently goes down** (monotonic decreasing) → negative Spearman ρ  

It does **not** have to be a perfectly straight line (that would be Pearson/linear).  
It just has to generally trend in one direction without reversing.

### In our weightlifting example
- More years of training → back squat (kg) almost always gets higher  
- No one with 10 years trains less than someone with 2 years  
→ This is a **monotonic increasing** relationship  
→ Perfect for Spearman (we don’t care if the increases are 10 kg or 50 kg each time, only the direction)


That’s why we got ρ = 0.976 and call it a **very strong positive monotonic relationship**.

### Now since you are likely in college they are gonna ask you to calculate this by hand. The madness, no worries bruh, i got ya'.

## How to Calculate Spearman’s Rank Correlation by Hand (Step-by-Step)

Here’s the complete manual calculation for this example:

### Step 1: Assign ranks to each variable
Rank the values from lowest to highest (rank 1 = smallest).  
If there are ties, average the ranks.

| Lifter | Years Training | Rank (Years) | Back Squat (kg) | Rank (Squat) |
|--------|----------------|--------------|-----------------|--------------|
| A      | 1              | 1            | 100             | 1            |
| B      | 2              | 2            | 135             | 2            |
| C      | 3              | 3            | 140             | 3            |
| D      | 4              | 4            | 170             | 5            |
| E      | 5              | 5            | 165             | 4            |
| F      | 6              | 6            | 190             | 6            |
| G      | 8              | 7            | 205             | 7            |
| H      | 10             | 8            | 220             | 8            |

(No ties in this dataset)

### Step 2: Calculate the difference in ranks (d) for each lifter and square it (d²)

| Lifter | Rank (Years) | Rank (Squat) | d = Rank_Years − Rank_Squat | d²   |
|--------|--------------|--------------|-----------------------------|------|
| A      | 1            | 1            | 0                           | 0    |
| B      | 2            | 2            | 0                           | 0    |
| C      | 3            | 3            | 0                           | 0    |
| D      | 4            | 5            | -1                          | 1    |
| E      | 5            | 4            | +1                          | 1    |
| F      | 6            | 6            | 0                           | 0    |
| G      | 7            | 7            | 0                           | 0    |
| H      | 8            | 8            | 0                           | 0    |
| **Σd²** |              |              |                             | **2**    |

### Step 3: Apply the Spearman formula
When there are **no tied ranks** (as in this case), the formula simplifies to:

$$
\rho = 1 - \frac{6 \times \sum d^2}{n(n^2 - 1)}
$$

Where:
- n = number of observations = 8
- Σd² = 2

Plug in the numbers:

$$
\rho = 1 - \frac{6 \times 2}{8(8^2 - 1)} = 1 - \frac{12}{8 \times 63} = 1 - \frac{12}{504} = 1 - 0.02381 = 0.97619
$$

→ **ρ ≈ 0.976** (matches Minitab exactly)

### Quick notes
- The factor of 6 in the formula comes from the mathematical derivation of rank correlation.
- If there are ties, you must use the full formula involving sums of cubed rank differences, or use statistical software (which is why most people prefer software when ties exist).
