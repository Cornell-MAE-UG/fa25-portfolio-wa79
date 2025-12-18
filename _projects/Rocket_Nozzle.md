---
layout: project
title: Mojave Sphinx Rocket Nozzle 
description: Rocket Nozzle of Mojave Sphinx
technologies: [Fusion 360]
image: /assets/images/nozzle2.png
---
Mojave Sphinx is a high-power amateur rocket powered by a liquid bipropellant engine using nitrous oxide as the oxidizer and compatible hydrocarbons (e.g., ethanol) as fuel. It was designed and proposed by Half-Cat Rocketry to provide a relatively simple and economical platform for new teams to gain practical experience in designing, manufacturing, and testing liquid rockets within a realistic student budget and timeline.

A key thermodynamic component of the Mojave Sphinx propulsion system is the converging–diverging (C–D) nozzle located downstream of the combustion chamber. The primary function of the nozzle is to convert the high-temperature, high-pressure combustion products into directed kinetic energy by accelerating the flow to high velocity.

Hot gases leaving the chamber enter the converging section of the nozzle. Under subsonic conditions, decreasing cross-sectional area increases velocity and decreases static pressure. At the smallest cross-sectional area (the throat), the flow becomes choked and reaches Mach 1 when the chamber-to-ambient pressure ratio is sufficiently high.

Beyond the throat, the nozzle diverges. In the supersonic region, the area–velocity relationship reverses: increasing cross-sectional area accelerates the supersonic flow further while its static pressure and temperature decrease. This geometry converts internal energy and pressure into exhaust kinetic energy. The resulting high-velocity jet produces thrust primarily through momentum exchange, accelerating the rocket.

Mojave Sphinx utilizes an aluminum heat-sink engine design, where the nozzle conducts heat away from the hot-gas region during the burn. To protect the most thermally stressed location, the nozzle incorporates a copper throat insert. Copper’s high thermal conductivity spreads and conducts heat away from the local hotspot, and its higher melting temperature (relative to aluminum) improves thermal robustness. The throat experiences high convective heat flux because the gas reaches sonic velocity there, producing strong shear and turbulence at high temperature. This increases the convective heat-transfer coefficient and concentrates thermal loading, making local thermal management essential for structural integrity and reliable operation.

---

### Nozzle Cross Section

![Photo of Cross Section]({{ "/assets/images/Nozzle.png" | relative_url }})

---

## Thermodynamic Model of the Nozzle

Rocket nozzle flow is complex, but several standard assumptions simplify the analysis and allow first-order performance estimates.

### Assumptions

1. **Adiabatic flow**  
   The nozzle is modeled as adiabatic (heat transfer to the surroundings is neglected). In practice, some heat enters the walls, but gas residence time is short and the chamber-to-exit enthalpy drop is typically much larger than wall losses.

2. **Steady-flow control volume**  
   During the main portion of the burn, the nozzle is treated as steady: mass flow in equals mass flow out, and properties at each location do not change with time. This enables steady-flow energy and momentum analysis.

3. **Isentropic flow (ideal nozzle)**  
   Expansion is often assumed isentropic (adiabatic and reversible), representing an upper bound with no losses from friction, shocks, or separation. Because real nozzles experience irreversibilities, we can account for deviations by using an efficiency/correction factor; HalfCat suggests that 95-98% efficiency is a good approximation.

4. **Ideal-gas combustion products**  
   Exhaust gases are modeled as an ideal gas with effective properties (e.g., representative $c_p$, $R$, and $\gamma$). This allows us to use relationships between pressure, temperature, Mach number, and velocity.

5. **Negligible shaft work and potential energy change**  
   No moving components exist in the nozzle (no shaft work), and potential energy changes are negligible compared to kinetic energy changes. The energy equation simplifies to an enthalpy–kinetic energy conversion model.

---

### Energy Balance (Control Volume)


![Energy Balance]({{ "/assets/images/eq2.png" | relative_url }})

![Energy Balance]({{ "/assets/images/eq1.png" | relative_url }})

---

### Isentropic Relations

![Isentropic Relations]({{ "/assets/images/eq.png" | relative_url }})

---

### Control Volume Model

<img src="{{ '/assets/images/model1.png' | relative_url }}" alt="Deflection diagram" style="max-width: 600px; width: 100%; height: auto;">

---
### Example Calculation and Analysis

Because Mojave Sphinx does not publicly provide detailed in-nozzle state data, we estimate nozzle performance using **NASA CEA** equilibrium properties at the nominal operating point ($\mathrm{O/F}=2.1$, $p_c=250\ \mathrm{psi}$) for nitrous oxide + ethanol. CEA returns the nozzle-inlet (stagnation) properties:

- $T_0 = 2331.86\ \mathrm{K}$
- $c_p = 1.9982\ \mathrm{kJ/(kg\cdot K)} = 1998.2\ \mathrm{J/(kg\cdot K)}$
- $k=\gamma=1.2673$

Assumptions: **isentropic nozzle**, **ideally expanded at sea level** ($p_e \approx p_a$), and **nozzle inlet pressure** ($p_0 \approx p_c$).

---

### 1) Exit velocity (isentropic expansion)

Using the constant-$c_p$ isentropic relation:

$$
V_e=\sqrt{2c_pT_0\left[1-\left(\frac{p_e}{p_0}\right)^{\frac{k-1}{k}}\right]}
$$

With $p_0=p_c=250\ \mathrm{psi}$ and $p_e=p_a=14.7\ \mathrm{psi}$:

$$
V_e \approx 2048\ \mathrm{m/s}
$$

---

### 2) Mass flow rate (from target thrust)

For an ideally expanded nozzle at sea level, pressure thrust is negligible, so:

$$
F \approx \dot{m}V_e
$$

Using the target thrust $F = 250\ \mathrm{lbf} = 1112\ \mathrm{N}$:

$$
\dot{m}=\frac{F}{V_e}\approx 0.543\ \mathrm{kg/s}
$$

---

### 3) Specific impulse

Specific impulse is defined as:

$$
I_{sp}=\frac{F}{\dot{m}g_0}
$$

Using $g_0=9.80665\ \mathrm{m/s^2}$:

$$
I_{sp}\approx 209\ \mathrm{s}
$$

---

## Design Consideration: Area Ratio and Expansion

The nozzle **area ratio** ($A_e/A_t$) strongly affects performance because it sets the exit pressure and the direction of the exhaust flow. A nozzle is **ideally expanded** when the exit pressure equals ambient pressure; in that case, the exhaust jet is well-aligned with the nozzle axis and most momentum contributes to axial thrust.

- **Underexpanded nozzle** ($p_e > p_a$): the flow continues expanding outside the nozzle via expansion fans; the jet spreads and some momentum is directed radially, reducing effective axial thrust at that condition. Underexpansion at sea level can become closer to ideal at higher altitude where ambient pressure is lower.

- **Overexpanded nozzle** ($p_e < p_a$): ambient pressure compresses the jet, generating compression waves and potentially shocks. Slight overexpansion mainly reduces efficiency, while severe overexpansion can cause boundary-layer separation and other additional losses.

For practical engines, the expansion ratio is chosen as a compromise across the expected operating altitude range. For Mojave Sphinx, the nozzle is designed to be **ideally expanded near sea-level atmospheric conditions**.

---

## Resources

YouTube (nozzle explanation):
https://www.youtube.com/watch?v=yMrJl-lJrRI&list=TLPQMjMxMTIwMjUaT-Oj5JbkUg&index=1

AST Forge (rocket nozzle overview):
https://astforgetech.com/rocket-nozzles-types-manufacturing-materials/

Half-Cat Rocketry - Mojave Sphinx:
https://www.halfcatrocketry.com/mojave-sphinx

NASA CEA: 
https://cearun.grc.nasa.gov/
