Below, are three essential technical architectural diagrams structured directly in scannable text and layout format for seamless integration into the repository documentation. They avoid programmatic code wrappers to maintain formatting integrity while providing clean, spatial representations of the core physics and process flows.

---

## Diagram 1: Fluid-Air Crossflow Interface Topology

This schematic maps the spatial relationship between the vertical falling-film vector and the horizontal aerodynamic vector within the sheet vault, highlighting the low-impedance geometry.

Liquid Input Vector (Gravity Weir Header)
│
▼
┌────────────────────────────────────────────────────────┐
│  Sheet Substrate No. 1                                 │
│  ├── Sub-millimeter Laminar Fluid Film ($\delta$)        │
│  └── Engineered Wetting Treatment Layer                 │
└────────────────────────────────────────────────────────┘
│
│   ➔  Horizontal Air Crossflow Vector ($2.0$ to $2.5\text{ m/s}$)
│   ➔  Projected Media Static Resistance: $\le 0.12\text{ in. w.g.}$
│
┌────────────────────────────────────────────────────────┐
│  Sheet Substrate No. 2                                 │
│  [Exploratory Pitch Track: $25\text{ mm}$ to $40\text{ mm}$]  │
└────────────────────────────────────────────────────────┘
│
▼
Hydrostatic Catchment Sump Basin ($\ge 2\%$ Drainage Grade) ➔ Central Vortex Drain

---

## Diagram 2: Water Rectification Train & Low-Mass Closed Loop

This block topology maps the continuous purification process from raw utility intake down to the ultra-pure baseline, terminating in the secondary Zero-Liquid-Discharge (ZLD) isolation loop.

### Phase A: Upstream Rectification Train

Raw Water Input ➔ Multi-Media Filtration ($10\,\mu\text{m}$) ➔ Hollow-Fiber Ultrafiltration ($0.02\,\mu\text{m}$) ➔ Duplex Alternating Softener Bed (Divalent Hardness Extraction) ➔ High-Recovery Reverse Osmosis Membrane ➔ Electrodeionization (EDI) Polishing Core ➔ Pure Sump Target ($<10\text{ to }15\,\mu\text{S/cm}$).

### Phase B: Main Heat Rejection Loop

Pure Sump Storage ➔ Variable-Speed Low-Head Pump ➔ Overhead Distribution Weirs ➔ Vaporization Vault (Latent Heat Transfer) ➔ Sloped Vortex Catchment ➔ Primary Plate-and-Frame Heat Exchanger ➔ Return to Sump.

### Phase C: Contaminant Concentration Failover

Vault Basin Blowdown (Ingested Air Pollutants) ➔ Secondary Concentrator RO Core ➔ Forward Osmosis Draw Cell / Mechanical Crystallizer ➔ Isolated Mineral Solids (Dry Cake Discharge) / Permeate Recycled to Phase A.

---

## Diagram 3: Micro-Scale Interfacial Physics (The Boundary Layer Frontier)

This comparative micro-profile visualizes the physical state of the falling film, contrasting the theoretical design goal with the central existential failure mode of the architecture.

### State A: Ideal Continuous Laminar Falling Film

```
[Solid Substrate Wall]
│█│ 💧 Fluid Film Layer (Uniform thickness $\delta$)
│█│ 💧 Flow Direction: Downward Vector ($\Gamma$)
│█│ 💧 Boundary Condition: Unbroken Interfacial Surface
│█│ 
└─── Air Boundary Layer (Micro-turbulence induced by $35^{\circ}\text{–}45^{\circ}$ corrugations)

```

* **Result:** Maximum active mass-transfer area ($A$), stable wet-bulb approach performance, minimal deposition risk.

### State B: Marangoni Film Collapse & Rivulet Formation

```
[Solid Substrate Wall]
│█│ 💧 High Surface Tension Zone (Cooler Fluid) ──🡰 Pulls Fluid Inward
│█│ ❌ DRY PATCH (Thermal spike, localized scaling core)
│█│ 💧 Low Surface Tension Zone (Warmer Fluid)  ──🡮 Pushes Fluid Away
│█│ 💧 
└─── Air Boundary Layer Choking (Altered local velocity due to thick fluid rivulets)

```

* **Result:** Catastrophic loss of operational surface area, local heat-flux spikes, localized mineral precipitation at dry-wet boundaries.
