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
# Stellar Magnitude and The Distance Modulus
You've probably encountered the term _magnitude_ in relation to stars before, perhaps even heard mention of the two types: _absolute magnitude (M)_ and _apparent magnitude (m)_.  Simply put, a star's **absolute magnitude** is how visibly bright it actually is, and its **apparent magnitude** is how bright it appears.
## The History of Magnitudes
### Apparent Magnitude

Early astronomers had to rely on the best equipment they could obtain — their own eyes.  So, magnitudes were originally determined by how faint a star appeared in the sky.  And, yes, Keppy, before you interrupt, it _was_ a woefully subjective system, but it was all they had to work with.  The system was formalized by Hipparchus, along with Claudius Ptolemy, in the Second Century BCE.

The most visible (brightest) stars were given a (visual) magnitude of $1$; magnitude $2$ stars were dimmer than magnitude $1$ stars, magnitude $3$ dimmer still, and so on.  Magnitude $6$ stars were those just barely bright enough to be seen with the naked eye.

>Note that this is based on ideal viewing conditions... dark sky, no full moon, no clouds, etc.
>- For modern people looking up under a suburban sky, the best they're likely to be able to see is around magnitude $4.5 – 5$
>- City dwellers will be lucky to see stars of magnitude $3$.


> [!info]
> >In fact, in 1994, the city of Los Angeles experienced a major power outage as a result of the Northridge earthquake.  The lack of "light pollution" gave residents a view of the night sky they were unfamiliar with, which included the Milky Way (our own galaxy) glowing overhead.  Observatories such as the one in Griffith Park, reported receiving calls from curious — and sometimes alarmed — residents, enquiring what the strange glowing cloud above was.

You'll notice that, astronomers being astronomers, these numbers also run "backward" — the higher the magnitude, the dimmer the star (or any object for that matter), so, yes, you will encounter _negative magnitudes_ for those objects that are brighter than the brightest stars; the Full Moon, for instance has an apparent magnitude of $-12.9$ on this scale, and the planet, Venus, has an apparent magnitude of $-4.7$ at its brightest in Earth's sky.

Later astronomers — _much later_, in fact more than _2000 years later_ — made the system mathematical, on a logarithmic scale.  This means that in the modern system, a magnitude $2$ star is $2.512$ times dimmer than a magnitude 1 star.

### **Why $2.512$?**

How did I know you were going to ask that — and marvelous pun, by-the-way.

When modern astronomer Norman Robert Pogson (1829 – 1891), decided to "mathematize" Hipparchus subjective scale, he didn't want to rewrite literally thousands of years of astronomical documents to re-categorize stars, so, he had to stick with the $1 – 6$ scale Hipparchus had established.  This means that there's a difference of $6 - 1 = 5$ steps between the dimmest and the brightest stars.

_Fortunately_, by measurement, the **brightness** difference between first and sixth magnitude stars is about a factor of $100$.  So, 5 steps in magnitude = $100\times$ in brightness; therefore the difference between each single step in the sequence is:

$$
d = \sqrt[5]{100} \approx 2.5118864
$$

… which is rounded to $2.512$ for convenience.  Practically speaking, one can simply remember that a magnitude $3$ star is $2.5\times$ brighter than a magnitude 4 star.
### Absolute Magnitude ($m$)

As with **apparent brightness**, however a star's magnitude is dependent on its distance from the observer, and once it became clear to astronomers that different stars were different distances away, the question naturally arose: "How bright are they, _really_, then?"

### Vega, The 'Standard Candle'

The star α-Lyrae, popularly known as Vega, acts as the standard candle for absolute magnitudes because:

- Vega is one of the brightest stars visible to the naked eye from Earth ($m_{vega} = 0.03$)
- It is almost directly overhead for mid-northern latitudes (where most of the "official", mathematical astronomy was being done at the time), and it is visible for much of the year.
- Vega's brightness is remarkably steady compared to many other stars.
- A magnitude of $0.03$ is _so_ close to $0$ that it made sense to ground the scale at $m_{vega} = 0$.
- Other stars were then calibrated to this "standard candle".
#### The Parallax Effect

- Astronomers measure nearby star distances by parallax — how much a star appears to shift against the background when Earth moves 1 AU (six months apart).    
- If a star shifts by **$1$ arc-second**, its distance is defined as $**1$ parsec** (“parallax-second”).    
- By coincidence of geometry, $1 \text{parsec} \approx 3.26\; \text{light years} \approx 206,265 AU$.

> [!info]
> One _arc-second_, by the way, is $\frac{1}{3600}$ of a degree on the sky, and $1$ degree on the sky is about twice as large as the width of the Full Moon, so, it's a _very small displacement_, indeed.
> 
> In fact an arcsecond is about 5 microns at arm's length, or about $\frac{1}{10}\; \text{to}\; \frac{1}{20}$ the width of a human hair from that same distance.  In other words, you're not going to notice this just by looking — very precise instruments are needed to detect such small variations. 

Instead of using really precise instruments, they used really _big_ ones.  The sextant used by Prince Ulugh Beg (1394 – 1449 CE) in his observatory in Samarkand had a radius of about $40$ meters ($131' 4''$), allowing him to make stellar position measurements as fine as $20$ arc-seconds — a precision not matched for centuries after his time.  His star catalog (*Zīj-i Sultānī*; "The Sultanic Tables"), finished in 1437 CE, listed the positions of $\approx1000$ stars with an accuracy better than $1$ arc-minute.  It corrected many errors in the _Almagest_ (Alexandria, c. 150 CE) of Claudius Ptolemy (c. 100 – 170 CE), which had been the standard tabulation for $1200$ years.  The precision of Ulugh Beg's work was not equaled in the West until Tycho Brahe's efforts in the late 16th century, and it was still a respected reference well into the 17th Century.


***
Tag Core
#stellamonics #ontics  #math 
