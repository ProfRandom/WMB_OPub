---
project: wmb
phase: 1
module: 1
status: draft
created:
updated: 2025-12-25
summary: ""
---
## Roche Limit

The **Roche Limit** marks the distance from a massive primaron at which the tidal gradient across a secondron body equals the secondron’s own gravitational cohesion.  Inside this limit, a self-gravitating satellite can no longer remain intact; it is tidally disrupted into fragments or rings.

For a rigid satellite of density $\rho_s$ orbiting a primaron of density $\rho_p$ and radius $R_p$:

$$
R_r \approx 2.44\,R_p
\left(
  \frac{\rho_p}{\rho_s}
\right)^{\!\tfrac{1}{3}}
$$
Where:
- $R_r$ = Roche Limit radius (measured from the primaron’s center)  
- $R_p$ = primaron’s radius  
- $\rho_p$ = primaron’s mean density  
- $\rho_s$ = satellite’s mean density  

> **Rule of thumb:** Fluid bodies (like icy moons) are disrupted near $\sim 2.5\,R_p$, while rigid, rocky bodies survive slightly closer (~1.5 – 2 $R_p$).

### Relation to Roche Lobe and Hill Sphere
$$
\begin{array}{lll}
\textbf{Regime} & \textbf{Controlling Effect} & \textbf{Outcome} \\
\hline
\text{Roche Lobe} & \text{Gravitational balance between companions} & \text{Mass exchange} \\
\text{Roche Limit} & \text{Tidal sheer exceeds self-gravity} & \text{Body disruption} \\
\text{Hill Sphere} & \text{Self-gravity exceeds external tides} & \text{Stable satellite region}
\end{array}
$$ 
## Roche Lobe Geometry
When two stellar bodies share a gravitational system, each defines a **Roche lobe**—the three-dimensional region around it within which orbiting material remains gravitationally bound to that star. Beyond this boundary, the gravitational influence of the companion star dominates. 

Material that crosses the inner point of contact between the lobes (the **inner Lagrange point**, $L_1$) can transfer from one star to the other, a process central to the dynamics of close-binaries and mass-transfer systems.

### Semi-Detached and Contact Binaries
When the Roche lobes **touch** (or one star even slightly *overflows* its own lobe and spills material through $L_1$, the system becomes what’s called a **contact binary** — or, if only one star fills its lobe, a **semi-detached binary**.

### Binary Configurations

- **Detached Binary**  
  - *Roche-Lobe Status:* Both stars are well within their Roche lobes.  
  - *Description:* No mass transfer occurs; each star evolves independently under its own gravity.  
  - *Example:* Most wide binary systems.

- **Semi-Detached Binary**  
  - *Roche-Lobe Status:* One star fills (or nearly fills) its Roche lobe; the other remains detached.  
  - *Description:* The donor star transfers mass through $L_1$ onto its companion, often forming an accretion disk. 
  - *Example:* Algol-type systems.

- **Contact Binary**  
  - *Roche-Lobe Status:* Both stars fill or slightly overflow their Roche lobes, sharing a common envelope.  
  - *Description:* The stars exchange mass and energy directly through $L_1$; the system behaves like a single, distorted body.  
  - *Example:* W Ursae Majoris-type systems.

## Eggleton’s Approximation of Roche Lobe Radii

For practical modeling, the Roche-lobe radius ($R_L$) can be approximated by the empirical fit derived by **Eggleton (1983)**. Expressed in a general form:

$$
\begin{aligned}
\text{Define: }&\quad
f(x) =
\frac{0.49\,x^{\tfrac{2}{3}}}
 {0.6\,x^{\tfrac{2}{3}} +
	 \ln\!\left(1 + x^{\tfrac{1}{3}}\right)
	 } \\[1em]
\text{Roche Lobe $M_1$:}&\quad R_{L,1} = A\,
	f\!\left(\frac{M_1}{M_2}\right) \\[1em]
\text{Roche Lobe $M_2$:}&\quad R_{L,2} = A\,
	f\!\left(\frac{M_2}{M_1}\right)
\end{aligned}
$$
Where:
- $A$ = average separation of the binary stars (in AU) 
- $M_1,\,M_2$ = stellar masses (in solar units) 
- $f(x)$ = dimensionless scaling function describing the fractional Roche-lobe radius 

#### Interpretation
- $R_{L,1}$ and $R_{L,2}$ give the **effective radii** of each star’s gravitational domain within the binary system. 
- Because $f(x)$ is not symmetric, the two lobes differ in size unless $M_1 = M_2$. 
- When $M_1 = M_2$, both lobes have equal volumes and share a common boundary at $L_1$. 
- For unequal masses, the lower-mass star has the *larger fractional lobe* (a smaller star but a larger gravitational domain relative to its own mass). 

#### Practical Rule of Thumb
For typical mass ratios in close binaries ($0.2 \le \frac{M_2}{M_1} \le 5$), Eggleton’s formula is accurate to within 1% — far more than sufficient for system-design or orbit-stability work in WCB. 


***
Tag Core
#ontics #math  #orbits #barycentrics #time 