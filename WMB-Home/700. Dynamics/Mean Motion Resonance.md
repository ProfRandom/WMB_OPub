---
project: wmb
phase: 1
module: 1
status: draft
created:
updated: 2025-12-25
summary: ""
---
# Mean Motion Resonance

When two bodies orbit a third body in common, there will be resonances in their orbits. If one body’s orbit is an exact integer value different from the other’s, the two are said to be in *mean motion resonance*, and the ratio of their orbits is **a : b**, denoted as the longer orbital period followed by the shorter orbital period, separated by a colon (∶).

![[MeanMotionResonance2-1.jpg]]

For example, in the figure above, Body 1 orbits twice for every one orbit of Body 2.  This is a *first order resonance*, because the difference between the two values is only 1 unit:

$$
2 - 1 = 1
$$
Other examples of first-order resonances[^1] would be 6 : 5, 13 : 12, etc.

Examples of a *second-order resonance* would be those in which the orbital periods were separated by a difference of 2; e.g. 3 : 1 or 5 : 3.  The higher the order of the resonance, the less stable the orbits will be over time.

Mean motion resonances can arise between three or more bodies.  Jupiter's moons Io, Europa, and Ganymede experience a 4 : 2 : 1 mean motion resonance between them, such that for every orbit Ganymede makes, Europa completes two, and Io completes four.  This also means that Io orbits twice per each orbit of Europa.

However, an interesting phenomenon also occurs, such that Ganymede, Europa, and Io *never line up* on the same side of Jupiter.  Any two of them may line up at various points in their orbital dance, but all three never do.

> While N-conjunctions are *technically* possible in N-orbiton systems, they are reliant on very specific conditions of orbital eccentricity and coplanarity; mean motion resonances between more than three objects should be treated for all intents and purposes as *impossible*.

## The Synodian: Non-Integer Resonances
When two bodies orbit a central body, but their orbital periods are:
1. not integer multiples of the system's base time unit *T*; and,
2. not directly commensurate[^2] with one another,
… a more sophisticated approach is required to calculate periodic alignments of the system.

The *base time unit* ($T$), may be years, months, days, even hours or minutes.

The interval between such instances of alignment is called the *synodic period*; here, we'll refer to it as a *synodion* $\Sigma$ (pl: *synodia*), for reasons which will become clear presently.  The moment of alignment, when the two orbitons are closest to one another, we call a *synodos* (pl: *synodoi*).

Thus, the synodion represents the time it takes for the two orbitons to return to the same relative configuration, such as having their centers fall on a line that includes the center of the central body.  While synodia are still predictable, their periodicity is less intuitive that in mean motion resonance systems, requiring more precise calculations.

The best way to grasp these concepts is by working through an example.  By appling the rules of synodic periods to a specific pair of orbiting bodies, we can illustrate how to calculate a synodion, and explore the patterns it reveals.

### A Worked Example
Let's imagine a system of three bodies, the central body (*centron* $\dot{C}$) and two less massive bodies orbiting it (the *orbitons* $M_\alpha$ and $M_\beta$).  $M_\alpha$ has the longer orbital period ($P_\alpha$; the time it takes $M_\alpha$ to orbit the centron) and $M_\beta$ has the shorter orbital period ($P_\beta$; the time it takes $M_\beta$ to orbit the centron).

> While the masses of the bodies have no bearing on the following equations, they *do* matter from a nomenclature perspective.  The more massive body is always the *primary*, the second-most massive body is the *secondary*; the third most is the *tertiary*, etc.  Their *radii* are not a factor in determining their hierarchy.
> For instance, Mercury is more massive than Ganymede, but Ganymede has a larger radius.  If the two of them were to form a two-body system, *Ganymede would orbit Mercury*, even though it is larger in radius and volume than Mercury.

For this example, we will define:

$$
\begin{aligned}
P_\alpha = 24.36\; \text{days} \\
P_\beta = 11.72\; \text{days}
\end{aligned}
$$
![[synodion01.jpg|300]]
The above figure illustrates the starting configuration of our system ($T_0$).  The starting angle at which all three bodies are lined up we call the *base angle*, denoted by $B^\theta$.

We can already make some determinations about our system:

$$
\begin{aligned}
P_\delta = P_\alpha - P_\beta = 24.36 - 11.72 = 12.64\; \text{days} \\
P_Q = \dfrac{P_\beta}{P_\alpha} = \dfrac{11.72}{24.36} = 0.481\; \text{days}
\end{aligned}
$$
The ratio of their orbits ($P_Q$) is not an integer, so these orbitons are not in a mean motion resonance; for every orbit of $M_\beta$, $M_\alpha$ only completes $0.481$ of its orbit, because $M_\alpha$ takes $12.64$ days longer to orbit the centron than does $M_\beta$.

Since a full orbit for *either* orbiton is $360^\circ$, we can figure out how many degrees of their orbit each orbiton completes within the system base time unit, which in this case would be $1$ day.

$$
\begin{aligned}
\theta_\alpha &= \dfrac{360^\circ}{24.36} = 14.778^\circ \qquad \text{The \emph{minor unit angle}}\\
\theta_\beta &= \dfrac{360^\circ}{11.72} = 30.717^\circ  \qquad \text{The \emph{major unit angle}}\\
\end{aligned}
$$

This tells us how many degrees $M_\alpha$ "lags behind" $M_\beta$ per day:

$$
\theta_\Delta = \theta_\beta - \theta_\alpha = 30.717^\circ - 14.778^\circ = 15.939^\circ \qquad \text{The \emph{orbiton difference angle}}
$$
So, every day $M_\beta$ moves almost $16^\circ$ farther in its orbit than $M_\alpha$ does in its orbit.

We can also calculate ho many degrees of its orbit $M_\alpha$ completes (subtends) per each full orbit of $M_\beta$:

$$
\alpha^\circ = P_Q \times 360 = 0.481 \times 360 = 173.202^\circ 
$$
So, after *two* of $M_\beta$'s orbits:

$$
2 a^\circ = (2)(173.202) = 346.404^\circ
$$
… $M_\alpha$ still hasn't completed one of its orbits, it has only completed

$$
\dfrac{346.404}{360} = 0.962
$$
orbits of the centron.

Conversely, by the time $M_\alpha$ completes one full orbit of the centron, $M_\beta$ will have completed

$$
P_R = \dfrac{24.36}{11.72} = 2.078
$$
orbits of the centron.

It is a curious feature of circular motion that if you get far enough ahead of the other body, you eventually come up behind it.  Think of a 5000-meter Olympic footrace.  All of the competitors start out on the same line and travel in the same direction.  Let's say there are two runners, Number 11 and Number 24.

Number 11 quickly pulls out ahead of Number 24 and for a time it is quite obvious that she is "way out ahead".  But if she maintains her higher running speed, eventually she will be *so far ahead* of Number 24 that *she will appear to be running behind them*.  Anyone looking in on the race at just that moment could be forgiven for thinking that Number 11 is losing, perhaps badly.

However, eventually Number 11 will catch up to Number 24 and pass them again; but for a moment they will be side-by-side, just as they were at the start of the race *but not back on the starting line*; their meeting point will be some angular distance around the track from where they began.  Where and when this moment occurs is entirely a matter of how fast each runner is running.

Returning to our orbitons, it becomes obvious that at some point while they are orbiting, they will "meet up" at their closest approach to one another, just as our runners did in the Olympic race — they will have achieved synodos.  The first synodos to occur after $T_0$ we label $T_1$; the second we label $T_2$, and so on.

Here's the really cool thing: we can calculate exactly *where* and *when* $T_1, T_2$, etc. take place!

#### The When
The synodic period (mentioned above) is the period of time that transpires between any two synodoi:

$$
\begin{aligned}
\begin{split}
\Sigma &= \dfrac{P_\alpha \times P_\beta}{|P_\alpha - P_\beta|} \\
&= \dfrac{24.36 \times 11.72}{|24.26 - 11.72|} \\
&= \dfrac{285.499}{12.64} \\
\Sigma &= 22.587\; \text{days ✓}
\end{split}
\end{aligned}
$$
So, each synodos occurs just over $22\frac{1}{2}$ days after the preceding one.

> Note that if we divide $360^\circ$ by the difference angle $\theta_\Delta$

$$
 \Sigma = \dfrac{360}{\theta_\Delta} = \dfrac{360}{15.939}= 22.587\; \text{days}
 $$
 … we also get the synodic period.

Notice that the synodion, $22.587$ days is more than two orbits of $M_\beta$ and less than one orbit of $M_\alpha$.  If we divide the lengths of each orbiton's period by the length of the synodion:

$$
\begin{aligned}
F_\alpha &= \dfrac{P_\alpha}{\Sigma} = \dfrac{24.36}{22.587} = 0.9272\; \text{orbit}\\
F_\beta &= \dfrac{P_\beta}{\Sigma} = \dfrac{11.72}{22.587} = 1.9272\; \text{orbits}
\end{aligned}
$$
Do you see it?  The decimal fraction of both of these quotients is the same: $0.9272$.  We designate this as the *synodial fraction*, and denote it as $F_\Sigma$, and it helps us to answer the question of "where" the synodoi take place.

What the synodial fraction tells us is that synodos $T_1$ occurs $1.9272$ orbits of $M_\beta$ and $0.9272$
orbits of $M_\alpha$ from their starting time ($T_0$) and place (the base angle $B^\theta$).  Multiplying the synodial fraction by the number of degrees in a circle:

$$
\Theta = F_\Sigma \times 360^\circ = (0.9272)(333.7975^\circ) \qquad \text{The \emph{synodial angle}}
$$
Subtracting the synodial angle from $360^\circ$:

$$
\Delta_\Theta = 360^\circ - \Theta = 360^\circ - 333.7975^\circ = 26.203^\circ \qquad \text{The \emph{synodial lag angle}}
$$
… we now know that each successive synodos occurs $22.587$ days after *when* and $26.203^\circ$ "short" of where the previous one occurred.  Thus the synodoi "march backward" around the centron.  We can calculate the precise angle relative to $B^\theta$ any given synodos occurs by:

$$
\widehat{\Theta} = 360^\circ - MOD((S \times \Delta_\Theta), 360)
$$
where S is the number of the synodos after $T_0$; e.g. for synodos $T_6, S = 6$.

## Diving Deeper
Above, we learned about the synodic period equation:

$$
\begin{aligned}
\Sigma &= \dfrac{P_\alpha \times P_\beta}{|P_\alpha - P_\beta|} \\
\end{aligned}
$$
Here is a comprehensive listing of the related equations:

$$
\begin{aligned}
& \text{Given: } P_\alpha > P_\beta \\[1em]
\Sigma &= \dfrac{P_\alpha P_\beta}{|P_\alpha - P_\beta|}
& P_\alpha &= \dfrac{\Sigma P_\beta}{\Sigma - P_\beta}
& P_\beta &= \dfrac{\Sigma P_\alpha}{\Sigma + P_\alpha} \\[1em]
\dfrac{1}{\Sigma} &= \left|\dfrac{1}{P_\alpha}-\dfrac{1}{P_\beta}\right|
& \dfrac{1}{P_\alpha} &= \dfrac{1}{P_\beta}-\dfrac{1}{\Sigma}
& \dfrac{1}{P_\beta} &= \dfrac{1}{P_\alpha}+\dfrac{1}{\Sigma} \\[1em]
\end{aligned}
$$
$$
\begin{array}{rcl}
Q &= \dfrac{P_\beta}{P_\alpha} 
&P_\alpha = P_\beta \times R = \dfrac{P_\beta}{Q} 
= \left(\dfrac{\Sigma}{Q} - \Sigma\right) = \Sigma(R - 1) \\[1em]
R &= \dfrac{P_\alpha}{P_\beta} 
&P_\beta = P_\alpha \times Q = \dfrac{P_\alpha}{R}
= \left(\Sigma - \dfrac{\Sigma}{R}\right) = \Sigma(1-Q)
\end{array}
$$
Where:
- $\Sigma$ = synodion
- $P_\alpha$ = period of the outer body, $M_\alpha$ (longer)
- $P_\beta$ = period of the inner body, $M_\beta$ (shorter)
- $Q$ = quotient of the outer body period to the inner body period
- $R$ = ratio of the inner body period to the outer body period

> *Note that the second row of equations perform the same calculations as the first row by using the reciprocals of the orbital periods.*

All of this leads us naturally to the question:

> Does any future synodos ever fall precisely at the base angle $B^\theta$ again?  In other words is

$$
\widehat{\Theta} = 0^\circ
  $$
  … ever true after $T_0$?

The answer is "yes" and we can calculate that, too.

***
Tag Core
#time #orbits #math 
