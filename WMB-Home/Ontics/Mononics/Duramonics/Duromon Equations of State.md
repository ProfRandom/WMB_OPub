---
project: wmb
phase: 1
module: 1
status: draft
created: 2025-11-28
updated: 2025-11-28
summary: ""
---
 

# Duromon Equations of State

The Duromon Equations of State can be arranged into a fully symmetric algebraic network: any two parameters determine the other three. This is mathematically true and occasionally useful — especially for inversion problems or exotic boundary cases.

However, **physical causality is not symmetric**.

WMB treats duromonic properties as a *directed hierarchy* with a strict upstream–downstream dependency:

### 1. Primaries → define the Consequent

$$
(\rho,\, m) \;\Rightarrow\; r
$$

### 2. Primaries + Consequent → define the Subsequent

$$
(m,\, r) \;\Rightarrow\; g
$$

### 3. Consequent + Subsequent → define the Emergent

$$
(r,\, g) \;\Rightarrow\; v_e
$$

This isn’t merely a teaching preference — it reflects how planetary bodies actually *are*.  
Mass and density establish the size of a body; size and mass fix its gravity; gravity and size together determine the depth of its gravitational well.

### Therefore:
Even though $v_e$ *can* be expressed directly from $(m,\rho)$, WMB **strongly discourages** using collapsed formulas except for analytic or diagnostic work.

A shortcut like:

$$
(m,\rho) \rightarrow v_e
$$

— short-circuits the physical logic, obscures the dependency chain, and creates the illusion that escape velocity is an independently tunable parameter. It is not.

Thus, while the full symmetric table of identities is correct and useful as a reference, the **recommended workflow** for all duromonic modeling is:

$$
\begin{aligned}
(\rho,\; m) \Rightarrow\; &r, \\[1ex]
\quad (m,\; &r) \Rightarrow g, \\[1ex]
 &\hspace{.8em}(r,\; g) \Rightarrow v_e
\end{aligned}
\tag{1}
$$

#### Full Equation Set


$$
\begin{array}{c|c|c|c|c}
\text{Mass }(m) & \text{Radius }(r) & \text{Density }(\rho) & \text{Gravity }(g) & \text{Escape Velocity }(v_e)\\[0.5em]
\hline
m = g r^2 & r = \dfrac{g}{\rho} & \rho = \dfrac{m}{r^3} & g = \dfrac{m}{r^2} & v_e = \sqrt{g r}\\
m = \rho r^3 & r = \sqrt{\dfrac{m}{g}} & \rho = \dfrac{g}{r} & g = r\rho & v_e = \sqrt{\dfrac{m}{r}}\\
m = \dfrac{g^3}{\rho^2} & r = \sqrt[3]{\dfrac{m}{\rho}} & \rho = \sqrt{\dfrac{g^3}{m}} & g = \sqrt[3]{m\rho^2} & v_e = \dfrac{g}{\sqrt{\rho}}\\
m = \dfrac{v_e^3}{\sqrt{\rho}} & r = \dfrac{v_e}{\sqrt{\rho}} & \rho = \left(\dfrac{v_e}{r}\right)^2 & g = v_e\sqrt{\rho} & v_e = \sqrt[4]{m g}\\
m = \dfrac{v_e^4}{g} & r = \dfrac{v_e^2}{g} & \rho = \left(\dfrac{g}{v_e}\right)^2 & g = \dfrac{v_e^2}{r} & v_e = r\sqrt{\rho}\\
m = r v_e^2 & r = \dfrac{m}{v_e^2} & \rho = \left(\dfrac{v_e^3}{m}\right)^2 & g = \dfrac{v_e^4}{m} & v_e = \sqrt[6]{m^2\rho}
\end{array}
$$


**Note:**  
Every formula in the table is algebraically valid, but WMB assumes and teaches the causal chain as shown above in Equation Set 1.

Use the symmetric identities when necessary, but rely on the causal hierarchy for constructive worldbuilding.

Duromon equations conventionally use **lower-case variables** ($m$, $\rho$, $r$, $g$, $v_e$) to emphasize their domain: compact, high-density bodies whose structure is governed primarily by internal material constraints rather than stellar-scale energy processes. This contrasts with the **stellamon state equations**, which employ **upper-case forms**($M$, $R$, $T$, $K$, $Q$, $L$) to distinguish the vastly different regimes of mass, scale, and pressure involved.

The capitalization isn’t aesthetic — it’s categorical. Lower-case identifies matter-bound, mechanically dominated bodies; upper-case flags fusion-driven, radiative systems. Mixing conventions would produce mathematical ambiguity and, worse, physical nonsense. So the typographic divide holds firm: **duromon, transomon** → lower-case, **fusomon, peromon** → upper-case.
