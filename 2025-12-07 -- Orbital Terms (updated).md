---
project: wmb
phase: 1
module: 1
status: draft
created:
updated: 2025-12-07
summary: ""
---
# Orbital Terms (updated)

**Gyrostat** (Γ) — name and true anomaly of the Prime Solstice (see below); can be calculated from the chronostat by: $\Gamma = \Lambda - 90$.
**Chronostat** ($\Lambda$) — name and true anomaly of the Prime Equinox; determines the start of the planemon's seasonal year.
**Orthostat** ($\Phi$) — the _reference position_ where the Prime Solstice is aligned with *periapsis*; marks the beginning of the Precession Cycle (Ψ)
**Precession Cycle** (Ψ) — the interval between successive orthostats
**Precession Phase** (ψ) — the current percentage of the Precession Cycle (where the true anomaly of the gyrostat falls in the planmon's orbit); calculated by $$\psi = \frac{(\Lambda - 90) \mod 360}{360} \cdot \Psi$$**Sectastat** (ζ) — name and true anomaly of the first seasonal event following periapsis (replaces chronex); marks the origin of the orbital _secta_
**Chronum** (χ) — orbital period of the planemon (expressed in Earth sidereal years)
**Eccentricity** (e) — expresses variation from circularity of the planemon's orbit
**True Anomaly** (ν) — the *spatial angle* between periapsis and the planet’s actual position, measured from the system’s focus. Some true anomalies are associated with specific locations on the orbit where significant geometric transisions occur, but every position of a planet along its orbital path corresponds to a specific true-anomaly angle.
**Eccentric Anomaly** (E) — the *geometric angle* measured at the ellipse’s center to the projected point on its circumscribed circle
**Mean Anomaly** (ς) — the *temporal angle* that increases uniformly with time, defining a constant angular rate around the orbit.
**Eccentric Tangent Factor** (ξ) – a dimensionless helper constant linking *true* and *eccentric* anomalies through their tangent relation, calculated by $$\xi = \sqrt{\frac{1 - e}{1 + e}}$$
**Obliquity** (ε) — _axial tilt_ between the spin vector and orbital normal. Governs the polarity and amplitude of hemispheric seasons.
**Prime Solstice** — the position in a planemon's orbit when its rotational axis is tilted directly away from the barymetric center of the system, per the right-hand rule.
**Prime Equinox** — the position in a planemon's orbit when the right ascension of the barymetric center of the system crosses the _ascending node_.
**Obliquity Progression** — an arrow ↑ or ↓ appended to a planemon's obliquity angle indicating whether obliquity is increasing or decreasing.
**Obliquity Envelope** ($\varepsilon_\eta$) — notation of the minimum, mean, and maximum obliquity angles, denoted by

$$
\begin{aligned}
\varepsilon_\eta &:=
\begin{bmatrix}
  \varepsilon_{min} \\
  \varepsilon_{mean} \\
  \varepsilon_{max}
\end{bmatrix}, \text{ or} \\[2ex]
\varepsilon_\eta &:= [\varepsilon_{min}, \varepsilon_{mean}, \varepsilon_{max}]
\end{aligned}
$$

**Obliquity Span** ($\varepsilon_\delta$) — the difference between $\varepsilon_{max} \text{ and } \varepsilon_{min}$
**Obliquity Cycle** ($\varepsilon_\sigma$) — the interval between two occurrences of the same obliquity angle ($\varepsilon$)
**Obliquity Tempo** ($\varepsilon_\tau$) — the rate of change of the Obliquity cycle

$$
\varepsilon_\tau = \dfrac{\varepsilon_{max} - \varepsilon_{min}}{\varepsilon_\sigma}
$$
**Obliquity Magnitude** ($\varepsilon_\rho$) — The ratio of the current obliquity to its maximum value, expressed as a percentage, with an arrow showing whether the trend is increasing $\uparrow$ or decreasing $\downarrow$:

$$
\varepsilon_\rho = \dfrac{\varepsilon}{\varepsilon_{max}}\times 100 \; (\uparrow,\downarrow)
$$
**Secta** (S) — fractions of the orbital perimeter based on orbital speed of the planemon at various points in its orbit.  _Secta_ are _not seasons_.  Seasons occur within secta... they may coincide if the chronostat = the sectastat, but will precess otherwise.
- When you calculate secta, you calculate season lengths, you just have to determine which sectal corresponds to which season by noting the relationship of the chronostat to the sectastat. if you want to make it easy on yourself, set Λ = ζ and Spring is S₀, etc.



