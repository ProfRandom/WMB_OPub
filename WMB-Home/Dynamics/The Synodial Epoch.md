---
project: wmb
phase: 1
module: 1
status: draft
created:
updated: 2025-12-25
summary: ""
---

## The Synodial Epoch

The *synodial epoch* ($Y$) is the time interval after which a synodion occurs at the base angle $B^\theta$ agin, completing a full cycle.

The *epochal aggregate* ($Y_0$) is the total number of synodia that transpire within a synodial epoch.

Whereas we used the synodic formula:

$$
\begin{aligned}
\Sigma &= \dfrac{P_\alpha \times P_\beta}{|P_\alpha - P_\beta|} \\
\end{aligned}
$$
to calculate the synodic period, we need to use a different method to calculate the Epochal Aggregate; we employ both the *Least Common Multiple* (LCM) and the *Greatest Common Divisor* (GCD):

$$
LCM(a, b) = \dfrac{a \times b}{GCD(a, b)}
$$
>❗️Important ❗️
>1. Most modern calculators, spreadsheets, and programming languages have built-in functions for calculating both LCM and GCD, but be aware that *both of these can only be correctly calculated for integer inputs*.  If something like LCM(1.5, 3.3) returns a value rather than an error, it will likely be the LCM of 1 and 3, not of 1.5 and 3.3.
>2. The GCD *can* be calculated by hand using the *Euclidean Algorithm* (detailed elsewhere), calculators, spreadsheets, or programmed scripts are much faster.

We need to calculate the LCM of $P_\alpha = 24.36$ and $P_\beta = 11.72$, but neither of these are integers, so we *normalize* them by multiplying by the factor of ten which will render the more precise of the two into an integer value.  In this case, both have two decimal places of precision, so multiplying by $10^2 = 100$ will be sufficient:

$$
P'_\alpha = 24.36 \times 100 = 2436 \quad \text{and} \quad P'_\beta = 11.72 \times 100 = 1172
$$
Now we can compute the LCM by:

$$
\begin{aligned}
\begin{split}
LCM(a, b) &= \dfrac{a \times b}{GCD(a, b)} \\[0.5em]
&= \dfrac{2436 \times 1172}{GCD(2436, 1172)} \\[0.5em]
&= \dfrac{2854992}{4} \\
&= 713748\; ✓
\end{split}
\end{aligned}
$$
Now, *since we normalized our inputs* by scaling up by a factor of $10^2 = 100$, we need to scale this result *down* by the same factor:

$$
Y_0 = \dfrac{713748}{100} = 7137.48\; \text{days } ✓
$$
The *epochal interval* ($\Psi$) is calculated by dividing the Epochal Aggregate ($Y_0$) by the synodic period ($\Sigma$):

$$
\begin{aligned}
\begin{split}
\Psi &= \dfrac{Y_0}{\Sigma} \\[0.5em]
&= \dfrac{7137.48}{22.587} \\[0.5em]
&= 316\; \text{synodia}
\end{split}
\end{aligned}
$$
This reveals that $T_{316}$ occurs in the same configuration at the base angle $B^\theta$.  We can double-check by supplying $S=316$ to our synodian instance angle ($\widehat{\Theta}$) equation:

$$
\begin{aligned}
\begin{split}
\widehat{\Theta} &= 360^\circ - MOD((S \times \Lambda_\Theta), 360^\circ) \\
&= 360^\circ - MOD((316 \times 26.203^\circ), 360^\circ) \\
&= 360^\circ - 360^\circ \\
&= 0\; ✓
\end{split}
\end{aligned}
$$
To convert the epochal aggregate $\Psi = 7137.48$ days into something more useful, we can divide by the number of days in a sidereal year ($≈ 365.2564$):

$$
Y_0^y = \dfrac{7137.48}{365.2564} = 19.54\; \text{years }✓
$$
… which is about

$$
19^y\;197^d\;11^h\;16^m\;20.724^s
$$
give-or-take a millisecond.

### Quarter Synodial Epoch

#### The Where
A quarter synodial epoch ($Y_{/4}$) is an important quantity, as well; at these intervals, synodoi occur precisely on a cardinal angle ($90^\circ, 180^\circ, 270^\circ$) in succession.  We call these the *cardinal synodoi*.  They occur, of course every one fourth of the synodion:

$$
Y_{/4} = \dfrac{Y_0}{4}
$$
In our worked example above, the quarter synodial epoch is:

$$
\begin{aligned}
Y_{/4} = \dfrac{Y_0}{4} = \dfrac{7137.48}{4} = 1784.37\; \text{days} \\[0.5em]
Y_{/4}^y = \dfrac{Y_{/4}}{365.2564} = \dfrac{1784.37}{365.2564} ≈ 4.89\; \text{years}
\end{aligned}
$$
### Quarter Epochal Interval
Similarly, a *quarter epochal interval* ($\Psi_{/4}$) is the number of *common synodoi* that occur between cardinal synodoi:

$$
\Psi_{/4} = \dfrac{\Psi_0}{4} = \dfrac{316}{4} = 79\; \text{synodoi}
$$
### The Epochal Complements
There are two of these, the *epochal major complement* ($Y_\alpha$) and the *epochal minor complement* ($Y_\beta$), which are the number of complete orbits of orbiton $M_\alpha$ and $M_\beta$, respectively, per each synodial epoch:

$$
\begin{aligned}
Y_\alpha &= \dfrac{Y_0}{P_\alpha} \\[1em]
Y_\beta &= \dfrac{Y_0}{P_\beta}
\end{aligned}
$$
In our worked example above:

$$
\begin{aligned}
Y_\alpha &= \dfrac{Y_0}{P_\alpha} = \dfrac{7137.48}{24.36} = 293\; \text{orbits }✓ \\[1em]
Y_\beta &= \dfrac{Y_0}{P_\beta} = \dfrac{7137.48}{11.72} = 609\; \text{orbits }✓
\end{aligned}
$$

[^1]: While the notation ²/₁ is notationally equivalent to 2 : 1, we use the colon format exclusively.

[^2]: literally, "having a common measure"; the orbit of one can't be expressed by a whole number or rational fraction of the other's.
 
***
Tag Core
#time #orbits 