---
project: wmb
phase: 1
module: 1
status: draft
created: <%* tp.file.creation_date("YYYY-MM-DD") %>
updated: <%tp.date.now("YYYY-MM-DD") %>
summary: ""
---
 

# Stellar Parametrics

Stellamons (stars), like duromons, have a basic set of parameters that describe them:
- **Temperature** — How hot is the surface?
	- Absolute measure: Kelvin ($K$)
	- Relative measure: Solar units ($T$)
- **Mass** — How much material is there? ($M$)
- **Luminosity** — How bright is it? ($L$)
- **Radius** — How big is it? ($R$)
- **Lifetime** — How long does it shine? ($Q$)
	- Chiefly relevant to *Main Sequence* stars, particularly stars that are **Solar Cognates**.
- **⊙** — the symbol for the Sun and its defining parameters

> Notes:
> 1. Where we use lower-case letters for the parameters of planemons, we use upper-case letters for stars, so it's easy to tell them apart.
> 2. While **mass** (*m*) is the primary parameter for planemons, with **density** (*ρ*) secondary, for stars **Temperature** (*T*) is the primary parameter, and **radius** (*R*) is secondary.
> 	- While luminosity is **technically derived** from a star's temperature and radius (see *the Stefan-Boltzmann Law*, below), it plays a **central role** in modeling stellar systems — particularly when calculating orbit distances, habitable zones, and irradiance. In practice, it’s often treated as the secondary parameter after termperature.

# The Fusor Continuum

 1.  The spectral class system used throughout this guide — the sequence **O, B, A, F, G, K, M** — is historically rooted in the observational astronomy of the late 19th and early 20th centuries. Its peculiar alphabetical order reflects the evolution of stellar classification from empirical cataloging to physical understanding.

> For readers curious about its origins — including the critical work of [**Annie Jump Cannon**](https://en.wikipedia.org/wiki/Annie_Jump_Cannon), [**Cecilia Payne-Gaposchkin**](https://en.wikipedia.org/wiki/Cecilia_Payne-Gaposchkin), and the less brilliant men who received most of the credit.

2. The spectral classes used in WMB are based on a **linearized temperature model**. This approach smooths over the irregularities of the traditional system to support clean interpolation, symbolic clarity, and consistent orbital modeling.
3. The surface temperature for the Sun used in WMB is $5800$ K; many "official" sources list $5770$ K.
## Spectral Class Table

Here are the spectral classes WMB uses:

$$
\begin{array}{c | r | r}
\textbf{Spectral Class} & \textbf{Min. Temp. (K)} & \text{Max. Temp. (K)} \\
\hline
\textbf{O} & 25000 & 55000 \\
\textbf{B} & 10000 & 25000 \\
\textbf{A} & 7500 & 10000 \\
\textbf{F} & 6000 & 7500 \\
\textbf{G} & 5000 & 6000 \\
\textbf{K} & 3500 & 5000 \\
\textbf{M} & 2400 & 3500 \\
\hline
\textit{Brown Dwarfs} & & \\
\hline
\textbf{L} & 1300 & 2400 \\
\textbf{T} & 600 & 1300 \\
\textbf{Y} & 300 & 600
\end{array}
$$


> Notes:
> - Each range reflects a star's **surface temperature**, typically noted as $T_{\text{eff}}$ in astronomical literature.
> - In WMB:
> 	- **K** = temperature in Kelvin 
> 	- **T** = temperature *relative to the Sun* (i.e., $⊙ = 5800\;K ⇒ T = 1.0$)

## Spectral *Type*
Each spectral class is subdivided into 10 **spectral types**, numbered **0** (hottest) to **9** (coolest).

For example:  
- The Sun, at **5800K**, is classified as a **G2** star —  
	- Spectral **Class: G**  
	- Spectral **Type**: $2$

> ### Note on Spectral Type Precision in WMB
> 
> In this system, a **spectral type** is defined by its **numerical position** within a spectral class.  For example:
> 	- **G2**, **G2.3**, and **G2.9** are all **Type 2** 
> 	- The decimal simply adds interpolation precision — it does **not** define a new type.
> 	- Therefore, **Type 2** refers to the full range (2.0 ·· 2.999···) within class *G*.

This allows for relatively simple mathematical treatment of the relationship between spectral type ($T$) and surface temperature ($K$).

$$
\begin{aligned}
S &= \dfrac{\kappa - K}{þ} \\ \\
\kappa & = S þ + K \\ \\
K &= \kappa - S þ \\ \\
þ &= \dfrac{\kappa - K}{S} \\
\end{aligned}
$$

Where:
- $K$ = the star's surface temperature in Kelvin
- $\kappa$ = the *upper bound* temperature of the relevant spectral class
- $þ$ = the thermal interval constant for the relevant spectral class
- $S$ = the spectral *type* number

> Note that this is a simple linear equation of the form $y = mx+b$.
### The Thermal Interval Constant ($þ$)

Where does $þ$ come from?

For a given spectral class $þ$ can be calculated by:

$$
þ = \dfrac{high\;temp - low\;temp}{10}
$$

Here is the above table with these constants added:

$$
\begin{array}{c | r | r | r}
\textbf{Spectral Class} & \textbf{Min. Temp. (K)} & \textbf{Max. Temp. (K)} & \textbf{TIC (\textit{þ})} \\
\hline
\textbf{O} & 25000 & 55000 & 3000 \\
\textbf{B} & 10000 & 25000 & 1500\\
\textbf{A} & 7500 & 10000 & 250 \\
\textbf{F} & 6000 & 7500 & 150 \\
\textbf{G} & 5000 & 6000 & 100 \\
\textbf{K} & 3500 & 5000 & 150 \\
\textbf{M} & 2400 & 3500 & 110 \\
\hline
\textit{Brown Dwarfs} & & \\
\hline
\textbf{L} & 1300 & 2400 & 110 \\
\textbf{T} & 600 & 1300 & 70 \\
\textbf{Y} & 300 & 600 & 30
\end{array}
$$
#### Example

Let's run the numbers for the Sun
- Known surface temperature: $5800$ K
- Checking the table, $5800$ K falls between $5000$ K and $6000$ K, so the Sun is **spectral class G**
- The high temperature (κ) for spectral class G is κ $6000$ K
- The thermal interval constant (þ) for spectral class G is $þ = 100$
- What is the Sun's spectral type ($S$)?

Running the numbers:

$$
\begin{aligned}
S &= \dfrac{\kappa - K}{þ} \\[1ex]
S &= \dfrac{6000 - 5800}{100} \\[1ex]
S &= \dfrac{200}{100} \\[1ex]
S &= 2\;\checkmark
\end{aligned}
$$
**The Sun is spectral type *G2***.

**Reversing the process:**
- The known spectral class of the Sun is **G**
- The known spectral type of the Sun is $S$ = 2$
- The high temperature ($\kappa$) for spectral class G is $κ = 6000$ K
- The thermal interval constant (þ) for spectral class G is $þ = 100$
- What is the Sun's Kelvin temperature (K)

Running the numbers:

$$
\begin{aligned}
K &= \kappa - S þ \\[1ex]
K &= 6000 - (2)(100) \\[1ex]
K &= 6000 - 200 \\[1ex]
K &= 5800\;✓
\end{aligned}
$$
**The surface temperature of the Sun is *5800K***.

## Converting Between Absolute Kelvin (K) And Solar Relative (T)
Nothing could be simpler:

$$
\begin{aligned}
T &= \dfrac{K}{5800} \\ \\
K &= 5800T
\end{aligned}
$$
For instance: the Sun's surface temperature is $K = 5800$:

$$
T = \dfrac{K}{5800} = \dfrac{5800}{5800} = 1\;\checkmark
$$
Conversely, the Sun's relative temperature is $T = 1.0$:

$$
K = 5800 T = (5800)(1) = 5800\;\checkmark
$$
## Fictional Examples
Let's say we have a star called Essem that we want to be spectral type *F3.65*.  What is its Kelvin temperature?
- The surface temperature for spectral class F is K ∈ ($6000$ ·· $7500$).
- The thermal interval constant for spectral class F is $þ = 150$.

Working through the equation:

$$
\begin{aligned}
K &= \kappa - S þ \\[1ex]
K &= 7500 - (3.65)(150) \\[1ex]
K &= 7500 - 547.5 \\[1ex]
K &= 6952.5\;\checkmark
\end{aligned}
$$
What is Essem's relative surface temperature?

$$
\begin{aligned}
T = \dfrac{K}{5800} \\ \\
T = \dfrac{6952.5}{5800} \\ \\
T = 1.199\;\checkmark
\end{aligned}
$$
**Essem's relative temperature is *T = 1.199*⊙**.

**Working The Other Direction**

Let us say that Essem has a near neighbor, Essel, and we know that its relative temperature is $T = 0.876\odot$.  What is its spectral type?

First, convert $T$ to $K$ by:

$$
K = 5800T = (5800)(0.876) = 5080.8\;\checkmark
$$

Looking at our table we see that this value falls in **spectral class G**:

| Spectral<br>Class | <center>Low<br>Temp.<br>(Kelvin)</center> | <center>High<br>Temp.<br>(Kelvin)</center> | <center>Thermal<br>Interval<br>Constant<br>(þ)</center> |
| :---------------: | ----------------------------------------: | -----------------------------------------: | ------------------------------------------------------: |
|         G         |                                      5000 |                                       6000 |                                                     100 |

… which gives us all the other information we need:

- G-class high temperature is $\kappa = 6000$
- G-class thermal interval constant is $þ = 100$

The spectral type is:

$$
\begin{aligned}
S &= \dfrac{\kappa - K}{þ} \\ \\
S &= \dfrac{6000 - 5080.8}{100} \\ \\
S &= \dfrac{919.2}{100} \\ \\
S &= 9.192\;\checkmark
\end{aligned}
$$
**Essel's spectral type is *G9.192*.**

# Parameter Ranges by Spectral Class

|        | SC →       | <center>O</center> | <center>B</center> | <center>A</center> | <center>F</center> | <center>G</center> | <center>K</center> | <center>M</center> |
| ------ | ---------- | -----------------: | -----------------: | -----------------: | -----------------: | -----------------: | -----------------: | -----------------: |
|        |            |                    |                    |                    |                    |                    |                    |                    |
|        | High       |              55000 |              25000 |              10000 |               7500 |               6000 |               5000 |               3500 |
| Kelvin | Mean       |              40000 |              17500 |               8750 |               6750 |               5500 |               4250 |               2950 |
|        | Low        |              25000 |              10000 |               7500 |               6000 |               5000 |               3500 |               2400 |
|        | TIC¹ (*þ*) |               3000 |               1500 |                250 |                150 |                100 |                150 |                110 |
|        |            |                    |                    |                    |                    |                    |                    |                    |
|        | High       |             9.4828 |             4.3103 |             1.7241 |             1.2931 |             1.0345 |             0.8621 |             0.6034 |
| T⊙     | Mean       |             6.8966 |             3.0172 |             1.5086 |             1.1638 |             0.9483 |             0.7328 |             0.5086 |
|        | Low        |             4.3103 |             1.7241 |             1.2931 |             1.0345 |             0.8621 |             0.6034 |             0.4138 |
|        |            |                    |                    |                    |                    |                    |                    |                    |
|        | High       |            17.0690 |             7.7586 |             3.1034 |             2.3276 |             1.8621 |             1.5517 |             1.0862 |
| R⊙     | Mean       |            12.4138 |             5.4310 |             2.7155 |             2.0948 |             1.7069 |             1.3190 |             0.9155 |
|        | Low        |             7.7586 |             3.1034 |             2.3276 |             1.8621 |             1.5517 |             1.0862 |             0.7448 |
|        |            |                    |                    |                    |                    |                    |                    |                    |
|        | High       |            2.356 M |           20.779 k |            85.1093 |            15.1476 |             3.9709 |             1.3298 |             0.1565 |
| L⊙     | Mean       |          348.608 k |            2.445 k |            38.1967 |             8.0501 |             2.3559 |             0.5015 |             0.0561 |
|        | Low        |           20.779 k |             85.109 |            15.1476 |             3.9709 |             1.3298 |             0.1565 |             0.0163 |
|        |            |                    |                    |                    |                    |                    |                    |                    |
|        | High       |            18.7759 |             8.5345 |             3.4138 |             2.5603 |             2.0483 |             1.7069 |             1.1948 |
| M⊙     | Mean       |            13.6552 |             5.9741 |             2.9871 |             2.3043 |             1.8776 |             1.4509 |             1.0071 |
|        | Low        |             8.5345 |             3.4138 |             2.5603 |             2.0483 |             1.7069 |             1.1948 |             0.8193 |
|        |            |                    |                    |                    |                    |                    |                    |                    |
|        | High       |          64.10E-06 |           4.00E-03 |             0.1280 |             0.4684 |             1.3041 |             4.7336 |            29.3785 |
| Q⊙     | Mean       |           0.67E-03 |          65.64E-03 |             0.2766 |             0.8441 |             2.1003 |            12.4968 |            82.4297 |
|        | Low        |           0.69E-06 |          35.57E-06 |           3.47E-03 |             0.0146 |             0.0447 |             0.1112 |             0.6614 |

¹ Thermal Interval Constant


