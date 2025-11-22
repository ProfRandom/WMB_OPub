---
Title: Ellipse Geometry Solver
tags:
  - math
  - meta
  - sanc
---
# 🧭 Ellipse Geometry Solver

This reference provides a complete algebraic toolkit for solving any ellipse — geometric or orbital — from any two independent parameters. All terms match the diagram above.  

## 📘 Glossary of Ellipse Parameters
  All variables match the labeled diagram above.

### 🔹 Core Axes & Foci
- **a** — semi-major axis  
- **b** — semi-minor axis  
- **c** — linear eccentricity (center to focus)  
- **e** — eccentricity (dimensionless) = $\dfrac{c}{a}$  
	  - Describes how "stretched" the ellipse is.  
		  - $e = 0$ → perfect circle  
		  - $0 < e < 1$ → ellipse  
		  - $e = 1$ → parabola (degenerate case)  
		  - $e > 1$ → hyperbola (not an ellipse)  
	- Eccentricity is **unitless** and invariant under scale.  
	-  It also defines the ellipse as a conic:

$$
e =  \dfrac{\text{distance to focus}}{\text{distance to directrix}}
$$
- **f** — flattening $b = 1 - \dfrac{b}{a}$  
- **i** — major axis $=2a$  
- **j** — minor axis $=2b$  
- **P, A** — primary vertices
- **X, Y** — co-vertices (±b along minor axis)  
- **C** — center of ellipse  
- **f₁, f₂** — the two foci  

### 🔹 Derived Lengths  
- **d** — focus-maximus = vertex to opposite focus $= a + c$  
- **g** — focus-minimus = focus to nearest vertex  $= a - c$ (e.g. $f_1P$)  
- **h** — focal span $=2c$  
- **ℓ** — semi-latus rectum $=\dfrac{1}{2} q$  
- **q** — latus rectum $= 2ℓ$

### 🔹 Directrix System  
- **m** — center-to-directrix $=\dfrac{a}{e}$  
- **n** — focus-to-directrix $=m - c$
- **s** — vertex-to-directrix $=m - a = \dfrac{c}{e} - a$  

## 🧮 Canonical Equations

### 🔹 Geometric
- $c = ae$  
- $b = a\sqrt{1 - e^2}$
- $a = \sqrt{b^2 + c^2}$

### 🔹 Orbital Geometry
- $f = a(1 - e^2) = \dfrac{b^2}{a}$  
- $r(\theta) = \dfrac{a(1 - e^2)}{1 + e \cos \theta}$  
- $r_p = a(1 - e)$ 

### 🔹 Directrix Relationships
- $m = \dfrac{a}{e}$  
- $s = m - a = \dfrac{c}{e} - a$  
- $n = m - c = \dfrac{a}{e} - c$

## 📐 What Is the Directrix?
For an ellipse, the **directrix** is:

> A fixed vertical line such that, for any point PPP on the ellipse,  
> the ratio of the distance from PPP to a **focus** and the distance from PPP to the **directrix** is equal to the **eccentricity** eee.

Formally:
$$\dfrac{\text{distance to focus}}{\text{distance to directrix}} = e$$
*This defines the ellipse!*
## 📏 Where Is the Directrix?

There are **two directrices**, one on each side of the center, at a distance:
$$m = \dfrac{a}{e}$$
… from the center, where:
- *a* is the semi-major axis
- *e* is the eccentricity    

So:
- Right-side directrix: $x = \dfrac{a}{e}$
- Left-side directrix: $x = -\dfrac{a}{e}$​
    If *e* → 0, the directrix moves off to infinity — which makes sense, because a circle (eccentricity 0) has no directrix-like behavior.

## 🎯 How the Directrix Relates to the Ellipse
You can think of the ellipse as a **set of points** where:
$$\dfrac{PF}{PD} = e$$
Where:
- PF is the distance from a point P on the ellipse to a **focus**
- PD is the distance from that same point P to the **directrix**   

This definition is symmetric and constructive: it's how conics are *defined* in classic geometry.

## 💡 So What Does It *Do*?
The directrix is mostly a **definitional and constructional tool** — not something we see in physical orbits, but:
- It gives us a clean formula for an ellipse in Cartesian coordinates:
$$r(\theta) = \dfrac{p}{1 + e \cos \theta} \quad \text{where } p = \dfrac{b^2}{a}$$
- It shows up in **ray-tracing**, **parabolic reflectors**, **classical mechanics**, and **procedural shape generation**.

## 🔍 Quick Facts
- Directrix location: $x= \pm \dfrac{a}{e}$
- Distance center to directrix: $m = \dfrac{a}{e}$
- Distance vertex to directrix: $s = m - a = \dfrac{c}{e}-a$
- Distance focus to directrix: $n = m - c = \dfrac{a}{e} - c$
- Eccentricity via directrix: $e = \dfrac{PF}{PD}$​

A reference sheet of exponent and logarithm rules useful in constructing systems of thermal, gravitational, orbital, and energetic relationships in scientifically-grounded worldbuilding.

