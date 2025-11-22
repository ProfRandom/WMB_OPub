---
title: The Euclidean Algorithm
tags:
  - math
concepts: Least Common Multiple, Greatest Common Divisor, Remainder, Modulo Arithmatic
---
# The Euclidean Algorithm

The Euclidean Algorithm provides an elegant and efficient (if somewhat involved) way to compute the greatest common divisor (GCD) of two integers.  This is especially useful for simplifying ratios or finding integer relationships when work with synodic systems

## The Algorithm
The algorithm itself is deceptively short and simple:
1. Start with two integers $a$ and $b$, such that $a>b$.
2. Divide $a$ by $b$, and note the *remainder*, $r$.
	- $r = a\; MOD\; b$
3. Replace $a$ with $b$ and $b$ with $r$.
4. Repeat steps 2 - 3 until $f = 0$.

The last *non-zero remainder* is the greatest common divisor between $a$ and $b$.

### Example

$$
\begin{aligned}
a = 2436 \qquad b = 1172 \\
r = a\;mod\;b = 92 \\[1em]
a = 1172 \qquad b = 92 \\
r = a\;mod\;b = 68 \\[1em]
a = 92 \qquad b = 68 \\
r = a\;mod\;b = 24 \\[1em]
a = 68 \qquad b = 24 \\
r = a\;mod\;b = 20 \\[1em]
a = 24 \qquad b = 20 \\
r = a\;mod\;b = 4\; ✓ \\[1em]
a = 20 \qquad b = 4 \\
⟶ r = a\;mod\;b = 0 \\
\end{aligned}
$$

If you don't have a tool that directly calculates modulos, $r$ can manually be calculated by:

$$
r = a - \left( b \times \left\lfloor \dfrac{a}{b} \right\rfloor \right)
$$

Here is an admittedly clunky longhand version for clarity

$$
\begin{aligned}
2 &\quad (Quotient)\\[-0.2ex]
1172)\,\overline{2436} &\quad (Dividend)\\[-0.4ex]
\underline{-2344} &\quad (Subtracted: 2\times1172)\\[-0.3ex]
92 &\leftarrow (Remainder)
\end{aligned}
$$

$$
\begin{aligned}
12 &\quad (Quotient)\\[-0.2ex]
92)\,\overline{1172} &\quad (Dividend)\\[-0.4ex]
\underline{-1104} &\quad (Subtracted: 12\times92)\\[-0.3ex]
68 &\leftarrow (Remainder)
\end{aligned}
$$

$$
\begin{aligned}
1 &\quad (Quotient)\\[-0.2ex]
68)\,\overline{92} &\quad (Dividend)\\[-0.4ex]
\underline{-68} &\quad (Subtracted: 1\times68)\\[-0.3ex]
24 &\leftarrow (Remainder)
\end{aligned}
$$

$$
\begin{aligned}
2 &\quad (Quotient)\\[-0.2ex]
24)\,\overline{68} &\quad (Dividend)\\[-0.4ex]
\underline{-48} &\quad (Subtracted: 2\times24)\\[-0.3ex]
20 &\leftarrow (Remainder)
\end{aligned}
$$

$$
\begin{aligned}
1 &\quad (Quotient)\\[-0.2ex]
20)\,\overline{24} &\quad (Dividend)\\[-0.4ex]
\underline{-20} &\quad (Subtracted: 1\times20)\\[-0.3ex]
\mathbf{4} &\;\boldsymbol{\checkmark}\leftarrow (Remainder)
\end{aligned}
$$

$$
\begin{aligned}
5 &\quad (Quotient)\\[-0.2ex]
4)\,\overline{20} &\quad (Dividend)\\[-0.4ex]
\underline{-20} &\quad (Subtracted: 5\times4)\\[-0.3ex]
0 &\leftarrow (Remainder)
\end{aligned}
$$

$$
\text{Since this remainder is } 0, \text{ the previous remainder is the GCD:}\\[0.5ex]
\therefore\;\gcd(2436,1172)=4
$$

