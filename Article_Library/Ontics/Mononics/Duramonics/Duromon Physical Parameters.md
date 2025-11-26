---
title: Duromon Physical Parameters
tags:
  - duromon
  - parameter
  - mass
  - radius
  - escape_velocity
  - density
  - gravity
  - surface_gravity
date: 2025-11-20
---
# Duromon Physical Parameters

m := (0.000001 ·· 4131.4)⨁ 
ρ := (0.0272 ·· 2.18)⨁ 
r := (0.0078 ·· 11.2)⨁
g := (0.0019 ·· 26.95)⨁ 
vₑ := (0.01145 ·· 17.37)⨁

$$
\text{DUROMON} := \left\{
\begin{aligned}
	&0.000001 ≤ m ≤ 4131.4 \\
	&0.0272 ≤ \rho ≤ 2.18 \\
	&0.0078 ≤ r(m, \rho) ≤ 11.2 \\
	&0.0019 ≤ g(m, r) ≤ 26.95 \\
	&0.0115 ≤ v_e(g, r) ≤ 17.37
\end{aligned}
\right.
$$
> **Note**: These bounds represent the physically realizable envelope for matter-regime worlds (duromons). Worlds below this space fall into synomonic behavior; above it, into transomonic or fusomonic physics.

Duromons are matter-regime monons — bodies whose structure is dominated by classical matter physics and gravitational cohesion, spanning micromons through planemons to the upper limits of pre-degeneracy worlds.

Duromonic parameters are grouped into tiers not by convenience, but by causality: primaries _define_ the consequents, and together they _generate_ the emergent.
## Primary Properties

**Mass** ($m$):  
The total amount of matter the duromon contains.  
*Mass is invariant* — it does not change with location or gravity.  
> *Mass and weight are not the same: weight depends on gravity, but mass does not.*

**Density** ($ρ$):  
The average amount of matter per unit volume — how tightly the duromon’s material is packed. Density depends on both composition (rock, ice, metal, etc.) and, for larger bodies, gravitational self-compression.
## The Consequent

**Radius** ($r$):  
The distance from the duromon’s center to its surface.  
Radius is also **consequent**, also arising from the interaction of mass and density:

$$
r = \sqrt[3]{\frac{m}{ρ}}
$$

## The Subsequent

**Surface Gravity** ($g$):  
The strength of gravitational acceleration at the duromon’s surface — how strongly it attracts objects located one radius away from its center.  

Gravity is **subsequent**, arising from the interaction of mass and radius:

$$
g = \frac{m}{r^2}
$$

Together, mass and density _produce_ the duromon’s consequent parameters.

They describe what the body *is* and how it *acts* gravitationally.
## The Emergent

**Escape Velocity** ($v_e$):  
The minimum speed required to escape the duromon’s gravitational field when starting from its surface.

This property emerges from the consequents:

$$
v_e = \sqrt{g\, r}
$$
Escape velocity represents the energy threshold imposed by the duromon’s gravitational well — the “height” of its gravity.
## Hierarchy of Dependence

Duromonic properties follow a clear causal chain, in which the **primary** properties ($m, \rho$) *define* the **consequent** properties ($g, r$), and together these *form* the **emergent** property ($v_e$):

![[Duromonic Physical Properties]]

$$
\begin{aligned}
(\rho,\; m) \Rightarrow\; &r, \\[1ex]
\quad (m,\; &r) \Rightarrow g, \\[1ex]
 &\hspace{.8em}(r,\; g) \Rightarrow v_e
\end{aligned}
$$

Together these five parameters define the **duromonic phase space**: the region of physical possibility for matter-regime monons.

# A Familiar Analogy

The classic riddle “Which is heavier — a pound of iron or a pound of feathers?” demonstrates the independence of *mass* from *density*.  

Both *weigh* the same, but the feathers occupy far more *volume* because they are less dense.  

The same principle applies on planetary scales: a rocky duromon and an icy duromon of equal mass can differ greatly in radius, surface gravity, and escape velocity.
