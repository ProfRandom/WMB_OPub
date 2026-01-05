---
project: wmb
phase: 1
module: 1
status: draft
created: 2025-11-28
updated: 2025-11-28
summary: ""
realm: logos
---
# The Distance Modulus

And _this_ is where the distances to the stars comes back into the story.  **Apparent magnitude** and **Absolute Magnitude** are related by a relationship called _the distance modulus_, mathematically expressed as:

$$
m - M = 5\;log_{10}(d) - 5
$$

Where $d$ is the distance to the star in _parsecs_.

So, a star's **Absolute magnitude** is how bright the star would appear to us if it were exactly $10$ parsecs away.  This is less straighforward than the simple inverse-square law that governs apparent brightness for _local_ observers, and might not really be that useful, unless you're wanting to know how bright your star would appear to someone looking at it from a significant distance away from your star system.
### Magnitude and Luminosity

The general equation relating **absolute magnitude** ($M$) to stellar luminosity in stellar units is:

$$
M = M\!⊙ - 2.5\; log_{10}(L)
$$

Where:
- $L$ = the star's luminosity in solar units.

Plugging in the Sun's absolute magnitude value $M=4.83$:

$$
M = 4.83 - 2.5\; log_{10}(L)
$$

… and rearranging:

$$
4.83 = -2.5\;log_{10}(C)
$$

… and solving for C:

$$
C = 10^{-\frac{4.83}{2.5}} \approx 0.01169
$$

… and rearranging again:

$$
M = -2.5\;log_{10}(0.01169L)
$$

Where:

- $L$ = the luminosity of the star in solar units.

… the inverse of which is:

$$
L = 85.5432 \times 2.512^{-M}
$$

Where:

- $M$ = the star's absolute magnitude.

This gives us a rough approximation of any star's absolute magnitude and we can use the **distance modulus** to calculate an apparent magnitude from that.


***
Tag Core
#stellamonics #ontics  #math

