---
title: Stellamons -- Magnitude and the Distance Modulus
tags:
  - stars
  - stellamon
  - magnitude
  - absolute_magnitude
  - apparent_magnitude
  - luminosity
---
# Stellar Magnitude and The Distance Modulus
You've probably encountered the term *magnitude* in relation to stars before, perhaps even heard mention of the two types: *absolute magnitude (M)* and *apparent magnitude (m)*. Simply put, a star's **absolute magnitude** is how visibly bright it actually is, and its **apparent magnitude** is how bright it appears.
## The History of Magnitudes

### Apparent Magnitude

^ebce43

Early astronomers had to rely on the best equipment they could obtain — their own eyes. So, magnitudes were originally determined by how faint a star appeared in the sky, and, yes, it *was* a woefully subjective system, but it was all they had to work with. The system was formalized by Hipparchus, along with Claudius Ptolemy, in the Second Century BCE.

The most visible (brightest) stars were given a (visual) magnitude of $1$; magnitude $2$ stars were dimmer than magnitude $1$ stars, magnitude $3$ dimmer still, and so on.. Magnitude $6$ stars were those just barely bright enough to be seen with the naked eye.

>Note that this is based on ideal viewing conditions... dark sky, no full moon, no clouds, etc.
>- For modern people looking up under a suburban sky, the best they're likely to be able to see is around magnitude $4.5 – 5$
>- City dwellers will be lucky to see stars of magnitude $3$.
>
>In fact, in 1994, the city of Los Angeles experienced a major power outage as a result of the Northridge earthquake. The lack of *light pollution* gave residents a view of the night sky they were unfamiliar with, which included the Milky Way (our own galaxy) glowing overhead. Observatories such as the one in Griffith Park, reported receiving calls from curious — and sometimes alarmed — residents, enquiring what the strange glowing cloud above was.

You'll notice that, astronomers being astronomers, these numbers also run *backward* — the higher the magnitude, the dimmer the star (or any object for that matter), so, yes, you will encounter *negative magnitudes* for those objects that are brighter than the brightest stars; the Full Moon, for instance has an apparent magnitude of $-12.9$ on this scale, and the planet, Venus, has an apparent magnitude of $-4.7$ at its brightest in Earth's sky.

Later astronomers — *much later*, in fact more than *$2000 $years later* — made the system mathematical, on a logarithmic scale. This means that in the modern system, a magnitude $2$ star is $2.512$ times dimmer than a magnitude $1$ star.

> **Why 2.512?

When modern astronomer Norman Robert Pogson (1829 – 1891), decided to *mathematize* Hipparchus subjective scale, he didn't want to rewrite literally thousands of years of astronomical documents to re-categorize stars, so, he had to stick with the $1 – 6$ scale Hipparchus had established. This means that there's a difference of $6 - 1 = 5$ steps between the dimmest and the brightest stars.

*Fortunately*, by measurement, the **brightness** difference between first and sixth magnitude stars is about a factor of $100$. So, $5$ steps in magnitude = $100×$ in brightness; therefore the difference between each single step in the sequence is:

$$
d = \sqrt[5]{100} \approx 2.5118864
$$

… which is rounded to $2.512$ for convenience. Practically speaking, one can simply remember that a magnitude $3$ star is $2.5×$ brighter than a magnitude $4$ star.
# Apparent Brightness

^3c5de0

How bright something that shines *is* and how bright it *appears* to an observer is a function of distance. The absolute apparent brightness can be calculated by:

$$
B_A = \dfrac{L_W}{4 \pi d^2}
$$
Where:
- $B_A$ = apparent brightness (flux, in Watts/m²)
- $L_W$ = luminosity of the star
- d = distance between the star and the observer in meters

This is a useful equation in general astrophysics, but it is less accessible for thesiastics, because one has to know the actual luminosity of the star in watts, which is not always an easy number to look up — and even harder to calculate. Also, distance in *meters*? Do you know how fast those numbers get *insanely large*?

## Relative Apparent Brightness
Here is a more useful equation for thesiastics:

$$
B_{A⊙} = \dfrac{L}{D^2}
$$
Where:
- $B_A$ = the apparent brightness of the star *in solar units*
- $L$ = the luminosity of the star *in solar units*
- $D$ = the distance to the star in AU (i.e. the semi-major axis of the planemon's orbit)

>Note that this is the same form as the *inverse-square law*. The amount of energy (of *any kind*) detectable from a radiating object decreases with the square of the distance of the observer from that object. If your campfire feels a certain intensity where you're standing, and you move twice as far away, the intensity will feel less by the inverse-square of the distance you've moved. Since you're now twice as far away as you were

$$
E = \dfrac{1}{2^2} = \dfrac{1}{4}
$$
… one-fourth as much as before.

### Example 1: How Bright Does The Sun Appear From Mars?
Since we're talking about the Sun, here, $L = 1$. The distance is Mars' orbital semi-major axis, $D = 1.524$ AU:

$$
B_{A⊙} = \dfrac{L}{D^2} = \dfrac{1}{1.524^2} = \dfrac{1}{2.323} = 0.431
$$
So, the sun is about 43% as bright seen from Mars as it is seen from Earth.

### Example 2
Let's imagine a star called Kalveru which has a luminosity $L=1.618$⊙. How bright would it appear to an observer on a planet 1 AU away? Here, the luminosity is what varies not the distance, so our equation becomes:

$$
B_{A⊙} = \dfrac{L}{D^2} = \dfrac{1.618}{1^2} = \dfrac{1.618}{1} = 1.618
$$
So, the apparent brightness in solar units of any star when viewed from 1 AU away is simply the relative luminosity of the star in solar units.

$$
\text{When}\quad D = 1, \quad B_{A⊙} = L⊙
$$
Now, let's put a planet (Dynon) in orbit around Kalveru at $D = 1.524$ AU. How bright does Kalveru appear from Dynon?

$$
B_{A⊙} = \dfrac{L}{D^2} = \dfrac{1.618}{1.524^2} = \dfrac{1.618}{2.323} = 0.697
$$
So, Kalveru appears about 70% as bright from Dynon as the Sun does from Earth.

| Planemon Type | Estimated Albedo (A) |
| --------------------------- | -------------------- |
| Snowball planemon | ⟨0.6 ∧ 0.8⟩ |
| Cloudy temperate Earthlike | ⟨0.25 ∧ 0.35⟩ |
| Rocky desert world | ⟨0.15 ∧ 0.25⟩ |
| Ocean planemon (few clouds) | ⟨0.05 ..0.15⟩ |
| Thick sulfur clouds (Venus) | ~0.75 |
### Absolute Magnitude

As with [[#^3c5de0|apparent brightness]], however a star's magnitude is dependent on its distance from the observer, and once it became clear to astronomers that different stars were different distances away, the question naturally arose: *How bright are they, **really**, then?*
### Vega, The 'Standard Candle'

The star α-Lyrae, popularly known as Vega, acts as the standard candle for absolute magnitudes, because:
- Vega is one of the brightest stars visible to the naked eye from Earth ($m = 0.03$)
- It is almost directly overhead for mid-northern latitudes (where most of the *official*, mathematical astronomy was being done at the time), and it is visible for much of the year.
- Vega's brightness is remarkably steady compared to many other stars.
- A magnitude of $m = 0.03$ is *so* close to 0 that it made sense to ground the scale at $m_{vega} = 0$.
- Other stars were then calibrated to this *standard candle*.
#### Sidebar: The Parallax Effect
- Astronomers measure nearby star distances by parallax — how much a star appears to shift against the background when Earth moves 1 AU (six months apart). 
- If a star shifts by **1 arcsecond**, its distance is defined as **1 parsec** (“parallax-second”). 
- By coincidence of geometry, **1 parsec ≈ 3.26 light years ≈ 206,265 AU**.

> [!important]
> One *arcsecond* is $\frac{1}{3600}$ of a degree on the sky, and $1$ degree on the sky is about twice as large as the width of the Full Moon, so, it's a *very small displacement*, indeed.
> 
> In fact, an arcsecond is about $5$ microns at arm's length, or about $\frac{1}{10} \text{to} \frac{1}{20}$ the width of a **human hair** from that same distance. In other words, you're not going to notice this just by looking — very precise instruments are needed to detect such small variations. However, instead of using really precise instruments, they used really *big* ones.

The sextant used by Prince Ulugh Beg (1394 – 1449 CE) in his observatory in Samarkand had a radius of about $40$ meters ($131 \text{ ft } 4 \text{ in}$), allowing him to make stellar position measurements as fine as $20$ arcseconds — a precision not matched until centuries after his time. His star catalog ([*Zīj-i Sultānī*; *The Sultanic Tables*](https://en.wikipedia.org/wiki/Zij-i_Sultani)), finished in 1439 CE, listed the positions of $\approx 1000$ stars with an accuracy better than $1$ arcminute.

It corrected many errors in the [*Almagest](https://en.wikipedia.org/wiki/Almagest)* of [Claudius Ptolemy](https://en.wikipedia.org/wiki/Ptolemy) (c. 100 – 170 CE), which had been the standard tabulation for $1200$ years. The precision of Ulugh Beg's work was not equaled in the West until Tycho Brahe's efforts in the late $16$th century, and it was still a respected reference well into the $17$th Century.
### The Distance Modulus: Relating Distance to Parallax

And *this* is where the distances to the stars comes back into the story.  **Apparent magnitude** and **Absolute Magnitude** are related by a relationship called *the [distance modulus*](https://en.wikipedia.org/wiki/Distance_modulus), mathematically expressed as:

$$
m - M = 5\;log_{10}(d) - 5
$$
Where $d$ is the distance to the star in [*parsecs*](https://en.wikipedia.org/wiki/Parsec) (about $3.26$ light years).

So, a star's **Absolute magnitude** is how bright the star *would appear to us if it were exactly $10$ parsecs away*.  This is less straighforward than the simple inverse-square law that governs apparent brightness for *local* observers, and might not really be that useful for worldmakers, unless you're wanting to know how bright your star would appear to someone looking at it from a significant distance away from your star system — or how bright a distant companion star appears in your planet's sky.
## Magnitude and Luminosity

The general equation relating **absolute magnitude** ($M$) to [[Stellamons -- Equations of State|stellar luminosity]] in stellar units is:

$$
M = M_⊙ - 2.5\; log_{10}(L)
$$
Where:
- $L$ = the star's luminosity in solar units.

> [!note]
> Notice the similarites to the distance modulus equation: $m - M = 5\;log_{10}(d) - 5$

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

 — gives us a rough approximation of any star's absolute magnitude and we can use the **distance modulus** to calculate an apparent magnitude from that.


