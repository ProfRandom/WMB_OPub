---
title: Number Notation
tags:
  - metric
  - prefix
  - mass_domain
  - engineering
  - notation
  - math
---
# Number Notation
## Prefixes
WMB uses the standard SI prefixes ([Metric prefix](https://en.wikipedia.org/wiki/Metric_prefix)) for number magnitudes:

$$
\begin{array}{l c r | l c r}
\textbf{Intervals} &
\textbf{Abbr.} &
\textbf{Power} & 
\textbf{Intervals} &
\textbf{Abbr.} &
\textbf{Power}\\
\hline
\text{quecto-}  & \text{q} & 10^{-30} & \text{quetta-}   & \text{Q} & 10^{30} \\
\text{ronto-}  & \text{r} & 10^{-27} & \text{ronna-}   & \text{R} & 10^{27} \\
\text{yocto-}  & \text{y} & 10^{-24} & \text{yotta-}   & \text{Y} & 10^{24} \\
\text{zepto-}  & \text{z} & 10^{-21} & \text{zetta-}   & \text{Z} & 10^{21} \\
\text{atto-}  & \text{a} & 10^{-18} & \text{exa-}   & \text{E} & 10^{18} \\
\text{femto-}  & \text{f} & 10^{-15} & \text{peta-}  & \text{P} & 10^{15} \\
\text{pico-}  & \text{p} & 10^{-12} & \text{tera-}  & \text{T}  & 10^{12} \\
\text{nano-}  & \text{n}  & 10^{-9}  & \text{giga-}  & \text{G} & 10^{9} \\
\text{micro-} & \mu      & 10^{-6}  & \text{mega-}  & \text{M} & 10^{6} \\
\text{milli-} & \text{m}  & 10^{-3}  & \text{kilo-}  & \text{k}  & 10^{3} \\
\text{centi-} & \text{c}  & 10^{-2}  & \text{hecto-} & \text{h}  & 10^{2}  \\
\text{deci-}  & \text{d}  & 10^{-1}  & \text{deka-}  & \text{da} & 10^{1} \\
\end{array}
\\
$$
## Engineering Notation
Engineering notation is a practical way of writing numbers so they stay readable and scale cleanly with SI prefixes.

It differs from scientific notation in one key way:  **the exponent is always a multiple of three**.

This means every value can be expressed as a number from 1 to 999, times a familiar SI prefix.

This does two things **WMB** cares deeply about:
- Humans can read it without a calculator.
- The prefix tells you, instantly, the scale you’re working at.
- Each prefix is $1000\times = 10^3$ larger than the next one below it, so:
	- $1$ millimeter = $1,000$ micrometers
	- $1$ micrometer = $1,000$ nanometers
	- $1$ kilometer = $1,000$ meters
	- $1$ megameter = $1,000$ kilometers

For context, here are the vernacular meanings of the most common prefixes:
- nano ⟶ $1$ *billionth* = $^1/_{1000000000} = 0.000000001 = 1.0 \times 10^{-9}$
- micro ⟶ $1$ *millionth* = $^1/_{1000000} = 0.000001 = 1.0 \times 10^{-6}$
- milli ⟶ $1$ *thousandth* = $^1/_{1000} = 0.001 = 1.0 \times 10^{-3}$
- centi ⟶ $1$ *hundredth* = $^1/_{100}  = 0.01 = 1.0 \times 10^{-2}$
- deci ⟶ $1$ *tenth* = $^1/_{10} = 0.1 = 1.0 \times 10^{-1}$
- kilo ⟶ $1$ *thousand* = $1,000 = 1.0 \times 10^{3}$
- mega ⟶ $1$ *million* = $1,000,000 = 1.0 \times 10^{6}$
- giga ⟶ $1$ *billion* = $1,000,000,000 = 1.0 \times 10^{9}$
- tera ⟶ $1$ *trillion* = $1,000,000,000,000 = 1.0 \times 10^{12}$
- 
## Why Engineering Notation Exists
Scientific notation is great for precision:
- $42,300 = 4.23 \times 10^5$    
- $0.00000000791 = 7.91 \times 10^{-9}$
…but scientific notation _still_ leaves you mentally converting:

- “Is that thousands? Millions? Nano-something?”

Engineering notation fixes that by snapping everything to the SI prefix ladder:

- $4.23 \times 10^3 \longrightarrow 423\; \text{k}$ (kilo)
- $4.23 \times 10^{-9} \longrightarrow 4.23\; \text{n}$ (nano)
- $0.000423 \longrightarrow 423\;\mu$ (micro)
    
Same number, **far more intuitive**.
## The Ratchet Rule

This is the heart of engineering notation:

> **Ratchet up the prefix when the number reaches $1000$.  
> Ratchet down the prefix when it drops below $1$.**

Examples (using various base units):
- $0.23\; μ\text{L} \longrightarrow 230 \text{ nL}$ (microliters ⟶ nanoliters)
- $12400 \text{ m} \longrightarrow 12.4 \text{ km}$ (meters ⟶ kilometers)
- - $5900000\; J \longrightarrow 5.9 \text{ MJ}$ (joules ⟶ megajoules)
- $0.0042 \text { t} \longrightarrow 4.2 \text{ mt}$ (terrans ⟶ milliterrans)
    
If the number is ever ≥ 1000 or < 1,  just shift one prefix up or down.

This keeps values in the **1–999** window where human brains work best.