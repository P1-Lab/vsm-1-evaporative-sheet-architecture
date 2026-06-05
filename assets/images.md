# Project VSM-1: Community Graphics & Visualization Contribution Roadmap

This document serves as an open framework and call for contributions for the visual assets required by the VSM-1 repository. Because this is an open-source research architecture, we rely on community-driven technical illustrations, CFD rendering exports, and vector schematics to ground our math and text.

---

## I. Contribution Guidelines & Asset Pipeline

To ensure all contributed graphics maintain absolute professional and mathematical integrity, submissions must adhere to the following baseline constraints:

* **Format:** Vector graphics (`.svg`) are mandatory for schematics, PFDs, and block diagrams to allow for scaling and modification. Lossless `.png` formats are acceptable only for high-density CFD post-processing renders.
* **Color Palette:** High-contrast, minimalist technical styling. Avoid dark-theme forced backgrounds. Use solid gray/slate for mechanical structures, clean blue for liquid/cold vectors, and amber/red for thermal energy zones.
* **Typography:** All labels and dimension text must use clean sans-serif system fonts (e.g., Arial, Helvetica).
* **Mathematical Notation:** Any variables or parameters embedded directly within the graphics must precisely match the LaTeX formatting utilized in the core repository documentation (e.g., $Re_{\text{film}}$, $\delta$, $\Gamma$, $\nabla_s \sigma$).

---

## II. Asset Status Matrix & Open Call

| Asset ID | Target Filename | Desired Format | Documentation Target | Status |
| --- | --- | --- | --- | --- |
| **Fig-1** | `vault_macro_geometry.svg` | SVG | `README.md` (Section II.2) | 📢 **OPEN FOR CONTRIBUTION** |
| **Fig-2** | `falling_film_hydrodynamics.svg` | SVG | `README.md` (Section III.1) | 📢 **OPEN FOR CONTRIBUTION** |
| **Fig-3** | `marangoni_regime_map.png` | SVG/PNG | `experiments.md` (Exp 1.1) | 📢 **OPEN FOR CONTRIBUTION** |
| **Fig-4** | `rectification_pfd.svg` | SVG | `README.md` (Section II.1) | 📢 **OPEN FOR CONTRIBUTION** |
| **Fig-5** | `drift_weber_analysis.png` | PNG | `experiments.md` (Exp 2.2) | 📢 **OPEN FOR CONTRIBUTION** |

---

## III. Detailed Target Specifications for Contributors

### Fig-1: Sparse Sheet Vault Macro-Geometry

* **Concept:** A 3D isometric cutaway illustrating the physical scaling of parallel vertical substrates relative to horizontal compute-driven airflow.
* **Required Callouts:** Adjustable exploratory pitch track ($25\text{ mm}$ to $40\text{ mm}$), uniform overhead precision gravity weir headers, and horizontal airflow velocity vectors ($2.0\text{ to }2.5\text{ m/s}$).
* **Thermal Representation:** A clear gradient showing cool/dry entering air shifting to hot/saturated exhaust air across the media section.

### Fig-2: Falling-Film Hydrodynamics & Interface Physics

* **Concept:** A detailed 2D micro-scale cross-section orthogonal to the vertical sheet wall mapping fluid-air boundary layer interactions.
* **Required Callouts:** Liquid phase thickness boundary ($\delta$) mapping the Nusselt approximation, downward velocity profile vectors ($u(y)$) within the film, and the gas-liquid interface convective mass transfer zone ($K$) driven by local humidity ratios ($Y_w - Y_a$).

### Fig-3: Marangoni Instability & Localized Dryout Regime Map

* **Concept:** A 2D Cartesian coordinate chart defining the operational boundaries where surface tension gradients destroy film continuity.
* **Required Callouts:** Y-axis showing liquid mass flow rate per unit width ($\Gamma$, scale: $0.0\text{ to }3.5\text{ kg/m}\cdot\text{s}$), X-axis showing localized thermal gradient ($\nabla_s T$, scale: $0.0\text{ to }10.0^{\circ}\text{C/m}$), and a non-linear critical wetting rate line ($\Gamma_{\text{min}}$) splitting the graph into a green stable zone and a red-hatched rivulet collapse zone.

### Fig-4: Comprehensive Process Flow Diagram (PFD)

* **Concept:** A complete industrial mechanical and chemical sequence layout mapping the filtration and heat loop stages using ISA-standard instrumentation block symbology.
* **Required Flow-lines:** Main purification train (Multi-media $\rightarrow$ Ultrafiltration $\rightarrow$ Softening $\rightarrow$ TFC RO $\rightarrow$ EDI Core), primary open loop (Sump $\rightarrow$ Pumps $\rightarrow$ Weirs $\rightarrow$ Vault Basin $\rightarrow$ Primary HX), and the secondary zero-liquid-discharge (ZLD) reclamation concentrator loop.

### Fig-5: Multi-Phase Droplet Stripping Mechanics

* **Concept:** A post-processed CFD particle-tracking render or detailed vector illustration detailing the trailing air-exit boundaries of the sheet cassettes.
* **Required Callouts:** Droplet shear thresholds at the sheet edge, liquid Weber number ($We$) vectors acting at the interface, and droplet tracking profiles showing lines that violate the target drift mass fraction ceiling ($<0.001\%$).

---

## IV. Submission Process

1. Select an open asset from the **Asset Status Matrix**.
2. Open a repository Issue titled `[Asset Contribution] Fig-X: [Asset Title]` to signal your intent and avoid duplicated effort.
3. Submit your vector or lossless file via a Pull Request (PR) targeted to the `/assets/images/` directory. Ensure your PR description includes a render preview and references the tracking issue.
