---
project: wmb
phase: 1
module: 1
status: draft
created: <%* tp.file.creation_date("YYYY-MM-DD") %>
updated: <%tp.date.now("YYYY-MM-DD") %>
summary: ""
---
 

# Stellamon Parameters
A regularized set of empirical relationships can be used to estimate any stellar parameter from the others.

## Blackbody Radiation

A **blackbody** is an **idealized physical object** that:
1. **Absorbs all** incoming electromagnetic radiation — no reflection, no transmission.
2. **Emits radiation** purely based on its temperature — not its material, shape, or color.
3. Emits a **perfectly smooth, continuous spectrum** (a "thermal spectrum").

In short:
> A blackbody is the theoretical gold standard for radiant heat emission — a perfect radiator and absorber.

### Why "Blackbody" Matters Here

Most stars (especially Main Sequence stars) behave **approximately like blackbodies**, meaning their energy output can be modeled using **temperature alone**. This makes them excellent candidates for:
- **Temperature-based modeling**
- **Color-temperature mapping** (blue = hotter, red = cooler)
- **Spectrum-based classification** (like spectral classes O–M)
- Real-World Deviation
	- planemons, dust clouds, and even stars aren’t *perfect* blackbodies.
	- Real objects have an **emissivity** ϵ (0 ·· 1):

$$ F = \varepsilon \sigma T^4$$
- But stars are close enough that the **blackbody approximation works very well**.

## Equations of State

$$
\begin{array}{c|c|c|c}
\text{Temperature} &\text{Mass} &\text{Radius} &\text{Lifetime} \\[0.1em]
\text{(T)} &\text{(M)} &\text{(R)} & \text{($Q$)} \\[0.5em] 
\hline
T=\sqrt[1.98]{M} & M=\sqrt[0.9]{R} & R=M^{0.9} & Q=M^{-2.5} \\[0.5em]
T=\sqrt[1.8]{R} & M=T^{1.98} & R=T^{1.8} & Q \approx \sqrt[-0.36]{R} \\[0.5em]
T=Q^{-0.2} & M=Q^{-0.4} & R=Q^{-0.36} & Q=T^{-5}
\end{array}\tag{1}
$$
> > **NOTE**:
> > All of the above equations are *approximations*; stars are a much more variable set of objects (after all, they're mostly gas and plasma, so fluid dynamics plays a major role in their characteristics).  These equations work **best *in general* for main sequence stars** of all classes.

## The Luminosity Conundrum
### The Stefan-Boltzmann Law
The Stefan-Boltzmann Law is a formulation that relates the **luminosity** of any luminous object to its **temperature** and **surface area**:

$$
L = 4 \pi R^2 \sigma T^4
$$
Where:
- $4 \pi R^2$  = the surface area of the body
- $T$ = is the temperature of the body in Kelvin
- $σ$ = the Stefan-Boltzmann constant
	- $\sigma = 5.670374419 \times 10^{-8} W m^{-2}K^{-4}$
		- **Watts** per square meter per Kelvin to the fourth power 1 K⁴
		- It tells you how much **radiant energy per second** (i.e., power) is emitted by a **1 square meter** portion of a **perfect blackbody** at **1 K⁴**.

In worldmaking terms, we can simplify the Stefan-Boltzmann equation to:

$$
\dfrac{L_s}{L_{Sun}} = \left(\dfrac{R_s}{R_{Sun}}\right)^2 \left(\dfrac{K_s}{K_{Sun}}\right)^4
$$
Where:
- $L_S$ = the absolute luminosity of the star
- $L_{Sun}$ = the absolute luminosity of the Sun
- $R_S$ = the absolute radius of the star
- $R_{Sun}$ = the absolute radius of the Sun
- $K_S$ = the Kelvin temperature of the star
- $K_{Sun}$ = the Kelvin temperature of the Sun

Because the form $\dfrac{X_s}{X_{Sun}}$ is the standard for converting a parameter to solar units, and $T = \dfrac{K_s}{K_{Sun}}$, this equation becomes:

$$
\begin{aligned}
L &= R^2T^4, \\[1.5ex]
& \text{with derivations of} \\[1ex] 
R &= \dfrac{\sqrt{L}}{T^2}, \qquad
T = \sqrt[4]{\dfrac{L}{R^2}}
\end{aligned}
$$
## Parameter Calculation Precedence
The above being the case, there is a "best" order for calculating stellar parameters when starting from any given parameter (though it is always best start with *K* or *T* whenever possible).

> All parameters (except $K$) are expressed in Solar-relative units; that is, $T = 1\odot$ for $5800$ K, $R = 1\odot$ for the solar radius, etc.

#### Starting with Temperature ($T$) or ($K$)
**Primary dependency chain**: $T/K \rightarrow R \rightarrow L \rightarrow M \rightarrow Q$

$$
\begin{aligned}
T &= \dfrac{K}{5800} \quad or \quad K = 5800T \\[1ex]
R &= T^{1.8} \\[1ex]
L &= R^2T^4 \\[1ex]
M &= T^{1.98} \quad or \quad M = \sqrt[0.9]{R} \\[1ex]
Q &= T^{-5} \quad or \quad Q = M^{-2.5}
\end{aligned}
$$
#### Starting with Mass ($M$)
**Primary dependency chain**: $M \rightarrow T/K \rightarrow R \rightarrow L \rightarrow Q$

$$
\begin{aligned}
T &= \sqrt[1.98]{M} \\[1ex]
K &= 5800T \\[1ex]
R &= T^{1.8} \quad or \quad R = M^{0.9} \\[1ex]
L &= R^2T^4 \\[1ex]
Q &= T^{-5} \quad or \quad Q = M^{-2.5}
\end{aligned}
$$
#### Starting with Radius ($R$)
**Primary dependency chain**:$R \rightarrow T \rightarrow K \rightarrow L \rightarrow M \rightarrow Q$

$$
\begin{aligned}
T &= \sqrt[1.8]{R} \\[1ex]
K &= 5800T \\[1ex]
L &= R^2T^4 \\[1ex]
M &= T^{1.98} \\[1ex]
Q &= T^{-5} \quad or \quad Q = M^{-2.5}
\end{aligned}
$$
#### Starting With Luminosity ($L$)
**Primary dependency chain**: $L \rightarrow T \rightarrow K \rightarrow R \rightarrow M \rightarrow Q$

$$
\begin{aligned}
T &= \sqrt[7.6]{L} \\[1ex]
K &= 5800T \\[1ex]
R &= T^{1.8} \\[1ex]
M &= T^{1.98} \\[1ex]
Q &= T^{-5} \quad or \quad Q = M^{-2.5}
\end{aligned}
$$
#### Starting with Lifetime ($Q$)
**As soon as you assume you'd never want to do this, you'll find a case for doing it.**
**Primary dependency chain**: $Q \rightarrow T \rightarrow K \rightarrow R \rightarrow L \rightarrow M$

$$
\begin{aligned}
T &= Q^{-0.2} \\[1ex]
K &= 5800 T \\[1ex]
R &= Q^{-0.36} \\[1ex]
L &= R^2 T^4 \\[1ex]
M &= \sqrt[3]{L}
\end{aligned}
$$
# Fine-tuning Stellar Parameters
## Standard Parameter Equations
The Standard Parameter Equations shown in Equation set (1), above, *generally* work well for most **Main Sequence** stars, but a survey of known stars in the Solar neighborhood suggests that *modest* adjustments to a couple of key exponents yield parameter equations that better reflect observed stellar characteristics.  Since worldmaking prioritizes plausible-world construction over strict theoretical purity, these revised values offer better performance across the mass range of interest.
### **Main Sequence** Stellar Equations of State
$$
\begin{array}{c|c|c|c|c}
\text{Temperature} &\text{Mass} &\text{Radius} &\text{Lifetime} & \text{Lifetime} \\[0.1em]
\text{(T)} &\text{(M)} &\text{(R)} & \text{($Q$)} &\text{(L)} \\[0.5em] 
\hline
T=\sqrt{M} & M=\sqrt[0.9]{R} & R=M^{0.9} & Q=M^{-2.5} & L = M^{3.8} \\[0.5em]
T=\sqrt[1.8]{R} & M=T^{1.98} & R=T^{1.8} & Q \approx \sqrt[-0.36]{R} & L \approx R^{4.\bar{2}} \\[0.5em]
T=Q^{-0.2} & M=Q^{-0.4} & R=Q^{-0.36} & Q=T^{-5} & L = T^{7.6} \\[0.5em]
T= \sqrt[7.6]{L} & M = \sqrt[3.8]{L} & R \approx \sqrt[4.\bar{2}]{L} & Q = L^{-1.52} & L = \sqrt[-1.52]{Q}
\end{array}
$$

**Notes**:
- The parameter relationship that changed from the previous table was $T ↔︎ M$, where the exponent increased slightly from $1.98$ to $2.0$
- The **major change** is the addition of direct calculation for the parameters to-and-from luminosity; these are included for the purpose of simplifying much of the math.
- 
- **For *greatest accuracy***:
	- The exponent $7.6$ can be more precisely specified as $7.5778$
	- The exponent $3.8$ can be more precisely specified as $3.7889$