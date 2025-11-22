---
title: General Use Equations
tags:
  - math
---
# 🧮 General-Use Equations

### 📘 Variable Definitions
- **u** = upper bound  
- **l** = lower bound  
- **s** = sum of bounds (total)  
- **d** = difference between bounds (span)  
- **r** = ratio of lower to upper bound  
- **m** = mean (average)  
- **p** = product of bounds  
- **q** = quotient of bounds  

## 📏 Number Relationships

### ➗ Ratio
$$
\text{ratio} = \frac{l}{u} = \frac{\text{sum} - \text{difference}}{\text{sum} + \text{difference}}
$$
### ➕ Sum & Difference Identities
$$
\text{sum} = u + l = d\left(1 + \frac{1}{r}\right), \qquad
\text{difference} = u - l = s\left(\frac{1 - r}{1 + r}\right)
$$
### 🔀 Transformations Between Bounds
$$
l = \frac{s - d}{2}, \qquad
u = \frac{s + d}{2}, \qquad
s = l + u, \qquad
d = u - l
$$
### 🔁 Alternate Forms with Ratio
$$
l = \frac{s}{1 + r}, \qquad
u = \frac{rs}{1 + r}
l = s \cdot \left(\frac{1}{1 + r}\right), \qquad
u = s \cdot \left(\frac{r}{1 + r}\right)
l = \frac{s - d}{2}, \qquad
u = \frac{s + d}{2}, \qquad
l = \frac{(s - d) \cdot r}{1 + r}, \qquad
u = \frac{s \cdot r + d}{1 + r}
$$
### 📊 Mean
$$
m = \frac{u + l}{2}, \qquad
m = \frac{s}{2}, \qquad
m = u - \frac{d}{2}, \qquad
m = l + \frac{d}{2}
$$
### 🧮 Inequality Notes
$$
m \gg \frac{1}{2} u \quad \text{(if } u < 0 \text{ and } l > 0\text{)}
m = \frac{1}{2} u \quad \text{(if } l = 0\text{)}
m = u = l \quad \text{(if } u = l\text{)}
$$
### ✖️ Product & Quotient
$$
\text{Product } = xy = \frac{s^2 - d^2}{4}
\text{Quotient } = \frac{x + d}{x - d} = \frac{(x + y) + (x - y)}{(x + y) - (x - y)}
\frac{s}{d} = \frac{x + y}{x - y}, \qquad \frac{d}{s} = \frac{x - y}{x + y}
$$
## 📉 Percentage from Portion

### 🔢 Percentage (p) from portion (x) of total  (n)

$$
p = \frac{x}{n}, \qquad x = pn, \qquad n = \frac{p}{x}
$$
### 📘 Definitions
- **p** = percentage  
- **x** = portion (part)  
- **n** = base number (whole)

## 🎯 Percentages in Ranges

### 📐 Percentage (p) Represented by a Value (v) in Range (l … u)
$$
p = \frac{v - l}{u - l}, \qquad v = p(u - l) + l, \qquad u = \frac{v - l}{p} + l, \qquad l = \frac{v - pu}{1 - p}
$$
#### 🔤 Variable Definitions
- **v** = value within the range  
- **l** = lower bound  
- **u** = upper bound  
- **p** = percentage of the \([l, u]\) range represented by \(v\)

### 🔁 Transfer a Percentage Between Two Ranges
#### 🧮 General Equations
Let:
- $R_1 = [\text{min}, \text{num}, \text{max}]$
- $R_2 = [z, x, y]$, where $x < z < y$

Then:

$$
\text{pct} = \frac{\text{num} - \text{min}}{\text{max} - \text{min}}, \qquad
z = \text{pct} \cdot (y - x) + x
$$
#### ✅ Example
Given:
- $R_1 = [0, 6, 10]$
- $R_2 = [4, z, 6]$

Then:

$$
\text{pct} = \frac{6 - 0}{10 - 0} = \frac{6}{10} = 0.60
z = 0.60 \cdot (6 - 4) + 4 = 0.60(2) + 4 = 5.2
$$

Check:

$$
\frac{5.2 - 4}{6 - 4} = \frac{1.2}{2} = 0.60
$$
## 🔢 Sums of Number Sequences

### 📘 Variable Definitions
- **Σ** = sum of all integers in the range (l … u)  
- **s** = sum of bounds: $u + l$  
- **d** = difference: $u - l$  
- **l** = lower bound of range  
- **u** = upper bound of range  

### ➕ Consecutive Integers from (l …  u)
$$
s = u + l, \qquad d = u - l
$$
#### 🧮 Summation Formulas
Basic:

$$
\Sigma = \frac{u(u + 1)}{2} - \frac{l(l - 1)}{2}
$$

Symmetric:

$$
\Sigma = \frac{l^2 - 1}{2} + \frac{u^2 + u}{2}, \qquad
\Sigma = \frac{(u + l)(u - l + 1)}{2}
$$

Sum in terms of $d$ and $s$:

$$
\Sigma = \frac{d + 1}{2} s, \qquad
\Sigma = \frac{sd + s}{2}
$$

Expanded forms:

$$
\Sigma = \frac{u^2 + u}{2} - \frac{l^2 - l}{2}
\Sigma = \frac{(u^2 + u) - (l^2 - l)}{2}, \qquad
\Sigma = \frac{u^2 - l^2 + u + l}{2}, \qquad
\Sigma = \frac{u^2 - l^2 + s}{2}
$$
## 🔢 Integer Sequences and Special Transformations

### 🟥 Consecutive Odd Integers (1 … u)
$$
\Sigma_o = \left( \frac{u + 1}{2} \right)^2 = \frac{u^2 + 2u + 1}{4}
$$
### 🟦 Consecutive Even Integers (2 … u)
$$
\Sigma_e = \left( \frac{u}{2} \right) \left( \frac{u}{2} + 1 \right) = \frac{u(u + 2)}{4} = \frac{u^2 + 2u}{4}
$$
### 🧮 Count of Consecutive Integers in Range (1 … u)
$$
\left\lfloor \frac{u - l}{2} \right\rfloor + 1 \quad \text{for odd or even spacing}
$$
 — or for total count of integers:

$$
\left\lfloor \frac{u - l}{2} \right\rfloor \cdot 2 + 1 = 2\left\lfloor \frac{u - l}{2} \right\rfloor + 1
$$
### 📉 Percent Difference

$$
\%\Delta = 100 \cdot \frac{\text{new} - \text{old}}{\text{old}} = 100 \left( \frac{\text{new}}{\text{old}} - 1 \right)
$$
### 🔁 Involutive Transformation
Given:

$$
y = \frac{1 - x}{1 + x}
$$
Then:

$$
x = \frac{1 - y}{1 + y}
$$

This is its own inverse: $f(f(x)) = x$

### 🔄 Percentage Inversion (Reciprocal Percentages)
If $x\% \text{ of } y = y\% \text{ of } x$, then:

$$
\frac{x}{100} \cdot y = \frac{y}{100} \cdot x, \qquad
x \cdot \frac{y}{100} = y \cdot \frac{x}{100}
$$
## 🟨 Generalized Metallic Mean for Any Integer $x$
The traditional formula is:

$$
N_x = \frac{x + \sqrt{x^2 + 4}}{2}
$$

This generalizes the golden ratio (\(x = 1\)), silver ratio (\(x = 2\)), bronze ratio (\(x = 3\)), etc.

Alternative equivalent form:

$$
N_x = \sqrt{1 + \frac{x^2}{4}} + \frac{x}{2}
$$

This version is symmetric and may be more intuitive in nested radical systems.

