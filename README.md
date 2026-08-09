#  4×4 Approximate Wallace Tree Multiplier
 4×4 Approximate Wallace Tree Multiplier implemented in Cadence Virtuoso 90mm CMOS using pareto optimal adders
# Area and Power Efficient 4×4 Approximate Wallace Tree Multiplier Using Pareto-Optimal Adders

## Overview
This repository contains the design, layout, and post-layout characterization of 4×4 Wallace Tree Multipliers (WTMs) implemented in a 90 nm CMOS process using Cadence Virtuoso.

To address the growing demand for low-power and high-speed digital signal processing units, this project explores **Approximate Computing** by replacing traditional full adders with Pareto-optimal approximate full adders (AFAs). The chosen AFAs feature the **0-in/0-out property** to prevent error propagation during trivial zero-operand computations.

## Key Architectures
1. **Exact Wallace Tree Multiplier (E-WTM):** Baseline design utilizing standard 28-transistor exact full adders.
2. **Approximate WTM 1 (AWTM-1):** Incorporates **A856** approximate full adders (MRED = 0.119%) for high accuracy with moderate power/area savings.
3. **Approximate WTM 2 (AWTM-2):** Incorporates **88F6** approximate full adders (MRED = 0.143%) optimized for maximum speed and power efficiency.

---

## Hardware Performance & Results

### Post-Layout Performance Comparison (90 nm CMOS @ 1.2 V, 25 °C)

| Metric | E-WTM (Exact) | AWTM-1 (A856) | AWTM-2 (88F6) | AWTM-2 Gain vs. E-WTM |
| :--- | :--- | :--- | :--- | :--- |
| **Area ($\mu\text{m}^2$)** | 3470.3 | 2171.29 | 2175.53 | **37.3% Reduction** |
| **Power ($\mu\text{W}$)** | 19.33 | 12.52 | 9.82 | **49.2% Reduction** |
| **Delay ($\text{ps}$)** | 298.66 | 271.48 | 170.58 | **42.9% Reduction** |
| **PDP ($\text{aJ}$)** | 5773.09 | 3398.93 | 1675.09 | **71.0% Improvement** |

---

## Project Structure
```text
├── docs/                # Internship report and documentation
├── schematics/          # Schematic views for FA, AFAs, and Multipliers
├── layouts/             # Physical layouts and DRC/LVS reports
├── extracted/           # Spectre post-layout parasitic extraction views
└── README.md            # Project description
