---
layout: default
lang: en
author:	eric_jacob
title: "Economic Modeling - H6 + S-iC Installation and Syngas Derivatives"
---

# Economic Modeling - H6 + S-iC Installation and Syngas Derivatives [(French version - FR)](Modelisation_economique_-_installation_H6_et_S-iC_et_derives_du_Syngas.md)

*Independent modeling based on Haffner Energy's public data - Éric Jacob, Engineer (Maths-Sup, DEA)*

> **Methodological Warning**: This document is an independent modeling > based on publicly available data (press releases, patents,
> shareholder webinars). The figures are estimates to be confirmed by
> Haffner Energy. Assumptions are made explicit for each calculation.
> This document also compiles publicly available technical data
> on hydrogen storage. Efficiency figures vary significantly
> depending on the source - sometimes by a factor of three - reflecting a real
> and unresolved technical debate. Ranges are presented
> honestly rather than smoothed.

---

## I. Fundamental Chemistry - The Syngas Equations

### The syngas produced by Haffner is a mixture of H₂ and CO. It is the platform molecule that allows the synthesis of all derivatives:

**Green Hydrogen** (direct separation):

$$\text{Syngas} \xrightarrow{\text{separation}} \text{H}_2 + \text{CO}$$

**Ammonia** (Haber-Bosch process):

$$3\text{H}_2 + \text{N}_2 \xrightarrow{400-500°C,\ 150-250\ bar} 2\text{NH}_3$$

**Biodiesel/SAF** (Fischer-Tropsch synthesis):

$$n\text{CO} + (2n+1)\text{H}_2 \xrightarrow{\text{cobalt/Fe}} \text{C}_n\text{H}_{2n+2} + n\text{H}_2\text{O}$$

**Methanol**:

$$\text{CO} + 2\text{H}_2 \xrightarrow{250°C,\ 50\ bar} \text{CH}_3\text{OH}$$

**Synthetic Methane / Biomethane** (Sabatier process - confirmed at Haffner):

$$\text{CO} + 3\text{H}_2 \xrightarrow{\text{Ni},\ 300-400°C} \text{CH}_4 + \text{H}_2\text{O}$$

### In addition to the identified derivatives (H₂, NH₃, SAF, methanol, methane), Haffner Energy is open to other molecules of interest derived from syngas:

**Dimethyl Ether (DME)** - clean diesel fuel, derived from methanol:

$$2\text{CH}_3\text{OH} \xrightarrow{\text{Al}_2\text{O}_3,\ 250°C} \text{CH}_3\text{OCH}_3 + \text{H}_2\text{O}$$

**Urea** (stable solid fertilizer, direct derivative of ammonia):

$$2\text{NH}_3 + \text{CO}_2 \xrightarrow{180°C,\ 150\ bar} \text{CO(NH}_2)_2 + \text{H}_2\text{O}$$

**Nitric Acid** (alternative nitrogen pathway, NPK fertilizers, civilian applications):

$$4\text{NH}_3 + 5\text{O}_2 \xrightarrow{\text{Pt/Rh},\ 800°C} 4\text{NO} + 6\text{H}_2\text{O}$$

**LOHC - Methylcyclohexane** (liquid storage at atmospheric pressure):

$$\text{Toluene} + 3\text{H}_2 \xrightarrow{\text{Pt/Pd catalyst}} \text{Methylcyclohexane}$$

---

## II. Pathways to Explore for Hydrogen Storage

### The Reference Problem: 350-700 bars

Gaseous compression storage, although the current industrial standard, requires heavy and expensive tanks (particularly carbon fiber) for limited volumetric energy density (~1.3 kWh/L at 700 bars, compared to ~9.7 kWh/L for gasoline). Cryogenic liquefaction is a serious technical pathway, but this relative weakness is not insurmountable: hydrogen offers a mass energy density three times higher than fossil fuels, not to mention its major advantages in terms of sovereignty and decarbonization. Haffner Energy even enables consideration of massive and low-carbon production. If volumetric storage remains a lock to be lifted, hydrogen's competitive advantage would become definitive with the emergence of new solutions. This is why it is essential to support research, particularly in innovative SMEs, rather than weakening a sector that is already overcoming its technical obstacles step by step.

### Pathway 1 - Storage via Ammonia (already in the Haffner ecosystem)

**Synthesis (Haber-Bosch):**

$$3\text{H}_2 + \text{N}_2 \xrightarrow{400-500°C,\ 150-250\ bar} 2\text{NH}_3 \quad (\eta = 70-75\%)$$

**Cracking (H₂ release):**

$$2\text{NH}_3 \xrightarrow{\text{catalyst},\ 400-600°C} 3\text{H}_2 + \text{N}_2$$

**Storage Advantage:** Liquid ammonia is stored at only **8-10 bars**

at ambient temperature (like LPG), versus 700 bars for pure H₂ - a considerable pressure gain, with a volumetric energy density 40% higher than liquid hydrogen.

**The Round-Trip Efficiency Debate:**

| Source | Announced Round-Trip Efficiency | Context |
|:-------|:-------------------------------:|:---------|
| CSIRO (Australia) | 76% cracking only / losses 1.41 MWh/tonne | Best optimized catalytic case |
| DOE / ESI 2026 | 60-70% (Haber-Bosch + cracking) | H2A v3.2 thermodynamic reference |
| CleanTechnica (critical analysis) | Only 20-30% | Includes final compression + fuel cell |
| Kleinman Energy (Penn) | 0.88-1.76 MWh/tonne NH₃ for cracking | Depending on catalytic technology |

**Why such a gap?** Optimistic figures (60-76%) measure

only synthesis + cracking. Pessimistic figures (20-30%) integrate
the entire chain up to the wheel of a fuel cell vehicle, where
losses accumulate: Haber-Bosch (25-30% loss) + cracking (15-40% loss) + final compression + fuel cell efficiency (50-60%).

**Estimated Additional Cost:** €0.50 to €1.00/kg H₂ for round-trip transformation, even before the CAPEX of cracking installations.

### Pathway 2 - Liquid LOHC (Liquid Organic Hydrogen Carriers)
$$\text{Toluene} + 3\text{H}_2 \rightleftharpoons \text{Methylcyclohexane}$$

**Advantage:** Transported like diesel in existing petroleum infrastructure,
at atmospheric pressure, long-term storage
without loss (unlike liquid H₂ which has continuous "boil-off").

**Disadvantage:** Generally lower efficiency than ammonia according
to several comparative analyses, and requires toluene recycling
(return infrastructure for the dehydrogenated carrier vehicle).

### Pathway 3 - Solid Metal Hydrides

$$\text{Mg} + \text{H}_2 \rightleftharpoons \text{MgH}_2$$
Storage at near-zero pressure, high volumetric density, but requires
thermal input (~300°C) for release - relevant for stationary storage
(datacenter, industrial site) rather than mobility.

### Pathway 4 - Exploratory Hypothesis: Structural Mesh Without Chemical Transformation

The idea mentioned - a material that "stores" hydrogen in a reduced volume under high pressure without chemically transforming it - actually corresponds to the principle of **MOFs (Metal-Organic Frameworks)**: nanoporous crystalline structures that physically adsorb H₂ in their pores (physisorption), without chemical reaction, therefore without energy conversion loss.

**Major Theoretical Advantage:** no Haber-Bosch, no cracking, therefore no loss of the 25-40% inherent to the ammonia pathway. Hydrogen remains H₂, simply compressed in a porous structure at lower pressure than an empty tank.

**Current Limit:** The most efficient MOFs achieve storage capacities still insufficient at ambient temperature to compete
with 700 bars in automotive use - research is active but not yet industrially mature. It is a research pathway, not a solution available today.

*This is a research hypothesis, not a deployed technology. But it
deserves to be explored with specialized laboratories (CNRS, CEA) if
Haffner wishes to explore a storage pathway without chemical transformation.*

---

## III. Applications by Mode of Transport - Which Vector for Which Use?

| Use | Recommended Vector | Justification |
|:------|:-------------------|:---------------|
| Light vehicle (car) | Compressed H₂ 700 bars | Existing infrastructure, fast refueling |
| Long-distance heavy truck | Compressed H₂ or ammonia | Depending on station availability on route |
| Ship (cargo, ferry) | **Direct Ammonia** (dedicated engine) | No cracking needed - direct NH₃ combustion possible |
| Airplane (SAF) | **Liquid SAF** (Fischer-Tropsch) | High mass energy density, existing airport infrastructure |
| Stationary storage (datacenter, factory) | Metal hydrides or ammonia | No onboard weight constraint |
| Electricity grid (back-up) | Direct H₂ fuel cell | Best efficiency without conversion step |

**Key Point for Ships:** Several shipyards are already developing direct ammonia combustion engines (without prior cracking), which avoids the 25-40% loss of cracking. This is the most mature pathway for decarbonized maritime transport by 2027-2030.

---

## IV. Comparative Synthesis of Vectors

| Criterion | Compressed H₂ 700 bars | Ammonia (NH₃) | LOHC (methylcyclohexane) | Metal Hydride |
|:--------|:---------------------:|:---------------:|:-------------------------:|:-------------------:|
| Storage Pressure | 700 bars | 8-10 bars | Atmospheric | Near-zero |
| Volumetric Energy Density | Low | High (+40% vs liquid H₂) | Medium | High |
| Round-Trip Efficiency | Reference (100%) | 20-76% (technical debate) | 60-70% estimated | 70-85% estimated |
| Existing Infrastructure | Dedicated stations | Existing LPG/ammonia | Petroleum (adapted) | None (to be created) |
| Round-Trip Conversion Cost | None | €0.50-1.00/kg | Variable | Variable |
| Best Use | Light mobility | Maritime, long-term storage | Long-distance transport | Stationary |

---

There is no universally superior hydrogen vector - each
molecule derived from Haffner syngas (pure H₂, ammonia, methane, methanol,
SAF) has a use where it is optimal. The versatility of Haffner technology
precisely allows choosing the right vector according to the final market,
rather than imposing a single solution on all uses.
The pathway of porous materials (MOF) for storage without chemical
transformation remains the most promising in the long term to eliminate conversion
losses - but it is still at the stage of fundamental research.

---

## V. H6 + S-iC Architecture - Modeling Assumptions

### Studied Configuration

The economic image published by Haffner Energy shows a coupled H6 + H4 (S-iC) installation. Here is the architecture as modeled:

| Component | Role | H₂ Production |
|:----------|:-----|:-------------:|
| H6 | Raw biomass thermolysis → syngas + biochar | 60 kg H₂/h |
| S-iC (improved H4) | Receives biochar from H6, advanced valorization | 482 kg H₂/h |
| **Total installation** | | **542 kg H₂/h** |

**Assumption on H6/S-iC ratio**: the S-iC receives biochar, not raw biomass.

If one H6 produces ~200-350 kg of biochar/tonne of biomass, and the S-iC
processes 482 kg H₂/h, it is estimated that **4 to 5 H6 modules** are needed to continuously feed
one S-iC. *To be confirmed by Haffner Energy.*

### Annual Availability

$$\text{Operating hours} = 8760 \times 85\% = 7446\ \text{h/year}$$

$$\text{Annual H}_2\ production = 542\ \text{kg/h} \times 7446\ \text{h} = 4\ 035\ 732\ \text{kg H}_2\text{/year}$$

---

## VI. Scenario A - Green Hydrogen Production (Reference)

This is the base scenario of the economic image published by Haffner:

| Parameter | Value |
|:----------|:------:|
| Annual H₂ Production | 4 035 732 kg |
| Minimum Selling Price | €6.50/kg |
| **Annual Revenue** | **€26 232 258** |
| Total OPEX (H6 + S-iC + maintenance) | €2 600 888 |
| **Annual Net Gain** | **€23 631 370** |
| Estimated CAPEX | €5 000 000 |
| **Amortization** | **< 3 months** |

---

## VII. Scenario B - Green Ammonia Production (Fertilizers)

### Scientific Data

- Haber-Bosch process: 3 mol H₂ + 1 mol N₂ → 2 mol NH₃
- Mass ratio: **1 kg H₂ → 5.65 kg NH₃**
- Energy required: 14-15 kWh/kg NH₃ (provided by the syngas itself)
- H₂ → NH₃ conversion efficiency: 76%

### Calculation on H6 + S-iC Installation

$$\text{Available H}_2 = 4\ 035\ 732\ \text{kg/year}$$

$$\text{NH}_3\ produced = 4\ 035\ 732 \times 0{,}76 \times 5{,}65 = 17\ 321\ 073\ \text{kg NH}_3\text{/year}$$

| Parameter | Value |
|:----------|:------:|
| Annual NH₃ Production | ~17 300 tonnes |
| Green NH₃ Market Price | €400-600/tonne |
| **Annual Revenue** | **€6.9 – €10.4 M** |
| Fertilizer Equivalent (urea) | ~22 000 tonnes urea |
| Agricultural Area Covered | ~15 000 ha of cereals |

> **Note**: Ammonia revenue is lower than pure hydrogen (€6.50/kg),
> but ammonia is easier to store and transport. The choice between
> the two depends on the local market.

---

## VIII. Scenario C - Biodiesel/SAF Production (Fischer-Tropsch)

### Scientific Data

- Biomass → FT liquids yield: **15-28% by mass** according to literature
- 1 tonne of biomass at 30% moisture → **159 liters of biodiesel** (ScienceDirect)
- FT-diesel calorific value: 43-45 MJ/kg (higher than fossil diesel)
- Overall FT yield: 40-51% of initial biomass energy

### Calculation on H6 Installation (alone, without S-iC)

In Fischer-Tropsch mode, syngas is directed toward FT synthesis rather than H₂ separation. We model on the H6 alone (60 kg H₂/h):

$$\text{Biomass processed H6} \approx 1\ \text{tonne/h} \times 7446\ \text{h} = 7446\ \text{t/year}$$
$$\text{Biodiesel produced} = 7446 \times 159\ \text{L} = 1\ 183\ 914\ \text{L/year}$$

| Parameter | Value |
|:----------|:------:|
| Annual Biodiesel Production | ~1 184 000 liters |
| Biodiesel/SAF Market Price | €1.20-1.80/L |
| **Annual Revenue (H6 alone)** | **€1.4 – €2.1 M** |
| Kerosene Equivalent Substituted | ~950 tonnes |
| CO₂ Reduction vs Fossil Kerosene | ~2 500 tCO₂/year |

---

## IX. Scenario Comparison - Summary Table

| Scenario | Product | Estimated Annual Revenue | Priority Market |
|:---------|:--------|:------------------------:|:---------------|
| A | Green Hydrogen | €23.6 M net | Datacenters, H₂ mobility |
| B | Green Ammonia | €6.9 – €10.4 M | Agriculture, fertilizers |
| C (H6 alone) | Biodiesel/SAF | €1.4 – €2.1 M | Aviation, heavy transport |
| A+B Mixed | H₂ + NH₃ | Variable according to ratio | Multi-use territory |

> **Observation**: Scenario A (pure hydrogen) is the most profitable in the short
> term. Scenario B (ammonia) is the most sovereign (local fertilizers).
> Scenario C (SAF) is the most relevant for aviation. A Haffner module
> can switch from one mode to another according to local demand.

---

## X. Mobility Demonstration - H₂ vs Gasoline

Based on the BMW iX5 Hydrogen (750 km / 7 kg H₂) with Haffner H₂ at €1.50/kg:

| Parameter | Gasoline Vehicle | BMW iX5 (Haffner H₂) |
|:----------|:----------------:|:--------------------:|
| Fuel Energy Density | 12.2 kWh/kg | **33.3 kWh/kg** |
| Engine Efficiency | 30-35% | **50-60%** (fuel cell) + >90% (motor) |
| Consumption/100 km | 6.5 L | **0.93 kg H₂** |
| Fuel Price | €1.70/L | **€1.50/kg** (local Haffner) |
| **Real Cost/100 km** | **~€11.05** | **~€1.40** |
| **Economy Factor** | reference | **×7.9 cheaper** |

$$\text{Annual Savings (20 000 km)} = (11{,}05 - 1{,}40) \times 200 = 1\,930\ \text{€/year/vehicle}$$

---

## XI. The Reinforcement Loop - Why Demand Self-Amplifies

It is not technology alone that creates economic value - it is the combination of four factors that reinforce each other:

**Low price** → accessible to a mass market (local authorities, SMEs, cooperatives), not reserved for large industrial groups only.

**Transportability** (2 MW module on truck, without exceptional convoy) → deployment in a few weeks, without centralized construction or heavy civil engineering.

**Usage versatility** (H₂, NH₃, SAF, methane, methanol, and other molecules to come) → a single industrial investment serves several markets simultaneously, reducing commercial risk for the buyer.

**Low CAPEX and rapid amortization** (< 3 months on the hydrogen scenario) → accessible to actors who could never have financed a classic centralized plant.

**The result is a self-sustaining loop:** more modules deployed → more industrial feedback → even lower manufacturing costs → even wider demand → new R&D investments to expand the range of produced molecules. It is a virtuous circle that oil
never needed to create, since it was already available in mass and geographically concentrated.

### Reliability through Redundancy: The Decisive Argument for Datacenters

The choice of unitary 2 MW modules rather than a monolithic 20 MW plant is not just a logistical advantage - it is a structural reliability argument. An installation of 10 to 20 modules of 2 MW, organized according
to the N+1 principle, never experiences a total shutdown: the failure or maintenance
of a single module only marginally reduces available power, whereas
a monolithic plant in shutdown is completely stopped.
Haffner seems to be durably orienting toward this modular model - confirmed by
the adaptation of the CORE100 program to demands for multi-
module configurations. This is precisely what AI datacenters require: a plant
that never stops, transportable, repairable module by module without
interrupting overall production.

---

## XII. Macroeconomic Impact France - Expanded Scenario to Future Molecules

The hydrogen-only scenario (10 000 H6+S-iC installations) underestimates
the real impact if we integrate the growing versatility of the technology.
Haffner Energy continuously expands its product range to meet
its clients' needs - synthetic methane and methanol are already
mentioned in its official communications, and other molecules
(DME, urea, nitric acid) are chemically accessible from the
same syngas without changing the technological core.

| Scenario | H₂ Alone | H₂ + NH₃ + CH₄ + SAF Mixed (estimated) |
|:---------|:-------:|:-------------------------------------:|
| Revenue Generated (10 000 installations) | €260 Bn/year | €320-380 Bn/year |
| Reduction in Fossil Imports | -€40 to -€60 Bn/year | -€70 to -€100 Bn/year |
| Reduction in Nitrogen Fertilizer Imports | Not counted | -€8 to -€12 Bn/year |
| Direct Jobs Created | 200 000 – 400 000 | 300 000 – 500 000 |
| CO₂ Sequestered (biochar) | 50-80 million tCO₂/year | 50-80 million tCO₂/year (unchanged) |

**Why this expanded range is plausible:** each installation
can dynamically switch between several products according to local demand
and market prices - an agricultural territory will favor ammonia and
urea, a logistics hub will favor hydrogen for its fleets, a coastal area near a port will favor SAF or maritime methanol.
This flexibility multiplies outlets without multiplying industrial investments.

> **Methodological Note**: These figures remain linear extrapolations
> for illustrative purposes. Actual deployment depends on available biomass resources
> (several hundred million tonnes in France), the pace of Haffner Energy's industrialization,
> and regulatory developments
> (fast-track ICPE in particular). Several molecules listed here (DME, nitric acid) are not yet confirmed in Haffner Energy's commercial catalog - they are chemically accessible from syngas, which does not
> guarantee their future industrial development.

---

## Conclusion

The Haffner economic model is remarkable for its versatility: the same
technological platform can produce, according to local needs, hydrogen,
ammonia, biodiesel or SAF - without modifying the core of the technology.
This flexibility is unique in the world. It allows each territory to choose
the product that corresponds to its priority needs: mobility, agriculture,
aviation or energy - with a return on investment in all cases
under 3 months for an H6+S-iC installation.

---

