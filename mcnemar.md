# McNemar Test – Weightlifting Example (Paired binary data)

## When do we use the McNemar test?
We use McNemar when we have:
- Paired nominal data (before/after or test/retest)
- Only two categories (Yes/No, Success/Failure)
- Same subjects measured twice

### Weightlifting Example
We asked 80 competitive lifters the same question before and after an 8-week training program:

“Could you squat ≥ 2 × bodyweight (≥2.0 strength ratio)?”

We want to know if the proportion of lifters who achieved this milestone changed significantly after the program.

### 2×2 Contingency Table (paired)

|                         | After: YES | After: NO |
|-------------------------|------------|-----------|
| **Before: YES**         | 25         | 5         |
| **Before: NO**          | 18         | 32        |

- 25 lifters could already do it before and still could after  
- 5 could do it before but could NOT after (got weaker or injured)  
- 18 could NOT before but could after (improved!)  
- 32 could not before and still could not

The McNemar test only looks at the **discordant pairs** (5 + 18 = 23 lifters who changed).

### Minitab Steps
1. Stat → Tables → Chi-Square → McNemar Test
2. Enter the 2×2 table (or use stacked data)
3. Click OK

### Example Minitab Output (simulated)
McNemar's Test
After YES   After NO
Before YES      25         5
Before NO       18        32
Chi-Square = 7.56   DF = 1   P-Value = 0.006
Exact P-Value = 0.008 (with continuity correction off)


### Conclusion
There is a **statistically significant improvement** (p = 0.006) in the proportion of lifters who can squat ≥2× bodyweight after the 8-week program.  
Specifically, 18 lifters gained the ability while only 5 lost it — a clear positive change.