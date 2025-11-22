---
title: Cascading Rounding Notation
tags:
  - math
concepts: Rounding
---
# 1. Purpose & Scope

**Cascading Rounding Notation (CRN)** is a lightweight, human-friendly method
for reporting rounded or truncated numerical values with clarity and transparency. Its primary purpose is to reveal *how* a practical number was obtained from a more precise or raw value, without imposing any requirements on how calculations *must* be performed internally.

CRN is a **reporting notation**, not a computational standard.

It provides:
- A clear **precision floor** (the digit where rounding occurs),
- A defined **Rounding Domain** ( )  — the digits responsible for
  rounding up (up-rounding) behavior,
- An optional **overflow region** ' —  (digits that cannot affect up-rounding at
  the declared precision),
- A transparent link between a raw value and the simplified **resultant**.

CRN is **designed for**:
- Worldmakers who need trustworthy approximations without unnecessary
  complexity,
- Authors and educators who want readable and reproducible mathematics,
- Anyone who benefits from honest, reconstructible rounding in explanatory or
  computational contexts.

CRN **does not**:
- Replace traditional rounding rules,
- Enforce a particular rounding mode,
- Impose significant-figure conventions or uncertainty notation (though it is fully compatible with both),
- Dictate how numbers must be stored or computed.

Instead, CRN sits on top of your normal math workflow, providing a simple,
notational “window” into the rounding process. It documents the *why* behind a
reported value, while leaving the *how* to the user’s chosen mathematical,
scientific, or computational context.

CRN is compatible with all rounding conventions, including **Magnitude-First Rounding (MFR)**, the default rounding convention adopted in this corpus, and exists solely to make numerical communication clearer, more honest, and easier to follow.


> [!attention] Caveat
> All this being said, it’s worth acknowledging one significant OEM concern: Microsoft Excel’s rounding behavior is … quirky.
> 
>Depending on which function you call — ROUND(), ROUNDUP(), ROUNDDOWN(), MROUND(), INT(), etc. — Excel may return values that differ subtly (or dramatically) from what CRN implies or what traditional rounding would suggest.
>
>If you're using a spreadsheet to perform calculations, watch closely.  Excel does not always round the way you think it rounds, and certainly not the way CRN documents rounding.

# 2. Conceptual Foundations

CRN is built on a small set of intuitive concepts. These define *where* a number may be rounded, *which* digits influence that rounding, and *which* digits can be safely ignored. Together, they form the full rounding landscape for any CRN-annotated value.
## Bidirectional Cascade Model

CRN expresses rounding as a **cascade** that may influence digits both upward and downward from the precision floor. This cascade determines which digits matter for rounding and which digits may be safely ignored.

- **Up-rounding:**  
  Digits inside the Rounding Domain ( ) can propagate an up-rounding effect *leftward* across multiple places. A digit $\geq 5$ may round the digit to its left, which  may round the digit to its left, and so on, until the cascade stabilizes.

- **Down-rounding:**  
  Digits after the apostrophe $'$ can **never** influence rounding at the declared precision floor. The presence of $'$ establishes a **valid truncation boundary**: all digits to the right of $'$ may be omitted without changing the resultant at the chosen precision. "Down-rounding" in the CRN context is basically simple truncation of a decimal expansion at a particular location in the number.

Together, these behaviors create a **directional precision landscape**:

$$
\begin{array}{ccc}
\text{precision floor} & \text{Rounding Domain} & \text{overflow region} \\
3.141 & (59) & {}'2654 \\
\text{\small ten-thousandth} & \text{\small discretionary} & \text{\small disposable}
\end{array}
$$

This structure makes the three regions of the number explicit at a glance:
- digits that *set* the rounded value,  
- digits that *could* adjust it upward,  
- and digits that are irrelevant at the chosen precision.
## Contextual Precision

CRN expresses **precision as a context-dependent choice**, not as a global property of the number itself. A value may be written with different CRN forms depending on the needs of the calculation, the level of detail required, or the scale of the model.

CRN therefore, treats precision as **local** rather than inherent:

- The same raw number may appear with different precision floors in different contexts.
- A coarse CRN representation may coexist with a finer one elsewhere in the corpus.
- CRN does not mandate a “correct” level of precision; it records whichever level the author chooses for that moment.
### Examples (using $\pi$):
- thousandths:  
  $3.141(59)'2654$
- ten-thousandths:  
  $3.1415(9)'2654$
- hundredths:  
  $3.14'1592654$

Each notation expresses a **different precision floor**, tailored to the
context in which the number is used.

CRN’s role is not to standardize precision but to **make the precision choice
explicit**, so the reader can see at a glance:
- where rounding occurred,
- what digits influenced it,
- and how much precision is being preserved.
## Precision Floor

The **precision floor** is the position in the number where rounding occurs.
It is the **rightmost digit** appearing before either an apostrophe or a left parenthesis.
### Examples:
- $3.141(59)'2654$  
  Precision floor $3.141$ = the thousandths place.
- $1.618'03399$
  Precision floor $1.618$ = the thousandths place

The precision floor is the author’s declared resolution for *this context*: the floor sets the *effective precision*, while the CRN notation documents *how* the final value was chosen.
## Rounding Domain `( )`

The **Rounding Domain (RD)** is a parenthetical group of digits immediately after the precision floor. It contains **all and only** the digits that may force an upward rounding at that floor.

A digit belongs in the RD **if it is itself an up-rounding digit** ($\geq 5$). The RD expresses the exact source of rounding pressure — no more, no less.
### Examples:
- $3.141(59)'2654$  
  The digits $5$ and $9$ form the RD because:  
  - the $9$ can trigger rounding the $5$ up to $6$, which then  
  - can trigger rounding the $1$ at the precision floor up to $2$.

  Note that the RD does *not* mandate rounding; it only describes where up- rounding *could* or *did* occur.

  *Valid resultants include*:  
  - $3.14159$  
  - $3.1416$  
  - $3.142$

- $365.2563(6)'3004$  
  The enclosed digit $6$ may force the preceding $3$ up to $4$, but the
  following $3$ cannot force the $6$ upward, so that digit does *not* appear
  in the RD.

  *Valid resultants include*:  
  - $365.25636$  
  - $365.2564$

- A more coarse-grained version of this same number may be expressed as  
  **$365.25(6)'363004$**, yielding valid resultants:
  - $365.256$  
  - $365.26$

***NOTE***: Only one RD may appear in any CRN number.

**Incorrect**:  
- $365.25(6)3(6)'3004$
## Overflow Region $'$

The apostrophe $'$ marks the start of the **overflow region** — digits that **cannot** affect up-rounding at the declared precision floor. Any digits appearing after $'$ may be safely truncated.

Overflow digits may include values $5$–$9$, but the **first digit** after the apostrophe must be $\leq 4$, ensuring that no up-rounding can occur at the declared precision. These digits are irrelevant *in this context*, but may become relevant again if the precision floor is later expanded.
### Example:
- $3.141(59)'2654$  
  The digits $2654$ form the overflow region: they do not influence rounding
  at the thousandths place, but they preserve deeper precision for future use.

- $3.14'1592654$  
  The $1$ following the $4$ in the hundredths place cannot force an up-round of the $4$, so it and all digits following it could be truncated from the value in calculations.

- *Valid resultants include*:  
  - $3.14$  

The overflow region is optional and may contain any number of digits.
## CRN Approximation Declaration (CAD)

A **CRN Approximation Declaration (CAD)** explicitly links a simplified, practical value (the **resultant**) to the more precise value from which it was obtained. It is used at the *first occurrence* of any rounded number within a given context.

A CAD is written using a **left-pointing arrow**:

$$
\text{resultant} \;\longleftarrow\; \text{CRN form}
$$

This communicates:
1. **What value is actually being used**, and  
2. **How that value was derived** from a more precise quantity.
### Examples:
- Simple truncation at the thousandths place:  
  
- $$
  1.618 \;\longleftarrow\; 1.618'03399
 $$

- Rounding at the precision floor using the Rounding Domain:  
  
- $$
  365.2564 \;\longleftarrow\; 365.2563(6)'3004
  $$

A CAD records the exact *reason* a given resultant is valid, without requiring the raw number to be used in subsequent calculations.
### When to Use a CAD

Use a CAD:
- the **first time** an approximated number appears in a calculation, model,
  or explanatory text;
- whenever a previously raw or high-precision value is reduced in precision;
- whenever switching to a different approximation tier (e.g., from $3.1416$ to $3.142$).

After a CAD is declared, the resultant may be used alone for all subsequent steps within the same context.
### Purpose of the CAD

A CAD provides:
- **Transparency** — the reader knows exactly how a value was obtained.  
- **Reconstructability** — the original precision can be recovered.  
- **Contextual honesty** — the user sees both the approximation *and* the rationale for it.  
- **Workflow clarity** — only the [[Resultant|resultant]] propagates forward.

A CAD is not a rounding rule; it is a **disclosure**.
# 3. Rounding Conventions in CRN Contexts

CRN does not impose a rounding rule. Any rounding convention may be used, and  CRN simply reveals how the resulting value was obtained.

In the absence of an explicitly stated convention, this corpus adopts **Magnitude-First Rounding (MFR)**: round the absolute value using the chosen precision, then reapply the original sign. This approach aligns with the intuitive “round the number, then add the minus sign back” method common in manual calculations.

Examples using MFR:
- $-3.14159 \rightarrow -3.142$
- $3.14159 \rightarrow 3.142$

CRN remains valid regardless of the rounding convention applied. The CAD notation records the derivation visibly:

$$
3.142 \;\longleftarrow\; 3.141(59)
$$

This section defines only the default rounding behavior assumed when using CRN within this corpus. 


