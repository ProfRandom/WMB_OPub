---
project: wmb
phase: 1
module: 1
status: draft
created: <%* tp.file.creation_date("YYYY-MM-DD") %>
updated: <%tp.date.now("YYYY-MM-DD") %>
summary: ""
---
 

# Fleshing Out A Star System

We've established:
- [[Stellamons -- Stars and Spectral Classes|Stars and Spectral Classes]]
- [[Orbits, Thermozones, and Animozones]]
- [[Stellamons -- Orbital Habitability Index|Orbital Habitability Index]]
- [[Orbits, Thermozones, and Animozones|Nucleal]] ($N$) Orbit, and
- [[Orbits, Thermozones, and Animozones|Perannual]] ($P$) Orbit

But planemons don't orbit only at these discreet distances – they're all over the place. Here's a breakdown of our own Solar system's planemon orbit data:

$$
\begin{array}{l | r | r}
\textbf{Planemon} & \textbf{$SMA^*$ (AU)} & \textbf{$e^†$}\hspace{1ex} \\
\hline
\textbf{Mercury} & 0.387 & 0.2056 \\[1ex]
\textbf{Venus} & 0.723 & 0.0068 \\[1ex]
\textbf{Earth} & 1 & 0.0167 \\[1ex]
\textbf{Mars} & 1.524 & 0.0934 \\[1ex]
\textbf{Asteroids} & (2.2 \cdot\cdot\; 3.2) & μ = 2.7 \\[1ex]
\textbf{Jupiter} & 5.204 & 0.0489 \\[1ex]
\textbf{Saturn} & 9.583 & 0.0565 \\[1ex]
\textbf{Uranus} & 19.191 & 0.2056 \\[1ex]
\textbf{Neptune} & 30.070 & 0.0087 \\[1ex]
\end{array}
$$
> >$\small *\; SMA = \text{semi-major axis}$
> >$\small †\; e = \text{orbital eccentricity}$
## Orbital Parameters
Ignoring the asteroid belt for the moment and inserting Ceres as the largest member of the belt:

$$
\begin{array}{l | r | r | r | r}
\textbf{Planemon} & \textbf{$SMA^*$ (AU)} & \textbf{$e^†$}\hspace{1ex} & \textbf{Gap (AU)} & \textbf{Interval (AU)} \\
\hline
\textbf{Mercury} & 0.387 & 0.2056 & —  &  — \\[1ex]
\textbf{Venus} & 0.723 & 0.0068 & 0.3362 & 1.8686 \\[1ex]
\textbf{Earth} & 1 & 0.0167 & 0.2767 & 1.3825 \\[1ex]
\textbf{Mars} & 1.524 & 0.0934 & 0.5237 & 1.5237 \\[1ex]
\textbf{Ceres} & 2.7 & 0.15 & 0.1763 & 1.7720 \\[1ex]
\textbf{Jupiter} & 5.204 & 0.0489 & 2.5038 & 1.9273 \\[1ex]
\textbf{Saturn} & 9.583 & 0.0565 & 4.3788 & 1.8415 \\[1ex]
\textbf{Uranus} & 19.191 & 0.2056 & 9.6087 & 2.0227 \\[1ex]
\textbf{Neptune} & 30.070 & 0.0087 & 10.8787 & 1.5669 \\[1ex]
\end{array}
$$

>Notes:
>\* The orbital **gap** is calculated by subtracting the planemon's orbital distance from the next closer-in planemon's orbital distance
> 
> $$G = O_n - O_{n-1}$$
> >† The orbital **interval** is calculated by dividing the planemon's orbital distance by the next closer-in planemon's orbital distance:
> 
> $$I = \dfrac{O_n}{O_{n-1}}$$

What we are concerned with here is the orbital *intervals*:
- The minimum interval is between Venus and Earth: $I = 1.3825\;AU$
- The maximum interval is between Uranus and Neptune: $I = 2.0027\;AU$
- The average interval is $I \approx 1.74\;AU$
- The median interval is $I \approx 1.81\;AU$
- The standard deviation is $\sigma = 0.2051$

This supports defining a **WMB-conservative orbital interval range** of $(1.400 ·· 2.000)$ AU by rounding up the minimum and rounding down the maximum.

However, a cursory survey of the Exoplanet Catalog seems to reveal a range of $(1.000 ·· 5.000)$ AU for planetary orbital intervals.  We'll define this as our optimistic orbital interval range, and, for completeness, average the two ranges at $(1.200 ·· 3.500)$ AU.

**Orbital interval ranges**

| Inner | Outer | Description |
| -----:| -----:| ------------ |
| 1.4 | 2 | Conservative |
| 1.2 | 3.5 | Medial |
| 1 | 5 | Optimistic |
# Calculating Other Orbits

This brings us to methods of calculating other orbits in a star system. In practice, any method the worldmakerchooses is *valid*, including just putting planemons where *it feels right*; however, even using this method *should* ideally take into account the above statistics and try to avoid an orbital interval between a given planemon and its nearest neighbor of $< 1.500\;AU$ or $> 2.000\;AU$.

## Starting From A Known Orbit

Most of the time, you'll have pre-established a particular orbit — usually either the *nucleal* or the *perannual* orbit, and want to arrange other planemons in the system relative to that orbit. Notating this orbit as the **base** orbit, we can set up two processes for calculating orbits inferior to (closer-in than) and superior to (farther-out than) that orbit.

**Intrabasal Orbit Calculation Process**

$$
r_i = B;\; \Omega = \text{«▢»}: \qquad
r_{i-1} = \frac{r_i}{(( \text{min} ·· \text{max} ))}
\quad \text{while } r_{i-1} ≥ \Omega
$$
**Extrabasal Orbit Calculation Process**

$$
r_i = B;\; \Omega = \text{«▢»}: \qquad
r_{i+1} = r_i \cdot (( \text{min} ·· \text{max} ))
\quad \text{while } r_{i+1} ≤ \Omega
$$
Where:
- *B* = basal orbital radius (e.g. the nucleal orbit $N$)
- *Ω* = orbital distance cuttoff (minimum or maximum allowed orbit based on the star system constraints)

## Usage Strategy

*Assuming the medial orbital interval range* $I \in ((1.200 ·· 3.500))\;AU$:
The **intrabasal** and **extrabasal** forms can be used independently depending on your desired anchoring strategy:

> **Inward-Only Generation** 
 If you begin at the **basal orbit** (innermost, nucleal, perannual, etc.), use the **intrabasal** form to expand inward via divisive steps:

$$
 r_0 = B;\; \Omega = «▢»:
 \quad r_{i-1} = \dfrac{r_i} {((1.200 ·· 3.500))}, \text{ while } r_{i-1} ≥ \Omega
$$
Where:
- *Ω* = the minimum safe orbital distance — usually taken to be $a = 0.100\;AU$.

> **Outward-Only Generation** 
 If you begin at an **innermost orbit** (e.g. a thermal, Roche, or design constraint), use the **intrabasal** form to expand outward via multiplicative steps:

$$
 r_0 = B;\; \Omega = «▢»:
 \quad r_{i+1} = r_i \cdot ((1.200 ·· 3.500)), \text{ while } r_{i+1} ≤ \Omega
$$
Where:
- *Ω* = the farthest orbit desired for a planemon in the system — based on whatever criterion desired, but physically limited to the Hill Sphere radius of the central mass.

> [!tip]
> > Applying these methods can fully define a system.
> > - If one wanted to start with the innermost safe orbit; e.g. $B = 0.100\;AU$, then one would use only the extrabasal process to calculate orbits outward.
> > - Conversely if one wanted to start with the most distant orbit, then one would use only the intrabasal process to calculate orbits inward.


> [!important]
> >> *If you are not starting from the perannual or nucleal orbit, always check randomized orbits against either (or both) to ensure proper interval **gaps** fall to either side of that orbit, and adjust accordingly!*

## A Worked Example

Let us say we've identified our nucleal orbit ($N$) as $N = 0.834\;AU$, and we want to calculate orbits interior-to and exterior-to that orbit, and we've chosen $a = 0.100\;AU$ as our innermost safe orbit.

### Working Inward
$$
\begin{aligned}
 r_0 &= 0.834;\; \Omega = 0.100:
 \quad r_{i-1} = \dfrac{r_i}{\langle1.200 \le x; x \le 3.500\rangle}, \text{ while } r_{i-1} ≥ 0.100 \\
r_{i-1} &= \dfrac{0.834} {1.723} = 0.482\;AU \qquad 1.732 := \text{Randomized interval between $\langle1.200 \le x; x \le 3.500\rangle$ AU} \\[1ex]
r_{i-1} &= \dfrac{0.482} {1.616} = 0.298\;AU \qquad 1.616 := \text{Randomized interval between $\langle1.200 \le x; x \le 3.500\rangle$ AU} \\[1ex]
r_{i-1} &= \dfrac{0.298} {1.573} = 0.190\;AU \qquad 1.573 := \text{Randomized interval between $\langle1.200 \le x; x \le 3.500\rangle$ AU} \\[1ex]
r_{i-1} &= \dfrac{0.190} {1.884} = 0.101\;AU \qquad 1.884 := \text{Randomized interval between $\langle1.200 \le x; x \le 3.500\rangle$ AU} \\[1ex]
r_{i-1} &= \dfrac{0.101} {1.963} = 0.051\;AU \qquad 1.963 := \text{Randomized interval between $\langle1.200 \le x; x \le 3.500\rangle$ AU}\;✘ \\[1ex]
\end{aligned}
$$

We stop at the fourth randomized orbit, because the next orbit randomly generated fails the $r ≥ 0.100\;AU$ test.
We now have a system of five orbits:

| Orbit | Distance |
| :-----: | :------: |
| 1 | 0.101 |
| 2 | 0.190 |
| 3 | 0.298 |
| 4 | 0.482 |
| 5 (*N*) | 0.834 |

We could stop here and have a fully legitimate star system, but let's say we want extranucleal orbits, as well. Again, beginning with the nucleal orbit $B = 0.834\;AU$, and setting an outermost orbit of $\Omega = 35.0\;AU$:

$$
\begin{aligned}
 r_0 &= 0.834;\; \Omega = 35.0 \\[1ex]
 \quad r_{i+1} &= r_i \cdot \langle1.200 \le x; x \le 3.500\rangle, \text{ while } r_{i+1} ≤ 35.0 \\[1ex]
r_{i+1} &= 0.834(1.829) = 1.525\;AU \qquad 1.829 := \text{Randomized interval between $\langle1.200 \le x; x \le 3.500\rangle$ AU} \\[1ex]
r_{i+1} &= 1.525(1.969) = 3.003\;AU \qquad 1.969 := \text{Randomized interval between $\langle1.200 \le x; x \le 3.500\rangle$ AU} \\[1ex]
r_{i+1} &= 3.003(1.578) = 4.739\;AU \qquad 1.578 := \text{Randomized interval between $\langle1.200 \le x; x \le 3.500\rangle$ AU} \\[1ex]
r_{i+1} &= 4.739(1.547) = 7.332\;AU \qquad 1.547 := \text{Randomized interval between $\langle1.200 \le x; x \le 3.500\rangle$ AU} \\[1ex]
r_{i+1} &= 7.332(1.552) = 11.379\;AU \qquad 1.552 := \text{Randomized interval between $\langle1.200 \le x; x \le 3.500\rangle$ AU} \\[1ex]
r_{i+1} &= 11.379(1.608) = 18.298\;AU \qquad 1.608 := \text{Randomized interval between $\langle1.200 \le x; x \le 3.500\rangle$ AU} \\[1ex]
r_{i+1} &= 18.298(1.823) = 33.357\;AU \qquad 1.823 := \text{Randomized interval between $\langle1.200 \le x; x \le 3.500\rangle$ AU} \\[1ex]
r_{i+1} &= 33.357(1.778) = 59.309\;AU \qquad 1.778 := \text{Randomized interval between $\langle1.200 \le x; x \le 3.500\rangle$ AU} \; ✘ \\[1ex]
\end{aligned}
$$
We stop at the seventh iteration, as the next value exceeds $\Omega = 35.0\;AU$.

This expands our system to 11 orbits:

| Orbit | Distance |
| :-----: | :------: |
| 1 | 0.101 |
| 2 | 0.190 |
| 3 | 0.298 |
| 4 | 0.482 |
| 5 (*N*) | 0.834 |
| 6 | 1.525 |
| 7 | 3.003 |
| 8 | 4.739 |
| 9 | 11.379 |
| 10 | 18.298 |
| 11 | 33.357 |

… and we can proceed to design planemons for each orbit, or eliminate some orbits and install asteroid belts, or adjust orbital intervals to suit our needs.... the sky's the limit.

With this method, a worldmaker can quickly generate a full planemon system that is physically plausible, statistically grounded, and symbolically consistent with WMB cosmology.

# Calculating the Thermozones
Since we know our nucleal orbit is $N = 0.834\;AU$, we can calculate the thermozone limits:

$$
\begin{aligned}
H_0 = 0.500N &= 0.500(0.834) = 0.417\;AU \\[1ex]
H_1 = 0.750N &= 0.750(0.834) = 0.626\;AU \\[1ex]
H_2 = 0.950N &= 0.950(0.834) = 0.792\;AU \\[1ex]
H_3 = 1.385N &= 1.385(0.834) = 1.115\;AU \\[1ex]
H_4 = 1.770N &= 1.770(0.834) = 1.476\;AU \\[1ex]
H_5 = 4.850N &= 4.850(0.834) = 4.045\;AU \quad \text{Frost Line}
\end{aligned}
$$

And we can add these to our orbits table from above and determine the thermozones and animozones of the orbits:

|  Orbit   | Distance | <center>Thermozone</center> | <center>Animozone</center> |
| :------: | :------: | --------------------------- | -------------------------- |
|    1     |  0.101   | Igniozone                   | Xenotic                    |
|    2     |  0.190   | Igniozone                   | Xenotic                    |
|    3     |  0.298   | Ignoizone                   | Xenotic                    |
|  $H_0$   |  0.417   |                             |                            |
|    4     |  0.482   | Calorozone                  | Inner Parahabitable        |
|  $H_1$   |  0.626   |                             |                            |
|  $H_2$   |  0.792   |                             |                            |
| 5 (*$N$) |  0.834   | Solarazone                  | Hospitable                 |
|  $H_3$   |  1.115   |                             |                            |
|  $H_4$   |  1.476   |                             |                            |
|    6     |  1.525   | Brumazone                   | Outer Parahabitable        |
|    7     |  3.003   | Brumazone                   | Outer Parahabitable        |
|  $H_5$   |  4.045   |                             |                            |
|    8     |  4.739   | Cryozone                    | Xenotic                    |
|    9     |  11.379  | Cryozone                    | Xenotic                    |
|    10    |  18.298  | Cryozone                    | Xenotic                    |
|    11    |  33.357  | Cryozone                    | Xenotic                    |

**Perannual Orbit**

We can calculate the perannual orbital distance and the star's spectral type by:

$$
\begin{aligned}
L &= N^2 = 0.834^2 = 0.696 \\[1ex]
M &= \sqrt[3.8]{L} = \sqrt[3.8]{0.696} = 0.909 \\[1ex]
A &= \sqrt[3]{0.909} = 0.969\;AU\; \checkmark
\end{aligned}
$$

The perannual orbit in this system is at $A = 0.969\;AU$.

**Spectral Type**

$$
\begin{aligned}
L &= 0.696 \\[1ex]
T &= \sqrt[7.6]{L} = \sqrt[7.6]{0.696} = 0.953\odot \\[1ex]
K &= 5800T = 5800(0.953) = 5529.92 \quad \text{Spectral Class G: κ = 6000; þ = 100} \\[2em]
S &= \dfrac{\kappa - K}{100} = \dfrac{6000 - 5529.92}{100} = \dfrac{470.08}{100} = 4.701\\
\end{aligned}
$$
The spectral type of our star is **G4.701**.

Wait: we already know that our nucleal orbit is at $N = 0.834\;AU$. *If* we put planemon on the perannual orbit at $A = 0.969\;AU$ the interval between the nucleal orbit and the perannual orbit is only:

$$
I = \dfrac{0.969}{0.834} = 1.162\;AU\;✓
$$
… which is less than our specified minimum $I > 1.500\;AU$.

Either we don't have a planemon on the nucleal orbit, *or* we don't have a planemon on the perannual orbit; those orbits are fixed by the stellar parameters – neither can be shifted.  This is the power — but also the limitation — of our system. Some things we can tweak as we please; other things we have to work with, or work around.

In this case, we're forced to choose between a planemon with Earth's stellar flux, or a planemon with Earth's orbital period, but we can't have both.  We'll drop the nucleal planemon and go with the parahabitable planemon ... let's work that through. Here's a modified orbit table taking that into account:

| Orbit | Distance | <center>Thermozone</center> | <center>Animozone</center> | Interval |
| :---------------: | :------: | --------------------------- | ------------------------- | -------- |
| 1 | 0.101 | Igniozone | Xenotic | |
| 2 | 0.190 | Igniozone | Xenotic | 1.884 |
| 3 | 0.298 | Ignoizone | Xenotic | 1.573 |
| $H_0$ | 0.417 | | | |
| 4 | 0.482 | Calorozone | Inner Parahabitable | 1.616 |
| $H_1$ | 0.626 | | | |
| $H_2$ | 0.792 | | | |
| 5 ($A$) | 0.969 | Solarazone | Hospitable | »1.927« |
| $H_3$ | 1.115 | | | |
| $H_4$ | 1.476 | | | |
| 6 | 1.525 | Brumazone | Outer Parahabitable | »1.574« |
| 7 | 3.003 | Brumazone | Outer Parahabitable | |
| $H_5$ | 4.045 | | | |
| 8 | 4.739 | Cryozone | Xenotic | 1.552 |
| 9 | 11.379 | Cryozone | Xenotic | 1.608 |
| 10 | 18.298 | Cryozone | Xenotic | 1.823 |
| 11 | 33.357 | Cryozone | Xenotic | 1.778 |

The interval between the perannual orbit and the next closer-in orbit is:

$$
I = \dfrac{0.969}{0.482} = 1.927\;AU
$$

… *just* within our $I = 2.000\;AU$ maximum, and the interval to the next orbit out is:

$$
I = \dfrac{1.525}{0.969} = 1.574\;AU
$$

… which, again, is *just* within our specified minimum $I = 1.500\;AU$.

> [!note]
> Planemons can certainly have wider intervals between their orbits than $I = 2.000\;AU$ – we just never want them to have an interval *less-than* $I = 1.500\;AU$.

And we can calculate that since $A = 0.969\;AU$ and $N = 0.834\;AU$, and we know that the stellar flux at $N = 1.0$, we can calculate that $A$ is:

$$
\Delta = \dfrac{0.969}{0.834} = 1.162
$$

… the perannual orbit is $1.162 \times$ farther out than the nucleal orbit, and since intensity decreases with the square of the distance:

$$
F = \dfrac{1}{\Delta^2}
$$
… we can calculate that the perannual planemon receives:

$$
F = \dfrac{1}{1.162^2}= \dfrac{1}{1.350} = 0.741
$$

… about $74.1$% of the stellar flux as the nucleal orbit does... but that's still:

$$
\begin{aligned}
H_I = -0.26\dfrac{D}{N} + 1.26 = -0.26\dfrac{0.969}{0.834} + 1.26 = -0.26(1.162) + 1.26 = -0.302 + 1.26 = 0.958
\end{aligned}
$$

… an orbital habitability index of $95.8$% that of the nucleal orbit. Slightly cooler, but not drastically so.

