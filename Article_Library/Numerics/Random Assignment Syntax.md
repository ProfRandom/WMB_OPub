---
title: Random Assignment Syntax
tags:
  - approx
  - math
concepts: Random, Random Numbers, Syntax, Precision
---
## 🎲 Random Assignment Syntax

Random assignment uses the **range connective** from the WMB inequality system, bracketed in angle brackets:

| Expression     | Meaning                                              |
| -------------- | ---------------------------------------------------- |
| ⟨a ≤ x; x ≤ b⟩ | Assign random value from a to b (inclusive)          |
| ⟨x < a; x > b⟩ | Must assign value outside strict range               |
| ⟨a ≤ x; x < b⟩ | Assign value in left-inclusive, right-excluded range |

**Mandation and prescription operators do not apply here;** random assignment uses strict (`<`) and inclusive (`≤`) ranges only.

## 🎲 Random Assignment Syntax With Weighting

$$
x = a + (b - a)\,\langle 0 ≤ x;\;x ≤ 1 \rangle^{p}
$$

Where:
- $a$ = low end of the random range  
- $b$ = high end of the random range  
- $p$ = weighting exponent  
    - $p > 1$: weights the randomization toward $b$  
    - $0 < p < 1$: weights the randomization toward $a$  
    - $p = 1$: produces a uniform (unbiased) distribution  
    - $p \neq 0$: undefined at zero  

> Because $\langle 0 < x; x < 1 \rangle$ represents a continuous uniform variable, and because the exponent $p \in (0, \infty)$ continuously reshapes that distribution, the **biasing space** is symmetric about $p = 1$: bias toward *a* for $0 < p < 1$, bias toward *b* for $p > 1$.

