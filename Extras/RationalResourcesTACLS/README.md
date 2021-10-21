# Rational Resources TAC 
## TAC LS Reconfig
The core of this mod lies in `RR_TACLS.cfg`. What it does is to replace the abstract Waste resource with the resources that were handwaved (due to not being immediately relevant to TAC LS) within the converter parts shipped in TAC Life Support.

Sabatier Reactors

| State | Inputs | Outputs |
| -- | -- | -- |
| Original | Water + CarbonDioxide + ElectricCharge | Oxygen + Waste |
| RR | Hydrogen + CarbonDioxide + ElectricCharge | Water + Methane |


Water Splitter

| State | Inputs | Outputs |
| -- | -- | -- |
| Original | Water + ElectricCharge | Oxygen + Waste |
| RR | Water + ElectricCharge | Oxygen + Hydrogen |


Carbon Extractor

| State | Inputs | Outputs |
| -- | -- | -- |
| Original | CarbonDioxide + ElectricCharge | Oxygen + Waste |
| RR | CarbonDioxide + ElectricCharge | Oxygen + Carbon |


Air Filter

| State | Inputs | Outputs |
| -- | -- | -- |
| Original | IntakeAir + ElectricCharge | Oxygen |

This module is removed and the part is treated as an atmospheric harvester capable of extracting ambient Oxygen (and Nitrogen, Water) directly at supported planets.

This mod affects TAC converters in the following parts mods:
* Airline Kuisine
* SSPXR