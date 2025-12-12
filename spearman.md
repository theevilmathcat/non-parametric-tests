# Spearman Rank Correlation - Weightlifting Example (kg)

## Objective
Determine if there is a monotonic relationship between **training experience (years)** and **best back squat (kg)** in a group of weightlifters using **Spearman's rank correlation** (non-parametric).

## Data (Weightlifters.xlsx)
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