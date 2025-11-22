---
title: Animotic Domains
tags:
  - animotics
  - gaean
  - geotic
  - telluric
  - xenotic
  - Kybelic
---
# Animotic Orders
## Biotic Order

m := ⟨0.01 ∧ 10.00⟩⨁ 
ρ := ⟨0.50 ∧ 7.00⟩⨁ 
g := ⟨0.15 ∧ 8.00⟩⨁ 
r := ⟨0.15 ∧ 3.00⟩⨁
vₑ := ⟨0.20 ∧ 3.00⟩⨁

> **Tellurics** are the full class of rocky, metallic, or icy solid-surface planemons.
> This domain spans everything from Earthlike worlds to massive superterrestrials, frozen dwarfs, scorched tidally-locked crusts, and subplanetary bodies like Ganymede or Titan.
> 
> Tellurics are defined purely by **structure** — a solid or semi-solid lithosphere —regardless of habitability, atmosphere, or surface conditions.
### Core Features

- This domain is broad:    
    - **1.7%** of Tellurics qualify as **Terric** (habitable)        
    - **0.34%** qualify as **Geotic** (Earthlike-leaning)        
    - **0.17%** qualify as **Gaean** (the sweet-spot ideal)        
    - **~1.2%** qualify as **Kybelic** (super-Earth habitable class)
        
- Tellurics possess well-defined surfaces or crusts, but have **no requirement** for environmental habitability, biospheres, or atmospheric stability.    
- Many are **parahabitable**—survivable only with domes, subsurface refugia, or environmental engineering.   
- This category includes:    
    - sub-Earths and dwarfs        
    - Earthlike and super-Earth rocky planets        
    - crusted ocean worlds        
    - cryogenic outer-system bodies        
    - irradiated volcanic hyperterrestrials
### Relations to Other Categories

- **Telluric** is the **parent domain** of the **Terric** and **Geotic** Domains and the **Gaean Province**, which is itself nested within Geotic.  
    All members of those narrower classes are, by definition, **Telluric**.    
- **Kybelic** worlds partially overlap Tellurics.  
    All Kybelics fall within Telluric structural–chemical allowances, but only a small fraction of Tellurics meet Kybelic conditions.    
- **Xenotic** worlds are defined by their **non-carbonic, non-water-solvent biotic potential**, not by their structure.
	- They may have rocky crusts, Earthlike densities, and familiar surface conditions —  
		  **but if their chemistry supports _alien_ bioregimes rather than terragen ones, they are classified as Xenotic, not Telluric.**
    
    In short:    
    - Telluric = _within terragen biochemical possibility_        
    - Xenotic = _outside terragen biochemical possibility_
	-  The two use **different axes** of classification and do **not** overlap in category.
### Symbolic Use

- _Telluric_ stems from **Tellus**, the primordial Roman Earth-mother —  
    older even than Terra, and tied to the deep, foundational substance of the world.    
- This etymology suits the domain’s role:  
    **Telluric = all solid-earth planemons**, the material envelope from which all habitable and quasi-habitable subclasses descend.    
- When contrasted with _Xenotic_, the distinction is **physical** rather than biological:  
- **Telluric** describes _worlds whose physical conditions fall within the possible envelope for carbonic–water–oxygen life_, regardless of whether they are actually habitable.  
    It is a **structural + chemical regime aligned with terragen biochemistry**.
- **Xenotic** describes _worlds whose physical or chemical environment favors non-carbonic biochemistries_ — ammonia, hydrocarbons, silicon-chain chemistries, supercritical solvents, etc.  
    They may resemble Tellurics physically, but they lie **outside the terragen-life regime**.
## Terric Realm

m := ⟨0.30 ∧ 3.35⟩⨁
ρ := ⟨0.85 ∧ 1.25⟩⨁
g := ⟨0.60 ∧ 1.65⟩⨁
r := ⟨0.60 ∧ 1.50⟩⨁
vₑ := ⟨0.65 ∧ 1.50⟩⨁

$$
\text{TERRIC} := \left\{ (m, \rho) \in \mathbb{R}^2 \ \middle|\
\begin{aligned}
&0.30 ≤ m ≤ 3.35 \\
&0.85 ≤ \rho ≤ 1.25 \\
&0.60 ≤ g(m, \rho) ≤ 1.65 \\
&0.60 ≤ r(m, \rho) ≤ 1.50 \\
&0.65 ≤ v_e(m, \rho) ≤ 1.50
\end{aligned}
\right\}
$$
> **Terrics** are **habitable** planemons — solid-surface worlds whose physical and environmental conditions fall within the broad envelope compatible with **carbonic, water-solvent life**, including human physiology.

### Core Features
- **Narrow density bounds** enforce a rocky–metallic–silicate structure typical of terrestrial worlds.    
- **Mass and radius** are allowed more freedom, producing Terrics that range from light sub-Earths to heavy super-Earths.    
- **Gravity and escape velocity** remain within ranges that are biologically tolerable for humans, plants, and Earth-derived biomes.

Terrics form the **primary habitable range** of the Talosic Domain.
### Implications and Examples

Terrics may include:
- **Marginal Earth-twins**  
    Near the edges of Geotic parameters — stable but imperfectly Earthlike.    
- **High-gravity super-Earths**  
    Still habitable, but challenging for human mobility and architecture.    
- **Cooler, lighter Earthlikes**  
    Low-pressure, broad-skied worlds where cold-tolerant biomes thrive.
    
**All Geotics are Terrics**, but not all Terrics meet the tighter Geotic criteria.
## Geotic Realm

m := ⟨0.45 ∧ 1.85⟩⨁
ρ := ⟨0.85 ∧ 1.25⟩⨁
g := ⟨0.90 ∧ 1.10⟩⨁
r := ⟨0.70 ∧ 1.30⟩⨁
vₑ := ⟨0.80 ∧ 1.20⟩⨁

$$
\text{GEOTIC} := \left\{ (m, \rho) \in \mathbb{R}^2 \ \middle|\
\begin{aligned}
&0.45 ≤ m ≤ 1.85 \\
&0.85 ≤ \rho ≤ 1.25 \\
&0.90 ≤ g(m, \rho) ≤ 1.10 \\
&0.70 ≤ r(m, \rho) ≤ 1.30 \\
&0.80 ≤ v_e(m, \rho) ≤ 1.20
\end{aligned}
\right\}
$$
>**Geotics** are **strong-Earthlike** planemons — worlds whose physical properties cluster near those of Earth, offering **stable, moderate, and biocompatible environments** that support long-term carbonic life with minimal modification.

They represent the **narrow center band** of the Terric Realm:  
physically close to Earth in gravity, size, composition, and escape energy, but not so restrictive as the Gaean Province.

Geotics are the **backbone category** for stable, Earth-normal ecosystems.

### Core Features

- **Earth-normal density range** yields terrestrial composition: rocky–metallic silicates with moderate self-compression.    
- **Gravity near 1⨁** ensures familiar biomechanics, atmospheric retention, and hydrological behavior.    
- **Radius and escape velocity** occupy the zone where Earthlike climates and circulation patterns are structurally favored.
    - These values collectively define the **Earthlike structural envelope** without requiring a perfect match.
    
Geotics are the worlds where Earth-based biology can operate naturally, not merely survive.
### Implications and Examples

Geotics include:
- **Earth-analog worlds**  
    Slightly warmer, cooler, wetter, or drier than Earth, but broadly similar.    
- **Moderate super-Earths and sub-Earths**  
    Provided gravity remains close to 1⨁ and escape velocity remains manageable.   
- **Worlds capable of supporting full biomes**  
    Including forests, oceans, complex food webs, and Earth-mode atmospheric dynamics.
    
Geotics may include:
- Planets with minor atmospheric modification needs    
- Worlds with regional extremes but global stability    
- High-oxygen or high-humidity variants still compatible with terragen life
## Gaean Province

(Optimal Earthlike Worlds — the Habitat Ideal)
m := ⟨1.00 ∧ 1.85⟩⨁
ρ := ⟨0.85 ∧ 1.25⟩⨁
g := ⟨0.85 ∧ 1.10⟩⨁
r := ⟨0.90 ∧ 1.30⟩⨁
vₑ := ⟨0.95 ∧ 1.20⟩⨁

$$
\text{GAEAN} := \left\{ (m, \rho) \in \mathbb{R}^2 \ \middle|\
\begin{aligned}
&1.00 ≤ \rho ≤ 1.25 \\
&0.85 ≤ g(m, \rho) ≤ 1.10 \\
&0.90 ≤ r(m, \rho) ≤ 1.30 \\
&0.95 ≤ v_e(m, \rho) ≤ 1.20
\end{aligned}
\right\}
$$
> Gaeans form the **habitat-perfect subset** of the Geotic Domain.
> Where Geotics are broadly Earthlike and comfortably habitable, **Gaeans are the apex** — worlds whose physical structure falls into the heart of human biomechanical and ecological preference.

A Gaean world is:

- **freely breathable**
- **walkable without adaptation**    
- **biomechanically effortless**    
- **stable across geologic time**    
- **instinctively familiar** even if alien in ecosystem
    
> **All Gaeans are Geotics.  
> 	Only ~48.8% of Geotics are Gaeans.**

Gaean = _the Earth-normal sweet spot of parameter space._

![[Gaean Province by Domains.png]]

## **How to Read This Chart**

This chart shows **where Gaean worlds fall inside larger envelopes**, not the other way around.

That is, the bars answer the question:

> **“Of all Gaeans, what percentage also meet the criteria of each broader class?”**

Because the **Biotic Order** is _much, much larger_ than the Gaean envelope, only a tiny fraction of all Biotic-compliant worlds qualify as Gaeans — but **every single Gaean is still part of the Biotic Order**.  

The small percentage for “Biotic Order” therefore reflects the _narrowness of the Gaean slice_, not an exclusion from the parent class.

In short:

- **Small bar ≠ exclusion**    
- **Small bar = Gaeans are a rare, narrow subset inside that much larger envelope**
## Kybelic Realm

(High-Mass, High-Vitality Terrestrial Worlds)

m := ⟨1.00 ∧ 3.00⟩⨁
ρ := ⟨0.85 ∧ 1.25⟩⨁
g := ⟨0.85 ∧ 1.70⟩⨁
r := ⟨0.90 ∧ 1.50⟩⨁
vₑ := ⟨0.95 ∧ 1.50⟩⨁

$$
\text{KYBELIC} := \left\{ (m, \rho) \in \mathbb{R}^2 \ \middle|\
\begin{aligned}
&1.00 ≤ m ≤ 3.00 \\
&0.85 ≤ \rho ≤ 1.25 \\
&0.85 ≤ g(m, \rho) ≤ 1.70 \\
&0.90 ≤ r(m, \rho) ≤ 1.50 \\
&0.95 ≤ v_e(m, \rho) ≤ 1.50
\end{aligned}
\right\}
$$
> *Kybelics* are **parahabitable** planemons — terrestrial super-Earths with conditions **favorable to rich biospheres** but likely **inhospitable to unmodified humans**. They may possess higher surface gravity, thicker atmospheres, and more energetic climates, often demanding mechanical, biological, or infrastructural adaptations for long-term Earthling presence. Nonetheless, they are considered highly conducive to complex, robust life — just not necessarily Earthlike.

**Overlap with Gaeans**:
- A **small subset** of Kybelics — **≈13.9%** — fall within the Gaean gravity range (0.9 ≤ g ≤ 1.1⨁). 
- These rare worlds are **massive and dense** enough to support Earth-normal surface conditions **while offering enhanced biospheric potential** — possibly the best of both worlds.
**Core Feature**:
- The **“superhabitable” zone**: larger size means broader climatic bands, more plate tectonics, greater magnetic shielding, and longer tectonic–volcanic cycling — all of which may favor biospheric richness and diversity. 
- **Human settlement** is plausible but typically **requires support**: enhanced structural design, medical mitigation of gravity effects, and climate regulation systems.
**Distinction from Geotics**:
- All Kybelics meet **Geotic** compositional constraints, but their **mass and gravity trends upward**. 
- **Not all Geotics** are Kybelic: Kybelics are a **subset of high-mass, dense, habitable** planemons. 
- Conversely, **not all Kybelics are Gaean** — only a small slice of them match that precise Earthlike window.

# Kybelic planemons

**Definition** 
The concept of *superhabitable planemons* was proposed by René Heller and John Armstrong (2014) to describe worlds with physical, orbital, and stellar characteristics that make them **more conducive to rich, diverse biospheres** than Earth — though not necessarily more suitable for humanoid or Earthlike life.

**Stellar Criteria** 
- Host star mass range: ⟨0.359 ∧ 0.817⟩⊙ (spectral classes M0∧G9)
- Host star lifespan: ⟨1.656 ∧ 12.934⟩⊙ years 
- Stellar age: Older than the Sun’s 4.5 Ga but younger than 7 Ga 

**Planemon Characteristics** 
- **Mass**: ⟨2.0 ∧ 3.0⟩⨁ (optimum ≈ 2.0⨁) 
- **Radius**: ⟨1.260 ∧ 1.442⟩⨁ (maintains Earthlike density and gravity) 
- **Geology**: Larger tectonic–volcanic cycling, longer plate tectonic activity, strong carbon–silicate cycle, thicker atmosphere retention. 
- **Magnetic Field**: Stronger due to larger liquid core and higher internal heat. 
- **Surface Geography**: Flatter topography, shallower oceans, widely distributed ocean coverage (~71% surface area) without large continuous land masses. 
- **Temperature**: Mean ≈ 25 °C (77 °F). 
- **Atmosphere**: Thicker than Earth’s; O₂ concentration > 20.95%. 
- **Orbit**: Closer to the center of the host system’s habitable zone than Earth is in the Solar System. 
 - Solar System example: center of optimistic HZ ≈ 1.26 AU; center of conservative HZ ≈ 1.16 AU.

**Scientific Rationale** 
From Heller & Armstrong (2014): 
> “Terrestrial planemons that are slightly more massive than Earth, up to 2 or 3 M⊕, are preferably superhabitable due to the longer tectonic activity, a carbon–silicate cycle active on a longer timescale, enhanced magnetic shielding, larger surface area, smoother surface, thicker atmosphere, and the positive effects of non-intelligent life on habitability.”

Lena Noack & Doris Breuer (2011) add: 
> “…the propensity of plate tectonics seems to have a peak between 1 and 5 Earth masses… a geological perspective suggests the optimal mass of a planemon is about 2 M⊕.”

**Relation to WCB Classifications** 
In *Worlds by the Numbers*, **Kybelic planemons** encompass the superhabitable concept, with parameter refinements for internal consistency within WCB’s classification system. 

**References** 
- Heller, René, and John Armstrong. “Superhabitable Worlds.” *PubMed* (National Library of Medicine, December 31, 2013). [https://pubmed.ncbi.nlm.nih.gov/24380533/](https://pubmed.ncbi.nlm.nih.gov/24380533/) 
- Noack, Lena, and Doris Breuer. “Plate Tectonics on Earth-Like Planets.” *ResearchGate*, January 2011. [https://www.researchgate.net/publication/225001335_Plate_Tectonics_on_Earth-like_Planets_Implications_for_the_Habitability](https://www.researchgate.net/publication/225001335_Plate_Tectonics_on_Earth-like_Planets_Implications_for_the_Habitability)

## Xenotic Order

m := ⟨0.0001 ∧ 4131⟩⨁
ρ := ⟨0.01 ∧ 7.00⟩⨁
g := ⟨0.02 ∧ 60.00⟩⨁
r := ⟨0.02 ∧ 11.00⟩⨁
vₑ := ⟨0.02 ∧ 25.00⟩⨁

$$
\text{XENOTIC} := \left\{ (m, \rho) \in \mathbb{R}^2 \ \middle|\
\begin{aligned}
&0.0001 ≤ m ≤ 4131 \\
&0.01 ≤ \rho ≤ 7.00 \\
&0.002 ≤ g(m, \rho) ≤ 60.00 \\
&0.02 ≤ r(m, \rho) ≤ 11.00 \\
&0.02 ≤ v_e(m, \rho) ≤ 25.00
\end{aligned}
\right\}
$$
> *Xenotics* are planemons whose environmental conditions may support **non-Earthlike life**, including **non-carbonic**, **non-water-based**, or otherwise exotic biochemistries. The term is not tied to physical parameters, but to the **biological strangeness** of the world's potential life-hosting capacity.

**Core Feature**:
- Xenotic classification **is not about what the world *is*** — it’s about **what kind of life it might support**.
- A Xenotic world might be a rocky, icy, or gaseous body — but its **biotic potential lies outside** the realm of Earth-normal life.
- This is an *extremely* broad classification: only 0.35% of planemons sharing Xenotic mass and density ranges qualify as *Tellurics*. Gaeans share mass and density range with only 0.001% of Xenotics.
**Key Principle**:
> A world may fall entirely within Gaean or Geotic **parameters** and still be **Xenotic in character** — if its biosphere is chemically or structurally **alien to terrestrial assumptions**.

**Included Provinces**:
- **Ammonia-based** or **methanogenic** biospheres (e.g., Titan-like)
- **Silicon-based** or **plasma phase** consciousness (hypothetical)
- **High-pressure deep-atmosphere lifeforms** on gas giants
- **Ultra-dense crust-worlds** with lattice-bonded metabolic substrates
- **Life emerging in conditions unreplicable on Earth**
**Exclusions**:
- Gaean or Geotic worlds are **not Xenotic** simply by shape or size.
- Xenotic worlds **may physically overlap** with all other categories — but their **life potential diverges completely**.
**Symbolic Use**:
- From Greek *xenos* (ξένος): “stranger,” “foreigner,” “outsider.” 
- Xenotic worlds are those where **life is not just different — it is alien**.
**Parameter Notes**:
- **Mass (⨁):** from sublunar pebbles to brown dwarf threshold. 
- **Density (⨁):** from hydrogen-ice slushes to ultra dense crystal-metallic cores. 
- **Gravity (⨁):** ~0.02⨁ (Mars-like) up to ~60⨁ (felt at inner gas dwarf surfaces). 
	- Spans everything from fragile ultralow-gravity cometary clumps to neutronium-crusted compact objects just short of degeneracy collapse.
	- This definition also accommodates highly stratified gas layers (e.g. floatable biospheres in Saturnian-class or puffy hot-Neptune exotics).
	- Any values beyond this envelope cross into **ulsic** or **hypotheticals**: black holes, quark matter, etc.
- **Radius (⨁):** up to 11⨁ to accommodate inflation-limited gas giants and Super-Jupiters.
	- Frequently exceeded by puffy planemons due to close proximity to their stars inflating their atmospheres.
- **Escape Velocity (⨁):** capped at 25⨁ ≈ 280 km/s, brushing the domain of hot-start brown dwarfs.

> These are **not bound by Earth-normal biology**. They simply represent physically plausible, self-cohering planemon-scale entities where exotic life — as chemistry permits — might arise.




| —        | Telluric | Terric | Geotic | Gaean  | Kybelic |
|----------|----------|--------|--------|--------|--------|
| Telluric | 1        | 0.0171 | 0.0035 | 0.0017 | 0.0115 |
| Terric   | 1        | 1      | 0.2013 | 0.0976 | 0.6935 |
| Geotic   | 1        | 1      | 1      | 0.4876 | 0.4876 |
| Gaean    | 1        | 1      | 0.9998 | 1      | 1      |
| Kybelic   | 1        | 0.9975 | 0.1391 | 0.1391 | 1      |

## Terric Realm

m := ⟨0.30 ∧ 3.35⟩⨁
ρ := ⟨0.85 ∧ 1.25⟩⨁
g := ⟨0.60 ∧ 1.65⟩⨁
r := ⟨0.60 ∧ 1.50⟩⨁
vₑ := ⟨0.65 ∧ 1.50⟩⨁

$$
\text{TERRIC} := \left\{ (m, \rho) \in \mathbb{R}^2 \ \middle|\
\begin{aligned}
&0.30 ≤ m ≤ 3.35 \\
&0.85 ≤ \rho ≤ 1.25 \\
&0.60 ≤ g(m, \rho) ≤ 1.65 \\
&0.60 ≤ r(m, \rho) ≤ 1.50 \\
&0.65 ≤ v_e(m, \rho) ≤ 1.50
\end{aligned}
\right\}
$$
> **Terrics** are **habitable** planemons — solid-surface worlds whose physical and environmental conditions fall within the broad envelope compatible with **carbonic, water-solvent life**, including human physiology.

### Core Features
- **Narrow density bounds** enforce a rocky–metallic–silicate structure typical of terrestrial worlds.    
- **Mass and radius** are allowed more freedom, producing Terrics that range from light sub-Earths to heavy super-Earths.    
- **Gravity and escape velocity** remain within ranges that are biologically tolerable for humans, plants, and Earth-derived biomes.

Terrics form the **primary habitable range** of the Talosic Domain.
### Implications and Examples

Terrics may include:
- **Marginal Earth-twins**  
    Near the edges of Geotic parameters — stable but imperfectly Earthlike.    
- **High-gravity super-Earths**  
    Still habitable, but challenging for human mobility and architecture.    
- **Cooler, lighter Earthlikes**  
    Low-pressure, broad-skied worlds where cold-tolerant biomes thrive.
    
**All Geotics are Terrics**, but not all Terrics meet the tighter Geotic criteria.