# Sectal-Length Estimation Methods (Sinusoidal)
This process assumes that you have already determined the duration of your planet's orbit around its star (its *sidereal chronum*, $\chi$).

## Chronex of the Tempostat

- **Sectal** *(pl. secta)* —  
  One quarter of a planet’s orbital period (denoted $S_0, S_1, S_2, S_3$); a **non-climatological “sectal.”**  
    A sectal is a **temporal span**, not a spatial angle — a section of the orbit *traversed through time* between two successive chronal stations.

**Tempostat** —
The **onset event** of the first sectal following periapsis; marks the temporal origin of the planet’s annual cycle.
* Defined by its **chronex (ζ)** — the true anomaly of the planet at the moment the first axial station occurs post-periapsis.
* The tempostat is an *event*, not a variable; it establishes the chromum’s temporal phase reference.
* It need not correspond to any surface season or cultural new year — it is purely orbital and axial in definition.

- **Chronex** *($\zeta$)* —  
  The **true anomaly** of the tempostat.  

## 1. Sinusoidal Approximation (Fast vs. Slow Half)
Here is a quick, algebra-only method that captures the *main effect of eccentricity* on secta:

$$
S \;\approx\; \dfrac{\chi}{4} + \left(\dfrac{2\!\;\chi\!\;e}{\pi} \times \sin \zeta\right)
$$
Where:  
- $\chi$ = year length (chronum, in diurns or days)  
- $e$ = orbital eccentricity  
- $\zeta$ = true anomaly of the tempostat  

## Sectal Adjustment
True anomaly of each **sectal onset** is determined from the **chronex** (ζ):

$$
\begin{aligned}
&\nu_n = (\zeta + 90n) \bmod 360 \\[1em]
&\begin{cases}
n = 1 & S_0 \\
n = 0 & S_1 \\
n = 3 & S_2 \\
n = 2 & S_3 \\
\end{cases}
\end{aligned}
$$
**NOTE: *The n-values here are out of numerical order so that the Earth's seasons come out listed in order of:***
- Spring
- Summer
- Autumn
- Winter

For fictional worlds, using an order of n = {0, 1, 2, 3}  will still produce usable results — which surface season they apply to is a matter of crafter's-choice.

#### Worked Example: Earth (Sinusoidal Approximation, Sidereal Chronum)
Given:  
- $\zeta = 77$  
- $\chi = 365.2564$ d (sidereal year)  
- $e = 0.0167$  

**Step 3 — Sectal Adjustments**
True anomalies from $\zeta = 0$:

$$
\nu_n = (\zeta + 90n) \bmod 360
$$
$$
\begin{cases}
n = 1 & \nu_1 = 167^\circ & \quad S_0 \\
n = 2 & \nu_2 = 77^\circ & \quad S_1 \\
n = 3 & \nu_3 = 347^\circ & \quad S_2 \\
n = 0 & \nu_0 = 357^\circ & \quad S_3
\end{cases}
$$

**Step 4 — Apply the Formula**

$$
S_n \;\approx\; \frac{\chi}{4} + \left(\frac{2\!\;\chi\!\;e}{\pi} \times \sin \nu_n \right)
$$
$$
\begin{cases}
n=1;\;\nu_1 = 167^\circ;\;\sin\nu_1 = 0.2250 & S_0 \approx 92.18 \\
n=2;\;\nu_2 = 257^\circ;\;\sin\nu_2 = 0.9744 & S_1 \approx 87.53 \\
n=3;\;\nu_3 = 347^\circ;\;\sin\nu_3 = -0.225 & S_2 \approx 90.44 \\
n=0;\;\nu_0 = 77^\circ;\;\sin\nu_0 = -0.9744 & S_3 \approx 95.09
\end{cases}
$$

**Result:**  
- $S_0$ ≈ 92.18 d  
- $S_1$ ≈ 95.09 d  
- $S_2$ ≈ 90.44 d  
- $S_3$ ≈ 87.53 d  
(Total = 365.24219 d)

**Conclusion**

The observed lengths of Earth's sectals are approximately:
- $S_0$ ≈ 92.771 d  
- $S_1$ ≈ 93.641 d  
- $S_2$ ≈ 89.834 d  
- $S_3$ ≈ 88.994 d
- (Total = 365.2400 d)
    - The difference in the totals here is due to the fact that the process is returning fractions of the *sidereal year*, but the observed values are fractions of the *tropical year*.

Discrepancies:

- $S_0$ ≈ -0.59 d  
- $S_1$ ≈ 1.49 d  
- $S_2$ ≈ 0.60 d  
- $S_3$ ≈ -1.47 d 

### ⚠️ **Symmetry Note — When ζ mod 90° = 0**

The sinusoidal tempostatic equation:

$$
S_n \;\approx\; \frac{χ}{4} + \frac{2\!\,\chi\!\;e}{\pi} \sin\nu_n
$$

produces two identical sectal durations whenever the **tempostat chronex ζ** lies at a 90° multiple — that is, when $ζ \bmod 360° = 0°, 90°, 180°, 270°$.

This arises directly from the sine function’s symmetry:

$$
\sin(ζ + 180°) = −\sin ζ.
$$

As a result, **S₀** and **S₂** (the first and third secta) mirror one another in duration, yielding *paired secta*.  

In any real planetary system where ζ ≠ 0° (mod 90°), this degeneracy breaks naturally and all four secta become distinct.  
No correction or “fudge factor” is required.

> **Note:** This pairing is *not* a failure of the method.  
> It reflects the actual temporal geometry a world would experience if its tempostat chronex ζ were perfectly aligned with a symmetry point of its orbit.
> 
> Such a planet would, in fact, exhibit two matching sectal spans during each chromum.
