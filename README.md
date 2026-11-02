# Fired Heater Model (480-FA-41-01): Radiant and Convective Sections

Rigorous Python model of the vertical cylindrical hot oil heating fired heater 480-FA-41-01, which supplies the amine regenerator reboilers of the Acid Gas Removal Unit (AGRU) at the Rhourde Nouss Natural Gas Central Processing Facility, southeastern Algeria.

## Overview
The model solves the mass and energy balances of the radiant and convective sections, predicts the key flame and furnace temperatures, and couples them with combustion and NOx kinetics. Predicted oil outlet temperatures were compared with plant (DCS) data, and predicted flue gas composition was compared with portable flue gas analyzer measurements.

## Model Description

### Radiant Section
- Energy and mass balances solved with the **Lobo-Evans method**.
- Predicts the **adiabatic flame temperature** and the **bridge wall temperature** at the radiant section exit.

### Convective Section
- Energy and mass balances solved with the **NTU method**.
- Predicts the oil outlet temperature from the convective section.

### Combustion and Flue Gas Species
- Kinetics ODEs for fuel gas combustion using the **Westbrook-Dryer reduced mechanism** for methane.
- **Yield-based NOx kinetics**, fine-tuned to match flue gas analyzer measurements.
- Predicted flue gas species: **CO₂, H₂O, CO, unburned hydrocarbons (C<sub>x</sub>H<sub>y</sub>), NO, NO₂ and total NOx**.

## Validation

### Temperatures: Model vs. Plant Data (DCS)
| Quantity | Model (°C) | Plant data (°C) | Deviation (%) |
|---|---|---|---|
| Oil outlet temperature, convective section | X | X | X |
| Oil outlet temperature, radiant section | X | X | X |

### Flue Gas Composition: Model vs. AMETEK Land Lancom 4 Portable Flue Gas Analyzer

**Major species and unburned products**
| Species | Model (mol%) | Analyzer (mol%) | Model (mg/Nm³) | Analyzer (mg/Nm³) |
|---|---|---|---|---|
| CO₂ | 12.2617 | 12.4600 | 240759.29 | 244652.87 |
| CO | 0.0021 | 0.0021 | 25.67 | 25.62 |
| C<sub>x</sub>H<sub>y</sub> | 0.0457 | 0.0433 | 326.91 | 309.09 |

**Nitrogen oxides**
| Species | Model (mg/Nm³) | Analyzer (mg/Nm³) | Deviation (%) |
|---|---|---|---|
| NO | X | X | X |
| NO₂ | X | X | X |
| Total NOx | X | X | X |

## Tools
Python

## Notes

Inputs are sanitized or normalized; no confidential plant or vendor data is included.

*This repository is only a preview of some results from the model developed in Python (no code is attached).*
