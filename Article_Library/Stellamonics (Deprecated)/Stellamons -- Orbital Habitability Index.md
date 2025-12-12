---
project: wmb
phase: 1
module: 1
status: draft
created: <%* tp.file.creation_date("YYYY-MM-DD") %>
updated: <%tp.date.now("YYYY-MM-DD") %>
summary: ""
---
 

# Orbital Habitability Index (OHI)

The Orbital Habitability Index (OHI) is a measure of how likely a planemon is to be habitable based on its orbit, with the nucleal orbit assumed to be 100% habitable and orbits closer-in and farther-out becoming progressively less habitable. It is calculated using one of two equations, depending on whether the orbit in question is *intranucleal* or *extranucleal*:

The OHI provides a scalar measure $(0.00 ·· 1.00)$ of the *relative biological viability* of a planemon orbit based on its distance from the nucleal orbit $N = \sqrt{L}$​. It assumes a peak habitability of $1.00$ ($100$%) at $1.000N$, declining linearly in each direction.

$$
H_I =
\begin{cases}
 \quad 2\dfrac{D}{N} - 1 & \text{if } {D} ≤ {N} \quad \text{(intranucleal)} \\[1em]
 -0.26\dfrac{D}{N} + 1.26 & \text{if } {D} > {N} \quad \text{(extranucleal)}
\end{cases}
\text{Where } R = \dfrac{D}{N}: \quad H_I =
\begin{cases}
 \quad 2R - 1 & \text{if } R ≤ 1 \quad \text{(intranucleal)} \\
 -0.26R + 1.26 & \text{if } R > 1 \quad \text{(extranucleal)}
\end{cases}
$$

Where:
- $H_I$ = the numeric value of the orbit's habitability index
- *$D$* = the orbit's distance in AU
- $N$ = the nucleal orbit's distance in AU

Values of $D < 0.500N$ and $> 4.850N$ return *negative numbers* for $H_I$, indicating that the orbit is not hospitable, habitable, or parahabitable for Earth-type lifeforms.

| Orbit<br>Type | Orbit<br>Distance | Habitability<br>Index |
| :-----------: | :---------------: | :-------------------: |
| Intranucleal  |     0.500$N$      |         0.00          |
| Intranucleal  |     0.750$N$      |         0.50          |
| Intranucleal  |     0.950$N$      |         0.90          |
|    Nucleal    |     1.000$N$      |         1.00          |
| Extranucleal  |     1.385$N$      |         0.90          |
| Extranucleal  |     1.770$N$      |         0.80          |
| Extranucleal  |     4.850$N$      |         0.00          |

