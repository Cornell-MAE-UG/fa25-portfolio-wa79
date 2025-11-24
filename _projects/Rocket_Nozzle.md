---
layout: project
title: Rocket Nozzle Portfolio
description: Rocket Nozzle of Mojave Sphinx
technologies: [Fusion 360]
image: /assets/images/nozzle2.png
---

Mojave Sphinx is a high-power amateur rocket powered by a liquid bipropellant engine using nitrous oxide as the oxidizer and compatible hydrocarbons, such as ethanol, as fuel. It was designed and proposed by Half-Cat Rocketry to provide a relatively simple and economical platform for new teams to gain practical experience in designing, manufacturing, and testing liquid rockets within a realistic student budget and timeline.

A key thermodynamic component of the Mojave Sphinx propulsion system is the converging–diverging nozzle located downstream of the combustion chamber. The primary function of the nozzle is to convert the high-temperature, high-pressure combustion products into directed kinetic energy by accelerating the flow to high velocity. Hot gases leaving the chamber enter the converging section of the nozzle, where under subsonic conditions,a decrease in cross-sectional area causes an increase in velocity and a decrease in static pressure. At the smallest cross-sectional area, known as the throat, the flow becomes choked and reaches Mach 1 when the chamber-to-ambient pressure ratio is sufficiently high.

Beyond the throat, the nozzle diverges. In this supersonic region, the area–velocity relationship reverses: increasing cross-sectional area causes the supersonic flow to accelerate further while its static pressure and temperature decrease. This geometry achieves a thermodynamic energy conversion from internal energy and pressure of the gas into directed kinetic energy at the nozzle exit. The resulting high-velocity exhaust jet generates thrust through momentum exchange with the surroundings, in accordance with Newton’s third law, thereby accelerating the rocket.

Mojave Sphinx utilizes an aluminum heat-sink engine design, in which the nozzle structure conducts heat away from the hot gas region during the burn. To protect the most thermally stressed location, the nozzle incorporates a copper insert at the throat. Copper’s high thermal conductivity helps spread and conduct heat away from the local hot spot, and its higher melting temperature compared to aluminum improves thermal robustness. The throat experiences the highest convective heat flux because the gas reaches sonic velocity there, producing strong shear and turbulence at high gas temperature. This combination leads to a large convective heat-transfer coefficient and concentrated thermal loading, making localized thermal management at the throat essential for maintaining structural integrity and reliable operation over the engine’s firing duration.

![Photo of Cross Section]({{ "/assets/images/Nozzle.png" | relative_url }})

**Thermodynamic Model of Nozzle:**
Rocket systems are extremely complex because of the nature of combustion processes that occur within the combustion chamber. However, there are many assumptions that can be made to simply calculations so that we can analyze a nozzle’s efficiency: 

**Adiabatic flow**
The nozzle is modeled as adiabatic, meaning heat transfer to the surroundings is neglected. In practice, some heat is conducted into the nozzle walls, but the residence time of the gases is very short, and the enthalpy drop between chamber and exit is much larger than the heat losses. This assumption simplifies the energy equation and focuses the analysis on the conversion of thermal energy into kinetic energy.

**Steady-flow control volume**
During the main portion of the burn, the nozzle is treated as a steady-flow control volume: mass flow into the nozzle equals mass flow out, and properties at each location do not change with time. This allows the use of steady-flow energy and momentum equations to relate chamber conditions to exit conditions and thrust.

**Isentropic flow (ideal nozzle)**
For performance calculations, the nozzle expansion is often assumed isentropic (adiabatic and reversible). This represents an ideal upper bound with no losses from friction, shocks, or flow separation. Real nozzles do experience irreversibilities, but well-designed contours can operate reasonably close to isotropic behavior, and deviations are accounted for through an isentropic efficiency or correction factor.

**Ideal-gas combustion products**
The exhaust gases are modeled as an ideal gas with effective specific heat and gas constant. At the high temperatures and moderate pressures typical of small liquid engines, this provides a good approximation and yields simple analytic relationships between pressure, temperature, density, Mach number, and velocity along the nozzle.

**Negligible shaft work and potential energy change**
The nozzle does not contain moving mechanical elements, so there is no shaft work crossing the control-volume boundary. Changes in gravitational potential energy across the nozzle length are also negligible compared to the large change in kinetic energy. As a result, the steady-flow energy equation simplifies to a balance between enthalpy and kinetic energy, highlighting the nozzle’s role in converting thermal energy into directed exhaust velocity.

**Energy Balance**
![Energy Balance]({{ "/assets/images/eq2.png" | relative_url }})

![Energy Balance]({{ "/assets/images/eq1.png" | relative_url }})

**Isentropic Relations**
![Isentropic Relations]({{ "/assets/images/eq.png" | relative_url }})

**Design Consideration:** 
The area ratio of the nozzle (exit area relative to throat area) strongly affects performance because it determines the exit pressure and flow direction of the exhaust gases. A nozzle is considered ideally expanded when the exit pressure of the gases equals the ambient atmospheric pressure. Under this condition, the exhaust jet is aligned with the nozzle axis, and essentially all of the gas momentum contributes to useful thrust in the axial direction.

In an underexpanded nozzle, the exit pressure is higher than the ambient pressure. The flow “wants” to keep expanding after it leaves the nozzle, so expansion fans form outside the nozzle and the jet continues to spread. As a result, part of the exhaust velocity is directed radially outward instead of purely axially, which reduces the effective axial thrust for a given mass flow and chamber pressure. However, a nozzle that is underexpanded at sea level may become closer to ideally expanded at higher altitude, where ambient pressure is lower.

In an overexpanded nozzle, the exit pressure is lower than the ambient pressure. The higher ambient pressure compresses the jet, generating compression waves or even shocks that can turn the flow back inward. At moderate overexpansion this mainly causes a loss in efficiency, since some of the exhaust momentum is redirected and dissipated through shocks. At more severe overexpansion, the flow can separate from the nozzle wall, leading to asymmetric side loads and additional performance penalties. For practical engines, the nozzle expansion ratio is therefore chosen as a compromise so that the nozzle operates near ideally expanded conditions over the most important part of its altitude range. For mojave sphinx, the nozzle is designed such that it is ideally expansive under normal atmospheric conditions. 
