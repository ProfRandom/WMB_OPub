---
title: Stellamons -- Lifetime and Habitability
tags:
  - stars
  - stellamon
  - lifetime
  - habitability
---
# Stellamon Lifetimes By Spectral Class

$$
\begin{array}{c | r | r}
\textbf{Spectral Class} & \textbf{Min. Lifetime} & \textbf{Max. Lifetime} \\
\hline
\textbf{O} & 130.41 \text{ ka} & 3.18 \text{ Ma} \\
\textbf{B} & 3.18 \text{ Ma} & 326.33 \text{ Ma} \\
\textbf{A} & 326.33 \text{ Ma} & 2.36 \text{ Ga} \\
\textbf{F} & 2.36 \text{ Ga} & 7.46 \text{ Ga} \\
\textbf{G} & 7.46 \text{ Ga} & 19.02 \text{ Ga} \\
\textbf{K} & 19.02 \text{ Ga} & 101.32 \text{ Ga} \\
\textbf{M} & 101.32 \text{ Ga} & 658.83 \text{ Ga} 
\end{array}
$$

# Stellamon Lifetimes and System Habitability

[Margaret Turnbull and Jill Tartar](https://ui.adsabs.harvard.edu/abs/2003ApJS..145..181T/abstract) have listed some criteria that stars would need to have in order to be what they call a “habstar” — one likely to have an Earth-like planet orbiting it.  Among their criteria, they list that the star should:
1. Be on the Main Sequence;
2. Be non-variable;
3. Have a habitable zone;
4. ***Be at least 3 billion years of age***.

This last criterion is critical (for our purposes perhaps the most important), because it automatically disqualifies any star which has a main sequence lifetime of $Q < 3.0$ Ga. This means that a “habitable star” needs to have a current age of *no less* than 65% that of the Sun, and a total Main Sequence lifetime of *at leas*t 30% that of the Sun ($3.0$ Ga; $0.300$⊙).
## Identifying A Maximum Spectral Class

For a star with $Q = 3.0⊙$, using our [[Stellamons -- Equations of State|Main Sequence Stellar Equations of State]]:

We can approximate a relative temperature of:

$$
T = Q^{-0.2} = 0.3^{-0.2} = 1.272⊙
$$
… which is a Kelvin temperature of:

$$
K = 5800T \approx 7379
$$

This Kelvin temperature falls into the **F-Class** range, which has a TIC of $þ = 150$.

Applying our [[Stellamons -- Equations of State|Spectral Class]] calculation from Kelvin temperature:

$$
\begin{aligned}
S &= \dfrac{\kappa - K}{þ} \\ \\
 &= \dfrac{7500 - 7379}{150} \\ \\
 &= \dfrac{121}{150} \\ \\
S &= 0.807 \\ \\
\end{aligned}
$$
So, no Main Sequence star above spectral type **F0.81** will have *total Main Sequence lifetime* long enough to qualify as *habitable*.

Since we have specified that the spectral type range for stars with perannual orbits within the parahabitable zone, and since **F2** is *later* on the spectral class continuum than **F0.81**, we know that all stars defined as *solar analogs* have lifetimes long enough to be *habitable* system hosts.
# Relating Stellamon Ages to Appearance and Evolution of Life

The earliest fossils of complex multicellular life appear about **$600$ million years ago**, and the earliest fossils widely accepted as animals are from the phylum [*Cnidaria*](https://en.wikipedia.org/wiki/Cnidaria#Fossil_record. ) — marine species that show up in the record around **$580$ million years ago** during the late Ediacaran, just before the Cambrian Explosion. Taking the accepted age of the Earth as **$4.56$ billion years**, this means Earth was about **4.0 billion years old** (~$88$% of its present age) before complex life began to appear.

If we assume a similar pace of biological development for complex life on other Earth-like exoplanets, then any star with a main sequence lifetime of **≤ $3.0$ billion years** would leave its habitable planets without enough time for complex life to evolve indigenously — ending its stable phase at least a billion years too soon. (This does not preclude such worlds from supporting transplanted or migratory complex life.)

On the other hand, the [**Great Oxygenation Event**](https://en.wikipedia.org/wiki/Great_Oxygenation_Event) — which shifted Earth’s atmosphere from one dominated by carbon dioxide and methane to one with persistent oxygen levels above ~$15$% — occurred around **$2.4$ billion years ago**, when Earth was roughly **$2.16$ billion years old** (~$47$% of its current age). The gap between that oxygenation and the first appearance of complex animals was thus about **$1.8$ billion years**. This suggests that, in principle, complex life *could* arise at any time after oxygenation, but on Earth the delay was geologically long.

For our purposes, we can specify that an Earth-analog planet must be at least **~$2.0$ billion years old** to have plausibly developed an aerobic atmosphere by biological means, and at least **~$4.0$ billion years old** to have produced indigenous complex life. The **minimum** planetary age for being (in)habitable to human colonists is therefore the lesser of these: **~$2.0$ billion years**.

A star with a main sequence lifetime of **$3.0$ billion years** could host an Earth-analog planet that had time to produce an oxygenated atmosphere, and then remain stable for roughly another **$1$ billion years** before leaving the main sequence. Such a system could be colonized by humans or other oxygen-breathing life, even if indigenous complexity had not yet evolved. The next step is to determine which spectral classes meet this **$≥ 3$ Ga** lifetime criterion.