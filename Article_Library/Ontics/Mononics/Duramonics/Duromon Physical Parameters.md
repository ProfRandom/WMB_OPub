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

Duromons are matter-regime monons — bodies whose structure is governed by classical matter physics and gravitational cohesion. This continuum spans micromons through planemons, reaching up to the upper limits of pre-degenerate worlds.

Duromonic parameters are grouped into tiers not by convenience, but by causality: the primaries define the consequents, and together they generate the emergent.
## Primary Properties

**Mass** ($m$):  
The total amount of matter the duromon contains.  
*Mass is invariant* — it does not depend on environment, location, or gravity.  
> *Mass and weight are not the same: weight depends on gravity; mass does not.*

**Density** ($ρ$):  
The average mass per unit volume — how tightly the duromon’s material is packed.  
Density reflects both **composition** (rock, ice, metal) and, for larger worlds, **gravitational self-compression**.

These **two** values form the foundational descriptors of every duromon.
## The Consequent

**Radius** ($r$):  
The distance from the duromon’s center to its surface.  
Radius is **consequent** — it _arises solely_ from mass and density:

$$
r = \sqrt[3]{\frac{m}{ρ}}
$$

## The Subsequent

**Surface Gravity** ($g$):  
The strength of gravitational acceleration at the duromon’s surface — how strongly it attracts objects located one radius away from its center.  

Gravity is **subsequent**, derived from mass and radius:

$$
g = \frac{m}{r^2}
$$

Once mass and density are fixed, gravity is fixed.  It cannot vary independently.
## The Emergent

**Escape Velocity** ($v_e$):  
The minimum speed required to escape the duromon’s gravitational well, beginning at the surface.

Escape velocity is **emergent**, produced by the interaction of surface gravity and radius:

$$
v_e = \sqrt{g\, r}
$$
This describes the energetic “depth” of the gravity well — not a fundamental trait but the _final consequence_ of all upstream parameters.
## Hierarchy of Dependence

All duromonic physical parameters follow a strict causal chain:

![[Duromonic Physical Properties]]

$$
\begin{aligned}
(\rho,\; m) \Rightarrow\; &r, \\[1ex]
\quad (m,\; &r) \Rightarrow g, \\[1ex]
 &\hspace{.8em}(r,\; g) \Rightarrow v_e
\end{aligned}
$$

Together, these five properties carve out the **duromonic phase space**: the region of physical possibility for matter-regime monons.
# A Familiar Analogy
The classic riddle, “Which is heavier — a pound of iron or a pound of feathers?” illustrates the independence of **mass** from **density**.

Both weigh the same, but the feathers take up vastly more **volume** because they are less dense.

On planetary scales the same principle holds:
- Two duromons with equal **mass** can differ enormously in **radius**, **gravity**, and **escape velocity** if their **density** differs.    
- Change the primary parameters, and the entire structure of the world reshapes itself.
