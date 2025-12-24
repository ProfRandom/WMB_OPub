---
title: "Orbits-4 — Kepler’s Eccentric Anomaly Method"
summary: Step-by-step procedure for estimating sectal durations using Kepler’s relations between true, eccentric, and mean anomalies.
domain: metric
category: methods
status: canonical
version: 1.0
updated: 2025-11-06
contributors: [M. Conrad, GPT-5]
---

# 1 · Context and Purpose

The **Eccentric Anomaly Method** provides a geometric and temporal framework for estimating **sectal durations** on worlds whose orbits are **non-circular**.

In the *World Crafting Basics* system, it serves as the **canonical procedure** for converting a planet’s **orbital geometry** into **time fractions** of its *chronum* — the sidereal year.

In any elliptical orbit, the planet’s orbital speed varies: it moves **faster near periapsis** (closest to the star) and **slower near apoapsis** (farthest away).

Because of this, the four “seasons” or **secta** do not occupy equal fractions of the year.  Where Kepler observed that planets sweep out *equal areas in equal times*, we might invert the insight to say that they traverse *equal distances in unequal times*.  This inversion reframes orbital mechanics from a geometric principle into an experiential one: a rhythm of motion that shapes the tempo of a world’s year.

The difference in season length arises purely from the **eccentricity** of the orbit, independent of axial tilt or climate.

The eccentric anomaly ($E_n$) is the key intermediary that links **spatial position** (true anomaly, $ν$) with **temporal progress** (mean anomaly, $\textit{ϛ}_n$).  

For **worldmakers**, this method turns abstract orbital parameters into practical narrative data:  
- It determines how long each season lasts on a given world.  
- It shows how eccentricity can create longer summers and shorter winters — or vice versa — without altering obliquity.  
- It provides a foundation for climate timing, cultural calendars, and the rhythm of a planet’s year.

By pairing **Kepler’s geometry** with **WCB’s chronum–sectal framework**, the eccentric anomaly method gives a clear, reproducible way to convert orbital shape into lived temporal experience — the heartbeat of a world’s cycle.

## 2 · Vocabulary

- **Chronum** *($\chi$)* —  
  One complete sidereal orbit; the planet’s **year** expressed in diurns.

- **Sectal** *(pl. secta)* —  
  One quarter of a planet’s orbital period (denoted $S_0, S_1, S_2, S_3$); a **non-climatological “season.”**  
    A sectal is a **temporal span**, not a spatial angle — a section of the orbit *traversed through time* between two successive chronal stations.
  - Sectal₀ begins with the tempostat (q.v.), and ends with the onset of the next chronal station.

- **Tempostat** —  
  The **onset of the first sectal** following periapsis; marks the temporal origin of the planet’s annual cycle.  
  - This need not correspond to a “spring” or vernal point for any given hemisphere — it is purely orbital and axial, not sectal, in definition.  

- **Chronex** *($\zeta$)* —  
  The **true anomaly** of the tempostat.  

- **Eccentricity** *($e$)* —  
  Describes how far the orbit departs from circularity (0 = circle, < 1 = ellipse).  

- **True Anomaly** *($\nu$)* —  
  The **spatial angle** between periapsis and the planet’s actual position, measured from the system’s focus.
Some true anomalies are associated with specific locations on the orbit where significant geometric transisions occur, but every position of a planet along its orbital path corresponds to a specific true-anomaly angle.
  - The true-anomaly measures of the four secta are denoted $\nu_0, \nu_1, \nu_2,\;\text{and}\; \nu_3$, calculated by:

$$
    \nu_n = (\zeta + 90n) \bmod 360
$$
 — where *n* is the **index of the sectal**.

- **Eccentric Anomaly** *($E_n$)* —  
  The **geometric angle** measured at the ellipse’s center to the projected point on its circumscribed circle; it simplifies Kepler’s relations and is generally denoted $E$, but the eccentric anomalies of the four secta are denoted $E_0, E_1, E_2,$ and $E_3$.

$$
\begin{gathered}
E_n = 2 \arctan \!\left( \xi \;\tan \frac{\nu_n}{2} \right), \qquad
\nu_n = 2 \arctan \!\left( \frac{1}{\xi} \;\tan \frac{E_n}{2} \right)
\end{gathered}
$$
*All angular measures in WCB are expressed in degrees unless otherwise specificially noted.*

- This represents an **algebraic frame-shift** that permits calculation of the **mean anomaly** ($\textit{ϛ}_n$) of a given sectal by projecting the *true anomaly* onto the circumscribed reference circle.

- **Mean Anomaly** *($\textit{ϛ}_n$)* —  
  The **temporal angle** that increases uniformly with time, defining a constant angular rate around the orbit.  
  Kepler’s relation (modified for WCB):

$$
\textit{ϛ}_n = \frac{(E_n - e\,\sin E_n) \bmod 360}{360}
$$

  This translates the varying orbital motion into a **uniform time variable**, allowing direct calculation of how much of the chronum has elapsed at any given point on the ellipse.  It represents the planet’s position as if it moved at steady speed along a circular path, providing a linear measure of elapsed orbital time.

> Note that $E_n$ **cannot** easily be back-calculated from $\textit{ϛ}_n$!

- **Eccentric Tangent Factor** *($\xi$)* —
  - A dimensionless helper constant linking *true* and *eccentric* anomalies through their tangent relation, calculated by:  

$$
	\xi = \sqrt{\frac{1 - e}{1 + e}}, \qquad
  \frac{1}{\xi} = \sqrt{\frac{1 + e}{1 - e}}
$$

- **Obliquity** *($\varepsilon$)* —  
  The **axial tilt** between a planet’s spin vector and the normal to its orbital plane.  
-  It governs the **intensity and polarity** of insolation across hemispheres, affecting climatic seasons but not the geometric secta themselves.

- **Prime Solstice** —  
  The moment in a planet’s chromum when its rotational axis is tilted **directly away** from the star, as viewed from above the planet’s right-hand-rule north pole.  
  - It marks the **maximum negative tilt** of the northern hemisphere relative to the star and serves as the reference orientation for defining chronal stations and obliquity-based chronal events.

These quantities together define the **Kepler frame** — the bridge between spatial geometry and temporal rhythm in the chromum.

# Eccentric Anomaly Conversion (Kepler’s Method)

## 1. Identify Key Quantities

Before beginning the conversion, identify the following key quantities:

- **$\varepsilon$** — the planet’s **obliquity** (axial tilt).  
  - *Note:* a planet with no tilt ($\varepsilon = 0$) experiences no seasons — and therefore no secta — in the usual sense. Proceeding further in such a case is non-productive.  
- **$e$** — orbital **eccentricity**, describing how far the planet’s orbit departs from circularity.  
- **$\zeta$** — the **chronex**, the true-anomaly angle of the first cardinal event (*tempostat*) to occur after the planet passes periapsis.  
- **$\chi$** — the planet’s **chronum**, its sidereal orbital period, best expressed in diurns (days).  

### How do I determine my planet’s *chronex*?

You choose it — but the choice shapes the rhythm of the world’s year. Consider the following:

**A.** Which sectal (“season”) do you want to begin **less than $90^\circ$ after periapsis**?  
That is your *tempostat.*  
> **Requirement:**  
> The chronex must fall within the first 90° of true anomaly after periapsis $(\zeta < 90°).$  
> This ensures that the tempostat — the first chronal station following periapsis — anchors the start of the chromum correctly.

If you’re designing a world from its sectal behavior outward, start by deciding **which sectal you want a particular season to occupy.**  From that, work backward to locate the first chronal station after periapsis — this determines **ζ**, the chronex of the tempostat. *(See the next section for calculation steps.)*

> **Requirement:**  
> The chronex must fall within the first 90° of true anomaly after periapsis ($\zeta < 90°$).  
> This ensures that the tempostat — the first chronal station following periapsis — properly anchors the start of the chromum.

**B.** The specific sectal you choose matters only insofar as it determines how the **fractions of the chronum** are distributed among the secta.

Sorted by duration, shortest-to-longest, the secta are:
- **$S_3$** — periapsis always falls in this sectal  
- **$S_2$**  
- **$S_0$**  
- **$S_1$** — apoapsis always falls in this sectal  

Thus, if you want your planet’s northern hemisphere summer to be the longest season, design its orbital geometry so that the *prime solstice* occurs during **$S_3$** — the periaptic sectal.

## 2. Calculate Secta ($Ⲁ_n$)

### Step 1 — Calculate The Eccentric Tangent Factor ($\xi$)

$$
\xi = \sqrt{\frac{1 - e}{1 + e}}
$$

### Step 2 — Calculate True Anomalies of the Chronal Stations
Calculate the true anomalies ($Ⲁ_n$) for the four sectal markers, offset by the chronex of the tempostat $\zeta$:

$$
\begin{aligned}
&\nuⲀ_n = (\zeta + 90n) \bmod 360 \\[1em]
&\begin{cases}
n = 0; \;\text{Sectal₀} \\
n = 1; \;\text{Sectal₁} \\
n = 2; \;\text{Sectal₂} \\
n = 3; \;\text{Sectal₃} \\
\end{cases}
\end{aligned}
$$

### Step 3 — Convert the True Anomalies to Eccentric Anomalies
For each $Ⲁ_n$, compute the eccentric anomaly $E_n$:

$$
\begin{aligned}
E_n &= 2 \arctan \!\left( \xi \;\tan \frac{\nu_n}{2} \right) \\[1em]
\nu_n &= 2 \arctan \!\left( \frac{1}{\xi}\;\tan \frac{E_n}{2}\right) \qquad \text{Inverse Relation}
\end{aligned}
$$
*All angular measures in WCB are expressed in degrees unless otherwise specificially noted.*

### Step 4 — Convert to Mean Anomaly
Translate each $E_n$ into mean anomaly $\textit{ϛ}_n$, which grows linearly with time:

$$
\textit{ϛ}_n = \frac{E_n - (e \sin E_n)}{360}
$$

The resulting mean anomalies ($\textit{ϛ}\_n$) represent the fractional progress through the chronum at each chronal station.  The differences between successive values yield the four sectal durations.

### Step 5 — Calculate the Sectal Durations ($\gamma_n$)
Once you have the mean anomalies for each sectal marker, subtract them in sequence to get the fractional year lengths:

$$
\begin{aligned}
\gamma_0 &= \frac{\textit{ϛ}_1 - \textit{ϛ}_0}{360} \\[1em]
\gamma_1 &= \frac{\textit{ϛ}_2 - \textit{ϛ}_1}{360} \\[1em]
\gamma_2 &= \frac{\textit{ϛ}_3 - \textit{ϛ}_2}{360} \\[1em]
\gamma_3 &= \frac{1 + \textit{ϛ}_0 - \textit{ϛ}_3}{360}
\end{aligned}
$$

Where:  
- Each $\gamma =$ fraction of the year occupied by that sectal.
> The first three differences are straightforward because each $ϛ$ increases through the orbit.
> The *last* subtraction crosses the $360^\circ \rightarrow 0^\circ$  boundary, so we add $1$ (representing $360^\circ$) before subtracting — ensuring the final sectal wraps correctly and the four $\gamma_n$ sum to **1.000** (the whole chronum).

### Step 6 — Scale to Year Length
Multiply each fraction by the chronum ($\chi$) to convert fractions into diurns:

$$
S_n = \chi \cdot \gamma_n
$$

These $S_n$ values represent the lengths of the four secta — the **unequal** segments of the chromum defined by the planet’s orbital eccentricity and tempostatic orientation.

# Worked Example
Given:  
- $\zeta = 33^\circ$  
- $\chi = 360$ days (sidereal year)  
- $e = 0.5$
  - Note that this is an *extreme* eccentricity, used solely for the purposes of demonstration!  

**Step 1 — True Anomalies**
Sectal markers from $\zeta = 33^\circ$:  

$$
\nu_n = (\zeta + 90n) \bmod 360 \qquad
\begin{cases}
n = 0 & \nu_0 = 33^\circ \\
n = 1 & \nu_1 = 123^\circ \\
n = 2 & \nu_2 = 213^\circ \\
n = 3 & \nu_3 = 303^\circ
\end{cases}
$$
> Note that these are not associated with any particular "season" at this time, they are just geometric divisions of the orbit.
 
**Step 2 — Convert to Eccentric Anomaly**
Kepler’s orbit runs faster near periapsis and slower near apoapsis, so we next translate the true anomalies into **eccentric anomalies**, which measure angles on the auxiliary circle.

$$
E_n = 2 \arctan \!\left( \xi \;\tan \dfrac{\nu_n}{2} \right) \qquad
\begin{cases}
E_0 = 19.4^\circ \\
E_1 = 93.5^\circ \\
E_2 = 234.8^\circ \\
E_3 = 325.5^\circ
\end{cases}
$$
> The eccentric anomaly is a *geometric intermediary*: it preserves the orbital geometry but lets us connect angle to time through Kepler’s equation.

**Step 3 — Convert to Mean Anomaly**
The **mean anomaly ($ϛ$)** increases uniformly with time, making it the “clock angle” of the orbit.
Note the use of the symbol ⛛ here which denotes that these are **temporal angles**, not spatial ones.

$$
ϛ_n = E_n - (e \sin E_n) \qquad
\begin{cases}
ϛ_0 = 19.22^\triangledown \\
ϛ_1 = 92.94^\triangledown \\
ϛ_2 = 234.32^\triangledown \\
ϛ_3 = 325.19^\triangledown
\end{cases}
$$

> These ϛ values show *where in time* each station occurs within the chronum.  Notice that the increments between them are **unequal**, reflecting the planet’s varying speed at different times in its journey around its orbit.

**Step 4 — Find Season Fractions**
Subtract successive $ϛ$ values to find the fraction of the *chronum* spent in each sectal:

$$
\begin{aligned}
\gamma_0 &= \frac{\textit{ϛ}_1 - \textit{ϛ}_0}{360}
= \frac{92.94 - 19.22}{360} = \boxed{0.2048}\\[1em]
\gamma_1 &= \frac{\textit{ϛ}_2 - \textit{ϛ}_1}{360}
= \frac{234.32 - 92.94}{360} = \boxed{0.3940}\\[1em]
\gamma_2 &= \frac{\textit{ϛ}_3 - \textit{ϛ}_2}{360}
= \frac{325.19 - 234.32}{360} = \boxed{0.2520}\\[1em]
\gamma_3 &= \frac{1 + \textit{ϛ}_0 - \textit{ϛ}_3}{360}
= \frac{1+ 19.22 - 325.19}{360} = \boxed{0.1492}
\end{aligned}
$$
> The first three differences are straightforward because each $ϛ$ increases through the orbit.
> The *last* subtraction crosses the $360^\circ \rightarrow 0^\circ$  boundary, so we add $1$ (representing $360^\circ$) before subtracting — ensuring the final sectal wraps correctly and the four $\gamma_n$ sum to **1.000** (the whole chronum).

**Step 5 — Scale by the Chronum Length**
Each $\gamma_n$ expresses a *fraction* of the chronum ($\chi$).
Multiplying converts them into actual durations:
 
$$
S_n = \chi\, \gamma_n \qquad
\begin{cases}
S_0 = 360 \cdot 0.2048 = 73.72\; \text{days} \\
S_1 = 360 \cdot 0.3940 = 141.85\; \text{days (apoaptic)} \\
S_2 = 360 \cdot 0.2520 = 90.73\; \text{days} \\
S_3 = 360 \cdot 0.1493 = 53.70\; \text{days (periaptic)}
\end{cases}
$$

> These are the temporal divisions of the orbit.
Note that the planet spends almost **three times longer near apoapsis** (S₁) than near periapsis (S₃) — a direct expression of Kepler’s Second Law.

# Orbital Eccentricity and Seasonal Effects

For a planemon orbiting a star (M₂ ⋘ M₁):
- **Periastron distance**:  

$$
 R_{min} = A(1 - e)
$$
- **Apastron distance**:  

$$
 R_{max} = A(1 + e)
$$
Where **A** is the *average orbital separation* between the bodies.  
When describing a planemon’s orbit, A corresponds to the **semimajor axis** of its elliptical path.  

## Fractional Distance Asymmetry (Ḋ)
The dimensionless measure of how much closer the planemon is to the star at periastron than at apastron:

$$
\dot{D} = \frac{R_{max}}{R_{min}} - 1 = \frac{2e}{1-e}
$$
- Earth ($e = 0.0167$):  $\dot{D} \approx 0.034$ → **3.4% closer at periastron**  
- Rosetta ($e = 0.05$):  $\dot{D} \approx 0.105$ → **10.5% closer at periastron**

## Flux Ratio
Because stellar flux $F ∝ 1/R^2$, the insolation contrast between periastron and apastron is:

$$
\frac{F_{min}}{F_{max}} = \left(\frac{R_{max}}{R_{min}}\right)^2
$$
- Earth ($e = 0.0167$):  $\frac{F_{min}}{F_{max}} \approx 1.068$ → **6.8% stronger insolation at periastron**  
- Rosetta ($e = 0.05$): $\frac{F_{min}}{F_{max}} \approx 1.23$ → **23% stronger insolation at periastron**

## WCB Note

- **Distance form (Ḋ)** → intuitive “how much closer/farther” language.  
- **Flux form ($\frac{F_{min}}{F_{max}}$)** → climatic impact (“how much hotter/colder”).  
- **Canonical terminology**: use *periastron/apastron* with $R_{min}$ and $R_{max}$ in star–planemon systems.  
- Avoid $r_p$, $r_a$, or ß notations; these are legacy/derivation-only.  
- In WCB canon, Ḋ is the preferred symbol for distance asymmetry.


## Applying Seasons



<!-- **Conclusion**
The Kepler method and sinusoidal shortcut agree closely but not exactly; but Kepler adds nuance:  
- Winter is slightly shorter, summer slightly longer, compared to the sinusoidal baseline.  
- Spring and autumn remain nearly identical.  

With Rosetta’s higher eccentricity ($e = 0.05$), the **sectal spread is extreme** — from 107 d to 139 d — a difference of over 30 diurns.  

This is exactly the kind of asymmetry you would expect on a world with such an orbit, and it needs **no fudge at all**. -->
