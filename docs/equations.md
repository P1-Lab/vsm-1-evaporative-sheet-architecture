# Governing Equations

These equations provide first-order approximations used to explore the VSM-1 architecture.

Real-world performance is expected to deviate due to:

* air shear
* corrugations
* fouling
* biological growth
* nonuniform wetting
* drift

---

# Falling Film Reynolds Number

Film Reynolds number is defined using liquid mass flow rate per unit width.

[
Re_{film}=\frac{4\Gamma}{\mu}
]

Where:

* Γ = liquid mass flow per unit width
* μ = dynamic viscosity

---

# Nusselt Falling Film Approximation

Clean-state approximation:

[
\delta=
\left(
\frac{3\mu\Gamma}
{\rho^2 g \sin\theta}
\right)^{1/3}
]

Where:

* δ = film thickness
* ρ = density
* g = gravity
* θ = inclination angle

---

# Average Film Velocity

[
u_{avg}=
\frac{\Gamma}
{\rho\delta}
]

---

# Residence Time

[
\tau=
\frac{H}
{u_{avg}}
]

---

# Total Heat Rejection

[
Q_{total}
=========

\dot m_a
(h_{out}-h_{in})
]

Where:

* dry air mass flow drives enthalpy change

---

# Evaporation Rate

[
\dot m_e
========

K A (Y_w-Y_a)
]

Where:

* K = mass transfer coefficient
* A = wetted surface area
* Y = humidity ratio

---

# Surface Tension Gradients

Marangoni-driven surface tension gradients:

[
\nabla_s \sigma
===============

\frac{\partial\sigma}{\partial T}\nabla_sT
+
\frac{\partial\sigma}{\partial c}\nabla_sc
]

These gradients may destabilize thin films and create rivulet formation.

---

# Important Warning

These equations are intended for:

* exploratory modeling
* first-order sizing
* sensitivity analysis

They are not validated design equations.
