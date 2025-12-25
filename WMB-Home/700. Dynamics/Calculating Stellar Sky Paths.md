Sidereal Day: One complete 360° rotation of the planet around its axis relative to the inertial frame.

Sidereal Year: One complete revolution of the planet around its star relative to the inertial frame.

Apical day: The interval between two successive instances of the primary star reaching its highest altitude in the sky (its apex) as observed from a given location on the planet; calculated from the synodic period of the sidereal day and the sidereal year.

Zenithal Year: The apparent length of a year as observed from the equator of the planet, defined as the interval between successive instances of the primary star passing through the zenith (or its equivalent highest point) for an equatorial observer. It is calculated from the synodic period of the apical day and the sidereal year.


## For any obliquity:

- The star’s path traces an **ellipse** on the sky with:
    - **Semi-minor axis** of $\Large \frac{\epsilon}{2}$ (vertical extent); where $\Large \epsilon$ = the axial obliquity of the planet.
    - **Major axis** of $\large 180^\circ$ (azimuthal extent).
- Whether the star's full path lies above the horizon depends on the observer’s **latitude ($\phi$)** and the star’s **declination ($\delta$)**.

---

### **Workflow for Calculating Stellar Path Parameters**

#### **Step 1: Input**
- **Obliquity ($\epsilon$)**: The planet’s axial tilt.
- **Latitude ($\phi$)**: Observer’s latitude.
- **Fraction of the zenithal year ($Z_f$)**: Time since the northern hemisphere summer solstice, as a fraction of the total zenithal year ($Z$).

---

#### **Step 2: Calculate the Fraction of the Zenithal Year ($Z_f$)**

1. **What is $Z$?**
   - $Z$ is the total length of the planet’s zenithal year (one full cycle of the star's declination).

2. **Standard Reference Points for $Z_f$:**
   - $Z_f = 0$: Northern hemisphere **summer solstice**.
   - $Z_f = 0.25Z$: Northern hemisphere **autumnal equinox**.
   - $Z_f = 0.5Z$: Northern hemisphere **winter solstice**.
   - $Z_f = 0.75Z$: Northern hemisphere **vernal equinox**.
   - $Z_f = Z$: Northern hemisphere **summer solstice** (completing one full zenithal year).

3. **How to Calculate $Z_f$:**
   If the current day of the zenithal year is known ($t_\text{current}$), calculate $Z_f$ as:
   $$
   Z_f = \frac{t_\text{current}}{Z}
   $$
   ...where:
   - $t_\text{current}$ is the number of days (or time fraction) since the summer solstice.
   - $Z$ is the total length of the zenithal year.

---

#### **Step 3: Calculate Star’s Declination**
The star’s declination varies sinusoidally over the zenithal year:
$$
\delta = \epsilon \cos\left(2 \pi Z_f\right)
$$

---

#### **Step 4: Calculate Maximum and Minimum Altitudes**
1. **Maximum Altitude ($h_\text{max}$):**
   $$
   h_\text{max} = 90^\circ - |\phi - \delta|
   $$

2. **Minimum Altitude ($h_\text{min}$):**
   $$
   h_\text{min} = 90^\circ - |\phi + \delta|
   $$

---

#### **Step 5: Conditional Check**
- **If $h_\text{max} > 0^\circ$ and $h_\text{min} < 0^\circ$:**
    - The star's path intersects the horizon. **Proceed to Step 6**.
- **Otherwise, STOP:**
    - If $h_\text{min} > 0^\circ$: The star never dips below the horizon (continuous daylight).
    - If $h_\text{max} \leq 0^\circ$: The star never rises above the horizon (continuous night).

---

#### **Step 6: Calculate Center Offset ($c$)**
If the conditional in Step 5 is satisfied:
$$
c = 90^\circ - \frac{|\phi - \delta| + |\phi + \delta|}{2}
$$

---

#### **Step 7: Calculate Azimuthal Intersections**
For the star’s path intersections with the horizon ($y = 0^\circ$):
$$
x = \pm a \sqrt{1 - \frac{c^2}{b^2}}
$$
...where:
- $a = 180^\circ$ (semi-major axis, azimuthal extent),
- $b = \frac{\epsilon}{2}$ (semi-minor axis, vertical extent).

---

