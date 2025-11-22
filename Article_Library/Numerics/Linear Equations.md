---
title: Linear Equations
tags:
  - math
concepts: Point-Slope, Slope-Intercept,
---
## 📈 Point–Slope of a Line
Given two points:

$$
\begin{aligned}
P_1 = (x_1, y_1) \\[6pt]
P_2 = (x_2, y_2)
\end{aligned}
$$
### 🧮 Slope Formula
$$
m = \frac{y_1 - y_2}{x_1 - x_2}
$$
### 🧾 Point–Slope Form
$$
y - y_1 = m(x - x_1)
$$
Or rearranged:

$$
y = m(x - x_1) + y_1
$$
### 🎯 Slope–Intercept Form
$$
y = mx + b
$$
### 🔃 Converting from Point–Slope to Slope–Intercept
$$
\begin{aligned}
\text{Start with point–slope:} \quad & y - y_1 = m(x - x_1) \\[6pt]
\text{Distribute the slope:} \quad & y = mx - mx_1 + y_1 \\[6pt]
\text{Group constants:} \quad & y = mx + (y_1 - mx_1) \\[6pt]
\text{Therefore:} \quad & b = y_1 - mx_1
\end{aligned}
$$
> 🧠 **Note:** The subscripts vanish because their values get absorbed into the constant $b$.  
> The slope–intercept form still “remembers” your point — just more subtly.

## 🧪 Example 1
Given:  
- $P_1 = (4.85, 0)$  
- $P_2 = (1, 1)$

### Step 1: Find the slope
$$
m = \frac{0 - 1}{4.85 - 1} = \frac{-1}{3.85}
$$

### Step 2: Use point–slope form
$$
y - 0 = \frac{-1}{3.85}(x - 4.85)
$$

### Step 3: Rearrange to slope–intercept form
$$
y = \frac{-1}{3.85}x + \frac{4.85}{3.85} \approx -0.26x + 1.26
$$
## 🧪 Example 2
Given:  
- $P_1 = (0.5, 0)$  
- $P_2 = (1, 1)$

### Step 1: Find the slope
$$
m = \frac{0 - 1}{0.5 - 1} = \frac{-1}{-0.5} = 2
$$

### Step 2: Use point–slope form
$$
y - 0 = 2(x - 0.5)
$$

### Step 3: Rearrange to slope–intercept form
$$
y = 2x - 1
$$

## 📉 Visualizing Point–Slope Examples

This plot shows the two lines derived in the examples above:

- **Blue Line**:  
  From $P_1 = (4.85, 0)$ and $P_2 = (1, 1)$  
  $y = -0.25974x + 1.25974$

- **Red Line**:  
  From $P_1 = (0.5, 0)$ and $P_2 = (1, 1)$  
  $y = 2x - 1$

They intersect at the point (1, 1), which lies on both lines.

