# Planning A Detailed Atmosphere

## Why Go Deeper Than The Basic Geotic Model?

You don’t *have to* go beyond the basic Geotic model — unless, of course, your players or readers are the kind who pull out calculators and gleefully point out why your planemon’s air shouldn’t work.

If you’re the kind of worldcrafter who likes knowing how things *actually work* (or just wants to stay one step ahead of the smart alecks), this Sidebar Module walks you through the fundamentals of atmospheric plausibility.

We're sticking to **generally habitable atmospheres** here — ones that humans or near-humans could plausibly breathe. But the core principles apply no matter how exotic you want to get.

- **Average atmospheric pressure (atm)**
	- Range: atm ∈ ⟨0.5 ∧ 2.0⟩
	-  Supports oxygen respiration and liquid water without requiring pressure suits or extreme acclimatization
- **Atmospheric Scale Height (H)**
	- H ∈ ⟨6 ∧ 12⟩ km
	- Governs pressure drop with altitude
	- Affects breathing, mountain height, and high-altitude flight
	- See below for details
- **Average atmospheric composition**
	- Oxygen
		- Range: O₂ ∈ ⟨15% ∧ 30%⟩
			-  > 30% even damp fuel ignites more easily, and spontaneous combustion becomes a risk
			-  < 15% requires acclimation or enhanced lung capacity (for any creature not evolved in the environment)
		 - Needed for aerobic respiration
	 - Buffer Gas
		-  Range:  ∈ ⟨70% ∧ 85%⟩
		- The chemically inert or low-reactivity bulk gas that fills out the atmosphere around oxygen
		- Defines overall *atmospheric* density, scale height, sound propagation, and temperature response
		- Nitrogen (N₂) and Argon (Ar) are your only reliable options
			- Other candidates (neon, helium, etc.) are too rare, too light, or too toxic
	- Trace Gases
		-  < 1%
		-  H₂O vapor, O₃, CH₄
		-  CO₂ ideally should comprise < 0.04%
		-  Required for climate regulation (greenhouse effect), UV shielding, biodynamics

## More About Scale Height

As related above, the atmospheric scale height (H)
	- Governs pressure drop with altitude
	- Affects breathing, mountain height, and high-altitude flight

However, the value of H varies with the composition of the atmosphere because the ***molecular mass*** is different for each component gas and is not a constant.

> **Hippy**: You need to calculate H based on how much O₂, buffer gas, etc. your atmosphere has.

Exactly!  So, how do you do that?

### Calculating Scale Height

Scale height (H) depends on:
- **T** = average temperature of the atmosphere (in Kelvin)
- **M** = mean molar mass of the gas mixture (in kg/mol)
- **g** = surface gravity (in m/s²)
- **R** = universal gas constant ≈ 8.314 J/mol·K

... related in the equation:

$$
H = \dfrac{R T}{M g}
$$
#### First

Find the mean molecular (molar) mass M.  Each gas in the atmosphere contributes to the average molar mass based on its ***mole fraction***:

$$
M = \sum{x_i M_i}
$$
> **Keppy**: *DON'T PANIC*!  That Σ might *look* like calculus, but it's not... all it's saying is that we sum up the molar masses of all the gasses present

Yes, in the above equation:
- $x_i$ is the **mole fraction** of each atmospheric gas (in Earth's case, that's 0.78 for N₂; 0.21 for O₂)
- $M_i$ is the molar mass of the gas in question.

Let's use Earth's atmosphere as an example:
- Atmosphere = 78% N₂, 21% O₂, 1% Ar  (using kg/mol):  
- $M_{N_2} = 0.028014$  
- $M_{O_2} = 0.031998$
- $M_{Ar} = 0.039948$
	- We lump argon in with the trace gasses in Earth's case

$$
M = (0.78 \times 0.028014) + (0.21 \times 0.031998) + (0.01 \times 0.039948) = 0.02896 \text{ kg/mol}​
$$

> **Keppy**: Where did 0.028014, and the other numbers come from?

Well spotted!

Each gas has a known molar mass — the mass of one ***mole*** of its molecules — and it's typically expressed in grams per mole (g/mol). Since we’re working in SI units, we convert those to kilograms per mole (kg/mol) by dividing by 1000.  And we look those numbers up in an appropriate (and reliable) source.  Here are a few for reference:

| Gas            | Chemical Formula | Molar Mass (g/mol) | Molar Mass (kg/mol) |
|----------------|------------------|--------------------|---------------------|
| Nitrogen       | N₂               | 28.014             | 0.028014            |
| Oxygen         | O₂               | 31.998             | 0.031998            |
| Argon          | Ar               | 39.948             | 0.039948            |
| Carbon Dioxide | CO₂              | 44.01              | 0.044010            |
| Water vapor    | H₂O (gas)        | 18.015             | 0.018015            |
| Methane        | CH₄              | 16.043             | 0.016043            |
| Helium         | He               | 4.003              | 0.004003            |

> **Hippy**: And you use these values in your atmosphere recipe to get your average molar mass.

Exactly! Once you've built your mix — say, 75% N₂ and 25% O₂ — just multiply each molar mass by its fraction and sum the results.

> **Keppy**: Seems like that equation could get lengthy and complex.

You are *not* wrong about that.  Getting warm and friendly with a spreadsheet or a programmable calculator is very good advice for the serious worldcrafter, for sure.

#### Second

Now that we have our value for M, we plug it into our other *known* values for R (8.314), T (288), and g (9.8) and get:

$$
H=\dfrac{R T}{M g} = \dfrac{8.314 \times 288}{0.02896 \times 9.8} = \dfrac{2395.6}{0.2838} = 8.44\text{ km},
$$

... which is usually rounded up to H = 8.5 km for convenience, but you can use the more exact value if you prefer.

> **Hippy**: T = 288 K is for Earth.  How does one determine it for a 'crafted planemon?

Ah — excellent question.  

The **average surface temperature** T depends on factors like:
- The **luminosity and spectral class** of the central star(s)
- The **orbital distance** of the planemon
- The planemon’s **albedo** (reflectivity)
- And any **greenhouse effects** caused by atmospheric composition    

That starts to pull us into stellar physics and orbital modeling, which is covered in:

> 🔗 **Module XY.Z — Building Your Star and Setting Your Orbit**

There, you'll find methods for estimating a planemon's **equilibrium temperature** and adjusting it for greenhouse gases to get a realistic T for your atmosphere model.

For now, if you're working with a roughly Earthlike setup, using:

$$
T ∈ \langle260 \wedge 320\rangle K,
$$
or roughly ⟨-13° ∧ 47°⟩C  will keep your numbers in a plausible range.

Here's some context for that range:

> - 260K (-13°C; 8.6°F)
> 	- Close to the freezing point of seawater
> 	- Sustained habitability without deep-cold adaptation is still possible
> - 273K (0°C; 32°F)
> 	- Freezing point of water
> 	- Important psychological and ecological threshold
> - 288K (15°C; 59°F)
> 	- Earth's average
> 	- Serves as benchmark for climate comfort and live-rich biomes
> - 310K (37°C; 98.6°F)
> 	- Human core temperature
> 	- Upper limit for comfort under heavy exertion
> - 320K (47°C; 116.6°F)
> 	- At or above this, heat stress becomes deadly without rapid evaporative cooling or climate control.

> ❗️ Important note: IF you *choose* a surface temperature for your world, be sure to note it down, because it will help *determine* your star's parameters later!

> **Keppy**: So, back to atmospheric composition: If you used argon instead of nitrogen as your buffer gas, the air would be heavier and H would shrink?

Exactly. More mass = more gravity per mole = thinner vertical spread = smaller H.

> **Keppy**: And in this case, we're just ignoring the trace gasses altogether?

 Mostly, yes — and here’s why:

Trace gases like CO₂, CH₄, and H₂O vapor are typically present in such **small quantities** (fractions of a percent) that they **barely shift the weighted average** of molar mass.

Let’s say your atmosphere is:
- 78% N₂ (0.028014 kg/mol)
- 21% O₂ (0.031998 kg/mol)
- 1% CO₂ (0.04401 kg/mol)

$$
M = (0.78 \times 0.028014) + (0.21 \times 0.031998) + (0.01 \times 0.04401) = 0.02899 \text{ kg/mol}​
$$

That’s a difference of only **+0.00003** compared to Earth-normal — **Less than a tenth of a percent.**  So, unless you’re at CO₂ levels high enough to make the air toxic or unbreathable, it’s safe to treat the trace gasses as negligible in the **H** calculation.

> **Hippy**: So just include the big players — buffer gas and oxygen — and don’t sweat the tenths of a percent?

Bingo. You can always do a full weighted sum if you really want to be *precise*, but for 99% of cases, O₂ and the buffer gas dominate the molar mass *for Geotic worlds*.

#### Third: Pressure vs. Altitude Approximation

For Earth:

$$
P(h) = P_0 \times 0.37^{\frac{h}{H}}
$$

Where:
- h = altitude in kilometers
- H = 8.5 (or 8.44) km

> **Keppy**: What is P₀, and how do we know its value?

Precisely the question I'd ask at this point!

P₀​ is the **surface pressure** of the planemon — that is, the pressure at **zero altitude**. On Earth, that value is defined as:
- 1 atm
- 101325 Pa*
- 101.325 kPa

\* Named for Blaise Pascal; there's not space here to go into this in detail, but it's a fascinating read if you want to look it up!

For any world you create, P₀​ is one of your **starting parameters**. You either:
- **Choose it** (e.g., 1.2 atm, or 0.65 atm), or
- **Derive it** from known gas composition, temperature, and gravity (which gets more advanced)

So, let's say you've chosen P₀ = 0.9 atm for your planemon, then at one scale height above the planemon's surface, the atmospheric pressure calculates to:

$$
P(H) = 0.9 \times 0.37 = 0.333\text{ atm}
$$
> **Hippy**: Which raises the question of where 0.37 comes from?

Excellent question. That 0.37 isn’t arbitrary — it’s actually derived from a **fundamental mathematical constant**: Euler’s number, e (≈ 2.71828).

The **pressure–altitude relationship** is an ***exponential decay*** equation. In its most general form:

$$
P(h) = P_0 \times e^{\frac{-h}{H}}
$$
... which means that at an altitude of exactly one scale height (where *h* = *H*):

$$
P(H) = P_0 \times e^{-1} = P_0 \times 0.3679 
$$
> **Keppy**: Ah!  I see... and P₀ is just whatever multiple of Earth's surface pressure in atm you've chosen for your world!

> **Hippy**: I always frown at "chosen"; is there any way to at least *approximate* an appropriate P₀ for your planemon based on how you decided to compose its atmosphere?

Well.... yes.... sort of.

You *can* approximate $P_0$​ from first principles — and it's especially useful if you've already defined your atmosphere’s:
- **Gas composition** (molar mix)
- **Surface gravity** (g)
- **Average temperature** (T)

... and rearranging the ***ideal gas law*** for planemon atmospheres:

$$
P_0 = \dfrac{\rho R T}{M}
$$
But this requires knowing ρ, the **near-surface air density** — which in turn depends on pressure and composition, so we go a different route.

Instead, for an atmosphere in hydrostatic equilibrium, you can approximate:

$$
P_0 ≈ \dfrac{g M N}{A}
$$
Where:
- g = surface gravity
- M = average molar mass (kg/mol)
- N = total moles of atmosphere
- A = surface area of the planemon

But this, too, gets messy without knowing how much gas the planemon *started with*, which is based on accretion, outgassing, escape velocity, etc.

So while you *can* try to derive it from theory — and I can help you do that — you’re usually safe choosing a $P_0$ based on:
- Your world’s **gravity** (g)
- Its **escape velocity** (vₑ)
- Its **molar mass and buffer gas makeup** (M – which we learned how to calculate above.)

Here's a "pressure plausibility chart" based on gravity and atmosphere type to give you an other "rule of thumb" to work from:

### 🌍 Pressure Plausibility Chart

*Rule-of-thumb surface pressures based on gravity and buffer gas makeup (M)*

| **Gravity**<br>(g in g⨁) | **Likely Pressure<br>Range (atm)** | **Notes**                                                                               |
| :------------------------: | :----------------------------------: | --------------------------------------------------------------------------------------- |
| 0.5                      |            ⟨0.2 ∧ 0.6⟩             | Light gravity;<br>thinner atmosphere unless<br>retained via cold temps or high mass gas |
| 0.75                     |            ⟨0.4 ∧ 0.9⟩             | On the thin side but potentially<br>breathable; requires attention to O₂ %              |
| 1.0                      |            ⟨0.8 ∧ 1.2⟩             | Earth-normal, depending on<br>mix of gases and water vapor                              |
| 1.25                     |            ⟨1.0 ∧ 1.5⟩             | Denser air; easier to retain<br>light gases like H₂O, CH₄                               |
| 1.5                      |            ⟨1.2 ∧ 2.0⟩             | Heavy air; pressure at sea level<br>could approach adaptation limits                    |

This assumes (!) an Earth-like atmosphere:
- Mean molar mass ≈ ⟨0.028 ∧ 0.032⟩ kg/mol
- Normal temperature (~288 K)
- Terrestrial radius (~1⨁)

You'll need to shift values worlds with high CO₂, significant greenhouse buildup, or non-volatile-rich origins, but the above should be well within bounds for *Geotic worlds*.
