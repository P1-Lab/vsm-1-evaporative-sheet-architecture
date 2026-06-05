# Architecture Overview

## Purpose

The VSM-1 architecture explores whether sparse falling-film evaporative geometries can reduce aerodynamic resistance sufficiently to justify increased water treatment complexity.

The architecture intentionally prioritizes:

* Low air-side pressure drop
* Large wetted surface area
* Falling-film stability
* High operational observability
* Explicit identification of failure modes

---

# System Overview

```text
Water Rectification
        ↓

Distribution Headers
        ↓

Vertical Sheet Vault
        ↓

Catchment Basin
        ↓

Low Head Pumps
        ↓

Plate Heat Exchanger
        ↓

Facility Thermal Loop
```

---

# Subsystem 1: Water Rectification

Purpose:

Reduce mineral-driven failure modes sufficiently to permit elevated operating envelopes.

Treatment train:

```text
Multi Media Filtration
        ↓

Ultrafiltration
        ↓

Softening
        ↓

Reverse Osmosis
        ↓

EDI Polishing
```

Target baseline:

* Conductivity: <10–15 μS/cm
* Elevated operating envelope
* Reduced mineral deposition risk

Primary limitation:

* Atmospheric contamination
* Material leaching
* Biological loading

---

# Subsystem 2: Falling-Film Sheet Vault

Purpose:

Decouple surface area from aerodynamic resistance.

Characteristics:

* Parallel sheet arrays
* Exploratory pitch range: 25–40 mm
* Horizontal crossflow
* Low pressure-drop geometry
* Engineered wetting surfaces

Target operating philosophy:

```text
Low Drag

+

High Surface Area

+

Stable Thin Films
```

---

# Subsystem 3: Thermal Isolation Loop

Purpose:

Prevent contamination transfer between atmospheric evaporative systems and compute infrastructure.

Components:

* Catchment basin
* Low-head pumps
* Plate heat exchanger
* Closed facility loop

Supported downstream systems:

* Direct-to-chip cooling
* Immersion cooling
* Conventional liquid cooling loops

---

# Design Philosophy

VSM-1 intentionally treats:

* chemistry
* geometry
* airflow
* economics

as a single coupled optimization problem.

The architecture should be viewed as a falsifiable research layout rather than a production design.
