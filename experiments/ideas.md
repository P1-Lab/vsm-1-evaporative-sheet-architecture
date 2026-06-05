# Experimental Campaign & Sandbox Validation Protocols

This document outlines the concrete experimental procedures and computational fluid dynamics (CFD) simulation configurations designed to test, validate, or falsify the core thermodynamic and hydrodynamic hypotheses of the VSM-1 architecture. 

The primary objective of this repository is not to prove a commercial concept, but to systematically map out where the physics of thin-film evaporative heat rejection breakdown.

---

## Stage 1: Single-Sheet Hydrodynamics & Interfacial Stability

### Experiment 1.1: Marangoni Rivulet Mapping and Critical Wetting Rate ($\Gamma_{\text{min}}$)
* **Target Boundary:** The Surface Tension Frontier (Section IV.1)
* **Objective:** Identify the exact boundary point where non-isothermal conditions cause a sub-millimeter falling film to collapse into rivulets, exposing dry patches.

#### Apparatus & Simulation Configuration
* **Physical Rig:** A single vertical substrate ($2\text{ m}$ height $\times$ $0.5\text{ m}$ width) mounted on an adjustable inclination frame ($35^{\circ}$ to $90^{\circ}$).
* **Instrumentation:** Non-contact ultrasonic or optical displacement sensors mounted on an automated X-Y gantry to profile film thickness ($\delta$) at $100\text{ mm}$ vertical increments. Thermal imaging camera tracking surface temperature gradients ($\nabla_s T$).
* **Fluid Delivery:** Gravity-fed overfall weir with a micro-metering pump supplying ultra-pure water ($<15\,\mu\text{S/cm}$).

#### Execution & Parameters to Track
1.  Establish a baseline isothermal falling film using the first-order Nusselt approximation:
    $$\delta = \left( \frac{3\mu\Gamma}{\rho^2 g \sin\theta} \right)^{1/3}$$
2.  Introduce a localized heat source to the back of the substrate to establish a controlled surface temperature gradient ($\nabla_s T \ge 5^{\circ}\text{C/m}$).
3.  Stepwise reduce the liquid mass flow rate per unit width ($\Gamma$) in increments of $0.1\text{ kg/m}\cdot\text{s}$.
4.  **Log metrics:** Film thickness profile ($\delta$), onset velocity of film retraction, surface tension gradient stress ($\nabla_s \sigma$), and coordinate map of dry-out patches.

#### Falsification Boundary
The hypothesis that *Nano-structured surface treatments can maintain an unbroken film under high thermal flux* is **falsified** if dry patches form at a fluid flux higher than $\Gamma = 1.2\text{ GPM per linear foot}$ under a temperature gradient of $\nabla_s T = 3^{\circ}\text{C/m}$.

---

## Stage 2: Multi-Sheet Cassette Dynamics & Aerodynamic Taxes

### Experiment 2.1: Clean-State Drag Coefficient & Pitch Optimization
* **Target Boundary:** Hydrophilic Thin-Film Sheet Vault Aerodynamic Baseline (Section II.2)
* **Objective:** Quantify the true static pressure drop ($\Delta P$) across varied sheet pitches to map the absolute limits of the low-pressure claim.

#### Apparatus & Simulation Configuration
* **CFD Mesh:** 3D structured mesh of parallel sinusoidal sheets ($35^{\circ}$ corrugation angle) inside a virtual wind tunnel. Boundary layers must resolve down to $y^+ \le 1$.
* **Physical Validation:** A $1\text{ m}^3$ modular cassette housing sheets on a variable pitch track ($15\text{ mm}$ to $50\text{ mm}$).
* **Airflow Induction:** Variable-speed draw-through fan capable of maintaining face velocities between $1.5\text{ m/s}$ and $4.0\text{ m/s}$.

#### Execution & Parameters to Track
1.  Run airflow through dry sheets to establish geometric baseline pressure drop.
2.  Introduce fluid flux $\Gamma = 1.5\text{ GPM/ft}$ to establish wetted-film baseline drop.
3.  Vary sheet pitch through $20\text{ mm}$, $25\text{ mm}$, $30\text{ mm}$, $35\text{ mm}$, and $40\text{ mm}$.
4.  **Log metrics:** Media-section static pressure drop ($\Delta P$), boundary layer velocity profiles via Pitot tube array, and fan power requirements.

#### Falsification Boundary
The core claim that *VSM-1 can maintain an aerodynamic baseline of $\Delta P \le 0.12\text{ inches w.g.}$ at a $2.5\text{ m/s}$ face velocity* is **falsified** if the clean-state wetted pressure drop exceeds $0.15\text{ inches w.g.}$ at any pitch setting $\ge 25\text{ mm}$.

### Experiment 2.2: Multi-Phase Droplet Stripping & Weber Bounding
* **Target Boundary:** Multi-Phase Fluid Dynamics Drift Model (Section IV.4)
* **Objective:** Map the threshold where crossflow air shear shears fluid droplets off the sheet faces.

#### Apparatus & Simulation Configuration
* High-speed shadowgraphy camera focused on the trailing edges of the multi-sheet cassette. Laser sheet illumination positioned perpendicular to airflow.

#### Execution & Parameters to Track
1.  Fix fluid flux at a steady $\Gamma = 1.8\text{ GPM/ft}$.
2.  Ramp crossflow air velocity from $1.5\text{ m/s}$ to $4.5\text{ m/s}$ in steps of $0.25\text{ m/s}$.
3.  Monitor the film Reynolds number ($Re_{\text{film}} = 4\Gamma / \mu$) and determine the exact air velocity where droplet detachment initiates.
4.  **Log metrics:** Liquid Weber number ($We$), droplet size distribution ($\mu\text{m}$ scale), and total drift mass fraction.

#### Falsification Boundary
The architecture’s claim of *eliminating droplet carryover without heavy drift eliminators* is **falsified** if the measured drift fraction exceeds $0.001\%$ of total circulating volume at an air velocity $\le 2.5\text{ m/s}$.

---

## Stage 3: Small-Scale Pilot Vault ($50\text{ kW}$–$100\text{ kW}$)

### Experiment 3.1: Biological Colonization and Interface Physics Shifts
* **Target Boundary:** The Biological Surface Colonization Problem (Section IV.2)
* **Objective:** Measure how long-term exposure to ambient atmospheric impurities impacts wetting angles and pressure drops.

#### Configuration & Environmental Conditions
* Deploy a $50\text{ kW}$ open-loop testing enclosure located outdoors to maximize natural atmospheric ingestion. Run continuously for $720\text{ hours}$.
* Upstream UV/Ozone loop configured to minimum baseline dosage ($0.1\text{ mg/L}$ continuous ozone equivalent).

#### Execution & Parameters to Track
1.  Measure baseline un-fouled wetted surface area ($A$), mass transfer coefficient ($K$), and media pressure drop ($\Delta P$) on Day 1.
2.  Do not manually clean sheets; allow ambient seeding from environmental airflow.
3.  Every $48\text{ hours}$, perform a psychrometric drawdown test to compute changes in heat rejection efficiency.
4.  Extract sheet coupons weekly to check contact angles via goniometer and audit biofilm density ($\text{mg/cm}^2$).

#### Falsification Boundary
The assumption that *upstream non-chemical disinfection is sufficient to maintain thin-film performance* is **falsified** if biological fouling causes a $\ge 20\%$ decrease in the mass transfer coefficient ($K$) or a $\ge 30\%$ spike in static pressure drop within $30\text{ days}$ of continuous un-cleaned operation.

---

## Stage 4: Techno-Economic & Environmental Stress Block

### Experiment 4.1: The Net-Parasitic Breakeven Boundary
* **Target Boundary:** The Economic Parasitic Breakeven Problem (Section IV.3)
* **Objective:** Define the boundary where the energy cost of running the ultra-purification train cancels out the energy savings from the low-pressure fans.

#### Evaluation Framework
Execute a complete mass-and-energy balance simulation using the repository’s sizing scripts. Run the logic across environmental Stress Profiles A, B, and C.
