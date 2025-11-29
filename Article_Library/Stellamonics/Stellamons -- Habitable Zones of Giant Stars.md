---
project: wmb
phase: 1
module: 1
status: draft
created: <%* tp.file.creation_date("YYYY-MM-DD") %>
updated: <%tp.date.now("YYYY-MM-DD") %>
summary: ""
---
 

# 'Habitable Zones' of Giant Stars

Remember that although the habitable zone limits are *calculated* using the luminosity of the star, they are *measured* in distance from its **center of mass**. Thus, a giant star like Aldebaran, with a radius of $44.2$⊙ and a luminosity of $439$⊙, will have much larger fundamental orbits than the Sun.

## Stellar Radius Is a Significant Factor

Aldebaran's radius is the Sun's radius of $695,700$ km $\times 44.2 = 30,749,940$ km. One astronomical unit is $149.6$ million kilometers, which means that Aldebaran's radius alone measures $0.206$ astronomical units.

Thus, were Aldebaran to replace the Sun in the Solar system, its surface would fall only about $0.181$ AU, which is a mere ≈ $27$ million km inside *Mercury's orbit*.

> [!important]
> Aldebaran’s true mass is measured at $1.16 M⊙$​.  If, however, we incorrectly applied the main-sequence radius–mass scaling, we’d get $M \approx 67.34⊙$.  The main-sequence [[Stellamons -- Stars and Spectral Classes|luminosity–mass scaling]] would give $M \approx 4.959⊙$​. Both are wildly wrong — illustrating why Main Sequence relations must only be applied to Main Sequence stars; using them on evolved stars like Aldebaran gives wildly misleading results.

Using Aldebaran's correct (measured) mass value, its perannual orbit falls at $P =\sqrt[3]{1.16} = 1.051$ AU, which is only $0.845$ AU (1.26 million kilometers) beyond the star’s surface.

Aldebaran’s habitable zone limits and nucleal orbit calculate to be:

$$
\begin{aligned}
H_0 = 0.500\sqrt{439} = 10.476 \\[1ex]
H_1 = 0.750\sqrt{439} = 15.714 \\[1ex]
H_2 = 0.950\sqrt{439} = 19.905 \\[1ex]
N = \sqrt{439} = 20.952 \\[1ex]
H_3 = 1.385\sqrt{439} = 29.019 \\[1ex]
H_4 = 1.770\sqrt{439} = 37.086 \\[1ex]
H_5 = 4.850\sqrt{439} = 101.619 \\[1ex]
\end{aligned}
$$
The orbital period of the nucleal orbit is:

$$
N_p = \sqrt{\dfrac{20.952^3}{1.16}} = \sqrt{\dfrac{9197.94}{1.16}} = \sqrt{7929} = 89.05 \text{ years}
$$
… or about $54\%$ of Neptune's orbital period.

## Extending Into The Supergiant Realm

The theoretical maximum mass for a star is $300$ M⊙.  We can't use the standard $L=M^{3.8}$ equation for stars above about $20$ M⊙, so we have to choose the *lesser* between:

$$
\begin{aligned}
L &= k \times M^{1.5}\;, \text{where } k=1.12 \times10^3 \\[1em]
&\text{or} \\
L_{Edd} &= 3.2 \times 10^4 \left(\dfrac{M_*}{M_⊙}\right)L\odot \quad \text{(The Eddington Limit)} 
\end{aligned}
$$
In our case the equations return:

$$
\begin{aligned}
L_{MS} &= (1.12 \times 10^3) \times (300^{1.5}) = (1.12 \times 10^3) \times (5.196 \times 10^3) = 5.82 \times 10^6 \\[1em]
&\text{and} \\
L_{Edd} &= 3.2 \times 10^4 \left(\dfrac{300}{1}\right)L⊙ = 9.6 \times 10^6
\end{aligned}
$$
… so we'd go with the $L_{MS}$ value, and calculate the thermozone limits by:

$$
\begin{aligned}
H_0 &= 0.500\sqrt{5.82 \times 10^6} = 1205.23 \\[1ex]
H_1 &= 0.750\sqrt{5.82 \times 10^6} = 1809.35 \\[1ex]
H_2 &= 0.950\sqrt{5.82 \times 10^6} = 2291.84 \\[1ex]
N &= \sqrt{5.82 \times 10^6} = 2412.47 \\[1ex]
H_3 &= 1.385\sqrt{5.82 \times 10^6} = 3341.27 \\[1ex]
H_4 &= 1.770\sqrt{5.82 \times 10^6} = 4270.07 \\[1ex]
H_5 &= 4.850\sqrt{5.82 \times 10^6} = 11700.47 \quad \text{(almost 19\% of a lightyear)} \\
\end{aligned}
$$
… but a perannual orbit of only

$$
P = \sqrt[3]{M} = \sqrt[3]{300} = 6.694\;\text{AU}
$$
… which is **$17.31$ AU _inside_** the minimum estimated $24$ AU radius of such a star.

## Working With a Known Star

The largest known star currently is Stephenson 2-18, with a radius of $R = 2150⊙\;(9.999AU)$, a measured luminosity of $L = 440000⊙$, and an upper estimated mass value of $M = 45⊙$. These values yield thermozone limits of:

$$
\begin{aligned}
H_0 &= 0.500\sqrt{440000} = 331.66 \\[1ex]
H_1 &= 0.750\sqrt{440000} = 497.49 \\[1ex]
H_2 &= 0.950\sqrt{440000} = 630.16 \\[1ex]
N &= \sqrt{440000} = 663.32 \\[1ex]
H_3 &= 1.385\sqrt{440000} = 918.71 \\[1ex]
H_4 &= 1.770\sqrt{440000} = 1174.09 \\[1ex]
H_5 &= 4.850\sqrt{440000} = 3217.13 \\[1ex]
\end{aligned}
$$
… and a perannual orbit of:

$$
P = \sqrt[3]{M} = \sqrt[3]{45} = 3.557\;\text{AU}
$$
… $6.442$ AU *inside* the radius of the star.

>Remember:
>Such hypergiants live only a few million years at most, far too short for Terran-like biospheres to develop. (See [[Stellamons -- Lifetime, Life, and Habitability]] for details.)

## Conclusion
You *can* calculate thermozones (and hence orbital architectures) for giant and supergiant stars, but their immense radii, unstable envelopes, and short lifespans mean those thermozones don’t correspond to genuinely *habitable real estate.* In Protagorean terms, they fail the human-centered test: such systems are not *Terran-hospitable*, though they may be *mathematically parahabitable* —that is, capable of hosting planets that humans could *use* (for energy, staging, or resource acquisition) without being worlds where Terran-like life would be expected to evolve. (Of course, whether truly alien **xenotics** might arise under such extreme conditions is another matter entirely.)
