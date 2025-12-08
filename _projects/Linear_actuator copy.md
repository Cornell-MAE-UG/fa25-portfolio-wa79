---
layout: project
title: Linear Actuator Design
description: Linear Actuator Assignment
technologies: [Draw.io]
image: /assets/images/linear.png
---
For this statics design, I created a linear-actuator lifting mechanism inside a **150 cm × 50 cm** 2D workspace using **three pin joints** (two grounded). From the provided catalog, I selected the **IMA55 actuator**, rated for a maximum thrust of **8050 lbf** with a **45.7 cm stroke**. The linkage geometry was chosen to achieve a **50 cm lift** while allowing rotation through ideal pin joints.

### Assumptions
- The bar is rigid (no bending).
- Pin joints are frictionless.
- The actuator and supports are rigid (no compliance).
- Static equilibrium (no acceleration).
- The payload load is modeled as a point load applied at the payload pin.

### Geometry / Design Choice
The bar length is **L = 150 cm**, oriented at approximately **θ ≈ 19.6°** from the ground to reach the 50 cm lift height.

Using a moment balance about the ground pin at **A**, I determined the maximum payload that can be lifted to 50 cm is:

- **Maximum lifted weight:** **W = 7357.82 lbf**

**(Insert image of rigid-bar FBD + moment calculation here)**  

![Rigid-bar FBD](images/fbd_rigid.png)  
![Moment balance](images/moment_calc.png)

---

## Beam Bending / Deflection Analysis (Non-Rigid Bar)

In reality, the bar is not rigid and will deflect under the combined action of the payload and actuator. To estimate the maximum deflection, I model the bar as an Euler–Bernoulli beam and define the beam axis as the $x$-axis along its length.

Per the assignment instructions, I consider only the **force components transverse to the beam** when constructing the bending moment function.

### Assumptions
- Euler–Bernoulli beam theory (small deflection; linear elastic; plane sections remain plane).
- Beam is prismatic (constant cross-section; constant $E$ and $I$).
- Pins do not resist moment (ideal pin supports).
- Beam self-weight is neglected.
- Payload is modeled as a point load near the end of the beam (approximately at $x=L=150\ \text{cm}$).
- Only transverse components of the payload/actuator forces contribute to bending (computed via the mechanism geometry).

### Boundary Conditions and Continuity
In this configuration, the beam is vertically constrained at:
- the ground pin at $x=0$ (point A),
- the actuator attachment point at $x=a$.

Therefore, the deflection boundary conditions are:
- $y_1(0)=0$
- $y_1(a)=0$

Because the beam remains continuous at $x=a$ (not a hinge), the slope must be continuous across the two regions:
- $y_1'(a)=y_2'(a)$

*(Slope continuity does **not** require the slope to be zero; it only requires the left and right slopes to match.)*

### Piecewise Bending Moment and Integration
The bending moment is defined piecewise:
- Region 1: $0 < x < a$
- Region 2: $a < x < L$

Using Euler–Bernoulli:
$$
EI\,y''(x) = M(x)
$$

I integrate $M(x)$ twice in each region to obtain $y_1(x)$ and $y_2(x)$, then apply the boundary conditions and continuity condition to solve for integration constants.

### Maximum Deflection
Maximum deflection occurs where the slope is zero:
$$
y'(x)=0
$$

For this geometry, the maximum occurs at:
- **$x^* = 79.15\ \text{cm}$**

Evaluating the deflection at this point gives:
$$
y_{\max} = \frac{1.08 \times 10^8}{E I}\ \text{cm}
$$

**(Insert image of moment diagram / deflection sketch here)**  

![Moment diagram](images/moment_diagram.png)  
![Deflection curve](images/deflection_curve.png)

---

## Beam Design Selection (Mass-Efficient)

The deflection requirement is:
$$
y_{\max} < 0.02L = 3\ \text{cm}
$$

To satisfy this while minimizing mass, I chose **6061 Aluminum** due to its favorable strength-to-density characteristics.

### Selected Beam
I selected a **6061 aluminum round tube** with:
- Outer diameter: **73 mm**
- Wall thickness: **2 mm**

Material and section properties:
- $E = 69\ \text{GPa}$
- $I \approx 2.81 \times 10^{-7}\ \text{m}^4$

Predicted performance:
- **Maximum deflection ≈ 2.9 cm** (meets the 3 cm limit)

Mass estimate (using $\rho = 2700\ \text{kg/m}^3$):
- Cross-sectional area: $A \approx 4.46 \times 10^{-4}\ \text{m}^2$
- Beam length: $L = 1.5\ \text{m}$
- Mass: 
$$
m = \rho A L \approx (2700)(4.46\times 10^{-4})(1.5) \approx 1.81\ \text{kg}
$$