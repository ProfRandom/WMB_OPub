---
title: Duramon Ground States
tags:
  - planemon
  - gravity
  - surface_gravity
  - escape_velocity
  - mass
  - density
date: 2025-11-20
---
# Duramon Ground States
When any single duramon parameter is normalized to $1$, the remaining variables collapse into simple power-law relationships. These “ground states” reveal the symmetry structure of the duramon system: which quantities scale together, which invert each other, and which collapse into equality under specific constraints. Each case below assumes one core variable is set to unity and derives the resulting canonical forms for the others.

> **Note**: If **any two** core parameters equal $1$ simultaneously, then **all** five must equal $1$.
>
> Because each variable is a direct power of the others, fixing **two** independent quantities to unity collapses all exponents, forcing the entire system into its fully normalized state:
> 
> 	$(m, r, \rho, g, v_e) = (1, 1, 1, 1, 1)$

Each block below lists the simplified relationships among the remaining parameters when one is set to $1$.  

**To calculate a specific value, just locate the line beginning with the variable you want to compute.**
## Mass: $m = 1$

$$
\begin{aligned}
r &=\sqrt{\dfrac{1}{g}}=\sqrt[3]{\dfrac{1}{\rho}}=\dfrac{1}{v_e^2}
\\[0.5ex]
\rho &=\dfrac{1}{r^3}=\sqrt{g^3}=v_e^6 \\[0.5ex]
g &=\dfrac{1}{r^2}=\sqrt[3]{\rho^2}=v_e^4 \\[0.5ex]
v_e &=\sqrt{\dfrac{1}{r}}=\sqrt[4]{g}=\sqrt[6]{\rho}
\end{aligned}
$$


## Density: $\rho = 1$

$$
\begin{aligned}
r &= g = v_e = \sqrt[3]{m} \\[0.5ex]
m &=r^3=g^3=v_e^3 \\[0.5ex]
g &=r=\sqrt[3]{m}=v_e \\[0.5ex]
v_e &=g=r=\sqrt[3]{m}
\end{aligned}
$$

> > **Note**: When **ρ = 1**, the values of **radius** (*r*), **gravity** (*g*), and **escape velocity** (*vₑ*) are all numerically equal. The **mass** (*m​*) is the cube of any of them.



## Gravity: $g = 1$

$$\begin{aligned}
m &=r^2=\dfrac{1}{\rho^2}=v_e^4 \\[0.5ex]
r &=\dfrac{1}{\rho}=\sqrt{m}=v_e^2 \\[0.5ex]
\rho &=\dfrac{1}{r}=\sqrt{\dfrac{1}{m}}=\dfrac{1}{v_e^2} \\[0.5ex]
v_e &=\sqrt{r}=\dfrac{1}{\sqrt{\rho}}=\sqrt[4]{m}
\end{aligned}
$$


## Escape Velocity: $v_e = 1$

$$
\begin{aligned}
m &=\dfrac{1}{\sqrt{\rho}}=\dfrac{1}{g}=r \\[0.5ex]
r &=\dfrac{v_e}{\sqrt{\rho}}=\dfrac{1}{g}=m \\[0.5ex]
\rho &=\dfrac{1}{r^2}=g^2=\dfrac{1}{m^2} \\[0.5ex]
g &=\sqrt{\rho}=\dfrac{1}{r}=\dfrac{1}{m}
\end{aligned}
$$


## Radius: $r = 1$

$$
\begin{aligned}
m &=g=\rho=v_e^2 \\[0.5ex]
v_e &=\sqrt{g}=\sqrt{\rho}=\sqrt{m}
\end{aligned}
$$

> > **Note**: When $r = 1$, the values of **mass** ($m$), **gravity** ($g$), and **density** ($\rho$) are all numerically equal. The **escape velocity** ($v_e$) is the square-root of any of them.