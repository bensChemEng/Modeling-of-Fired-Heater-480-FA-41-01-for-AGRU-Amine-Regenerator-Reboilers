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
- Predicted flue gas species: **CO₂, H₂O, CO, unburned hydrocarbons (C<sub>x</sub>H<sub>y</sub>), NO and NO₂**.

## Validation

### Temperatures: Model vs. Plant Data (DCS)
| Quantity | Model (°C) | Plant data (°C) | Deviation (%) |
|---|---|---|---|
| Oil outlet temperature, convective section | X | X | X |
| Oil outlet temperature, radiant section | X | X | X |

### Flue Gas Composition: Model vs. AMETEK Land Lancom 4 Portable Flue Gas Analyzer
| Species | Unit | Model | Analyzer | Deviation (%) |
|---|---|---|---|---|
| CO₂ | vol% | X | X | X |
| H₂O | vol% | X | X | X |
| CO | ppm | X | X | X |
| C<sub>x</sub>H<sub>y</sub> | ppm | X | X | X |
| NO | ppm | X | X | X |
| NO₂ | ppm | X | X | X |

## Tools
Python

## Notes

Inputs are sanitized or normalized; no confidential plant or vendor data is included.

*This repository is only a preview of some results from the model developed in Python (no code is attached).*
