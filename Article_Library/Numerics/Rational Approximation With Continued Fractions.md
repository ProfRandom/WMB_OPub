---
title: Rational Approximation With Continued Fractions
tags:
  - math
concepts: Continued Fraction, Rational Approximation, Convergents
---
# Rational Approximation (Continued Fractions)
```latex
$$
x = a_0 + 1/(a_1 + 1/(a_2 + 1/(a_3 + \dots)))
$$
```

$$
x = a_0 + 1/(a_1 + 1/(a_2 + 1/(a_3 + \dots)))
$$

```latex

$$
x = a_0 + \cfrac{1}{a_1 + \cfrac{1}{a_2 + \cfrac{1}{a_3 + \cdots}}}
$$
```
$$
x = a_0 + \cfrac{1}{a_1 + \cfrac{1}{a_2 + \cfrac{1}{a_3 + \cdots}}}
$$
```latex
$$
x = 1 + \cfrac{1}{2 + \cfrac{1}{2 + \cfrac{1}{2 + \ddots}}}
$$
```
$$x = 1 + \cfrac{1}{2 + \cfrac{1}{2 + \cfrac{1}{2 + \ddots}}}$$
## Step 1 — Define the goal

Given a real number $x$, find a fraction $\dfrac{p}{q}$ that’s as close as possible while keeping $q$ below some limit, $Q_{max}$.

$$
\text{minimize}\;\left|x-\frac{p}{q}\right|, \quad q \le Q_{max}
$$

## Step 2 — Start the continued-fraction expansion
Begin:

$$
\begin{array}{ll}
x_0 = x, & a_0 = \lfloor x_0 \rfloor
\end{array}
$$

Iterate:

$$
\begin{array}{ll}
x_{n + 1} = \dfrac{1}{x_n - a_n}, & a_{n + 1} = \lfloor x_{n + 1} \rfloor
\end{array}
$$
> In each iteration, replace $a_n$ with the value of $a_{n+1}$ from the previous iteration.

Record each $a_n$: the sequence $a_0, a_1, a_2,\ldots$ forms the **continued-fraction coefficients** of $x$.

$$
x = \mathbf{a_0} + \cfrac{1}{\mathbf{a_1} + \cfrac{1}{\mathbf{a_2} + \cfrac{1}{\mathbf{a_3} + \cdots}}}
$$

Thus, the number $x$ can be written as:

$$
x = [a_0; a_1, a_2, a_3, \ldots]
$$
Where:
- $a_0$ = the integer portion of $x$ (if any)
- $a_1, a_2, a_3, \ldots$ = the sequence of $a_n$ recorded above.

## Step 3  — Build convergents
Initialize:

$$
\begin{array}{lll}
p_{n-2} = 0, &p_{n-1} = 1, \\[0.5em]
q_{n-2} = 1, &q_{n-1} = 0 \\[0.5em]
n = 1
\end{array}
$$

Calculate:

$$
\begin{array}{lll}
&p_n = a_n\,p_{n-1} + p_{n-2}, \\[0.5em]
&q_n = a_n\,q_{n-1} + q_{n-2} \\[0.5em]
\text{Test:} &y_n = \dfrac{p_n}{q_n}, \\[0.5em]
\text{If:} &y_n \not\approx x, \\[0.5em]
\text{Increment n:} &n = n + 1 \\[0.5em]
\text{Continue until:} &|x - y_n| \quad\text{is within the desired tolerance}
\end{array}
$$

