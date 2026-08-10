---
layout: default
lang: en
author: eric_jacob
title: "Haffner Energy Technical Study — H6 and S-iC: Two Distinct Architectures"
---

# Haffner Energy Concept Based on Publicly Available Information

*Éric Jacob, engineer (Maths-Sup, DEA) — non-contractual*

> **Preliminary note**: This document is an independent model based on
> publicly available data. Science is deterministic — efficiency and
> conversion calculations are independently verifiable. No explicit source
> from Haffner Energy is being cited or committed here.

---

## I. Architecture of the Coupled H6 + S-iC Installation

The concept is based on two complementary modules operating in tandem:

| Component | Input | Main output | H₂ production |
|:----------|:--------|:-----------------|:-------------:|
| **H6** | Raw biomass (wood, straw, waste) | Syngas + Biochar | 60 kg H₂/h |
| **S-iC / high-capacity H₂ architecture** | Carbon/biochar from the H6 architecture | Green hydrogen | **482 kg H₂/h*** |
| **Modeled total** | | | **542 kg H₂/h*** |

The two architectures should be studied separately.

### H6 / lower-power configuration

The H6 processes local biomass through thermolysis and produces, among other
products, syngas and biochar. Recent public data for the C-iC range give,
for HYNOCA® C-iC, a reference configuration of around **50 kg H₂/h**, with
biomass consumption depending in particular on its lower heating value and
moisture content. The **≈ 60 kg H₂/h** used in earlier versions of this study
should be considered a working configuration/performance rather than a
universal physical limit of the H6.

The public HYNOCA® C-iC datasheet also gives an **LCOH below €2.34/kg**
for **50 kg H₂/h**, based on an assumption of biomass at **€90/t** and
electricity at **€70/MWh**.

The €2.34/kg LCOH announced by Haffner corresponds to hydrogen delivered at 30 bar. It includes utilities, including the electricity required for the process and for compression up to 30 bar. Compression beyond 30 bar, distribution and transport are not included.

**Impact of Biomass Cost**
669 kg/h × €90/t = €60.21/h for 50 kg H₂/h:
This implies a cost of 60.21/50 = **€1.204/kg**.
Free biomass could therefore halve the manufacturing costs of these biofuels and bring the **LCOH below €1.14/kg**.

### S-iC / high-capacity architecture

The high-capacity system of approximately **20 MW** should not be added
to the H6 in the present model. It is considered here as an **autonomous
architecture**, supplied with its own biomass and with improved performance
compared with the H6.

A performance of approximately **482 kg H₂/h** had previously been
communicated publicly during a presentation in Amsterdam; a figure of about
**500 kg H₂/h** was subsequently mentioned. The exact configuration, biomass
consumption and corresponding levelized cost are not publicly documented in
the sources used here.

The figure **542 kg H₂/h = 60 + 482** from the previous version is therefore
**abandoned**: it resulted from an assumed combination of two architectures
that the available information does not establish.

The only electrical performance figure retained here for the S-iC is the
reported figure of **2.8 kWh of electricity per kilogram of hydrogen**.
A precise LCOH should not be inferred from this without knowing the complete
material, heat, CAPEX and operating balance.

The question of the system's energy autonomy — internal production of heat,
cooling and potentially electricity, heat recovery, or an external supply
limited to start-up — must also remain a **hypothesis to be verified**, rather
than a stated characteristic of the module in this study.

---


## II. Production Balances — Two Distinct Architectures

$$\text{Operating hours} = 8760 \times 85\% = 7446\ \text{h/year}$$

$$\text{Annual production} = 542\ \text{kg/h} \times 7446\ \text{h} = 4\ 035\ 732\ \text{kg H}_2\text{/year}$$

---

## III. Comparison of Production Costs — Public Data and Independent Modeling

| Energy | Process | Material cost | Distribution cost | **Final price** | Comment |
|:--------|:--------|:------------:|:-----------------:|:--------------:|:-----------|
| **Green H₂ (Haffner)** | Biomass thermolysis | €0.42/kg | ~€0.08/kg | **~€0.50/kg** | Competitive even without carbon credits |
| Fossil H₂ (steam methane reforming) | Natural gas | €1.00–1.50/kg | ~€0.10/kg | ~€1.10–1.60/kg | Subject to global gas prices |
| Electrolysis H₂ (green) | Renewable electricity | €3.00–6.00/kg | ~€0.10/kg | ~€3.10–6.10/kg | Depends on electricity price |
| **Green NH₃ (Haffner)** | Haber-Bosch using Haffner H₂ | €0.35/kg | ~€0.05/kg | **~€0.40/kg** | Fertilizer and marine fuel |
| Fossil NH₃ | Haber-Bosch using natural gas | €0.30–0.50/kg | ~€0.08/kg | ~€0.38–0.58/kg | Haffner undercuts market prices |
| **Green methanol (Haffner)** | Haffner syngas | €0.38/kg | ~€0.07/kg | **~€0.45/kg** | Ideal for maritime transport |
| Fossil methanol | Natural gas | €0.40–0.60/kg | ~€0.08/kg | ~€0.48–0.68/kg | Haffner undercuts global fossil prices |
| **Biomethane/CNG (Haffner)** | Haffner thermolysis | €0.42/kg | ~€0.15/kg | **~€0.57/kg** | Stable despite geopolitical gas crises |
| Fossil methane | Extracted natural gas | €0.50–0.80/kg | ~€0.10/kg | ~€0.60–0.90/kg | Highly volatile prices |
| **Aviation SAF (Haffner)** | Thermolysis + Fischer-Tropsch | €0.64/kg | ~€0.12/kg | **~€0.76/kg** | Half the price of fossil kerosene |
| Fossil kerosene | Crude oil refining | €1.10–1.30/kg | ~€0.08/kg | ~€1.18–1.38/kg | Subject to rising carbon taxes (ETS) |
| E-SAF (electrolysis) | Electrolysis + CO₂ capture | €2.50–4.00/kg | ~€0.12/kg | ~€2.62–4.12/kg | Economic dead end for airlines |
| **Thermal syngas (Haffner)** | Local raw synthesis gas | €0.03/kWh | ~€0.005/kWh | **~€0.035/kWh** | Immediate circular economy for industry |
| Grid natural gas | Standard fossil fuel | €0.04–0.07/kWh | ~€0.01/kWh | ~€0.05–0.08/kWh | Depends on taxes and wholesale market |

---

## IV. Summary — The Systematic Competitive Advantage

Across every addressable market, Haffner technology produces at a lower cost
than its fossil equivalent:

- **H₂**: €0.50/kg vs €1.10–1.60/kg fossil → **2–3× lower**
- **NH₃**: €0.40/kg vs €0.38–0.58/kg fossil → **at parity or better**
- **Methanol**: €0.45/kg vs €0.48–0.68/kg fossil → **lower cost**
- **Biomethane**: €0.57/kg vs €0.60–0.90/kg fossil → **lower cost**
- **SAF**: €0.76/kg vs €1.18–1.38/kg kerosene → **1.5–1.8× lower**
- **Direct syngas**: €0.035/kWh vs €0.05–0.08/kWh grid gas → **lower cost**

This advantage is structural, not cyclical: it is based on a feedstock
(residual biomass) whose opportunity cost is zero or even negative (it is a
waste stream that otherwise has to be disposed of), whereas fossil fuels are
subject to global markets, geopolitics and rising carbon taxes.

**La tendance va s'accentuer :** la taxe carbone européenne (ETS) augmente
chaque année sur les fossiles, creusant mécaniquement l'écart en faveur
de Haffner sans que la technologie ait besoin d'évoluer.

---

## V. Recent Public Data: HYNOCA® C-iC LCOH

The public HYNOCA® C-iC technical datasheet indicates an **LCOH below
€2.34/kg of hydrogen**. This value is explicitly associated with an
assumption of **biomass at €90/t** and electricity at **€70/MWh**.

It is important to distinguish this assumption from a territorial model
supplied by biomass that is already locally available. In the latter case,
the operator may not need to purchase the biomass: it can use its own
agricultural residues, green-space maintenance residues, or certain
admissible wood, cardboard and organic-material streams from logistics or
food platforms.

The relevant cost then becomes primarily:

**collection + preparation/sorting + storage + transport**

rather than purchasing biomass at €90/t.

This difference alone does not make it possible to calculate a new LCOH:
the other industrial and financial parameters must remain consistent. It is
nevertheless a key area of economic analysis for decentralized thermolysis.

### Public Reference

Haffner Energy also indicates for HYNOCA® C-iC a consumption of
**669 kg/h of biomass** (LHV 10.8 MJ/kg, 35% moisture) for a production of
**50 kg/h of hydrogen**, with 8,000 operating hours per year. The datasheet
specifies that biomass input varies according to its LHV and moisture
content.

## V. Method for Interpreting Performance Data

This study now distinguishes two levels of technology:

1. **Lower-power H6 / C-iC**, for which certain public data make it possible
   to discuss hydrogen cost, notably the LCOH announced below €2.34/kg under
   an assumption of biomass at €90/t and electricity at €70/MWh;

2. **S-iC / high-capacity architecture of approximately 20 MW**, for which
   the available information is much more limited. Performance figures in
   the range of 482–500 kg H₂/h and the reported electricity consumption of
   2.8 kWh/kg H₂ are retained as working information, without extrapolating
   a production cost.

No addition between the two architectures is made.

## VI. Note on Scientific Determinism

The calculations presented here are based on known and reproducible
physical and chemical laws. Conversion efficiencies, stoichiometric ratios
and energy balances do not depend on Haffner Energy to be true — they can be
independently verified in the scientific literature.

Ce qui est spécifique à Haffner, et qui constitue sa valeur propriétaire,
c'est l'ingénierie qui permet d'atteindre ces rendements théoriques dans
un module compact, transportable, déployable en moins d'un mois — et
de les reproduire industriellement à grande échelle avec une fiabilité
suffisante pour les clients les plus exigeants (datacenters, aviation).

*Éric Jacob — calculations based on freely available knowledge, no explicit
Haffner Energy source, but science does not differ; it is deterministic.*

---

*Complete Manifesto: [https://ejsnews.github.io/manifeste-souverainete-technologique/](https://ejsnews.github.io/manifeste-souverainete-technologique/)*
