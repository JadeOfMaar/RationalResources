# Rational Resources Nuclear Family
This modlet enables all supported atomic rockets to have fuel switching and accept resources other than LiquidFuel or Hydrogen. Support-able atomic rockets must have their primary mode only accept one propellant (please do not tag something that already consumes Hydrogen + EnrichedUranium, like Kerbal Atomics' gas cores). This mod also supports atomic rockets that have LOX-augmented second mode.

![screenshot](https://i.imgur.com/8gNXvRi.png)

> :bulb: This mod involves an opt-in system. Parts must be tagged and correctly in order to be handled.

> :bulb: WBI Classic Stock is supported. CRP resources are replaced where necessary.

> All affected engines, in addtion to the details below, also receive Kerbalism radioactivity. This rating scales with the part's dry mass.

> :warning: This mod may conflict with Kerbal Atomics' optional extra: KerbalAtomicsLH2NTRModSupport

> :small_orange_diamond: = Given values are for reference and will scale with the original thrust and Isp of the affected engine.

## NTR Primary/Single Mode
Rational Resources Nuclear Family operates on any atomic rocket part that is given the tag `RRNF = Yes`. The affected engine gets its title appended and gets cloned: one instance for oxidating agents (propellants that contain Oxygen) and one for reducing agents (propellants that don't contain Oxygen).


The Oxidating Agent engine receives the following options for its primary mode: 

CRP:

| Propellant | Vac Isp :small_orange_diamond: | Thrust :small_orange_diamond: | Detail |
| -- | -- | -- | -- |
| Hydrogen | 800 s | 60 kN | This is the highest efficiency, baseline option for NTRs. |
| Ammonia | 400 s | 100.9 kN | This may be very niche but is made very available, the Ammonia option trades exactly half the baseline efficiency for double the thrust. |
| Carbon Dioxide | 283 s | 130.8 kN | Impulse is as good as the average LiquidFuel rocket, and this is the most convenient option due to the great abundance of Carbon Dioxide in some planets' atmospheres. |
| Carbon Monoxide | 253 s | 142.3 kN | This is the highest thrust option among all RR NTR options and is fitting for use at inner rocky worlds with atmospheres. |
| Methane | 606 s | 73.9 kN | This option trades a very modest portion of efficiency for thrust but makes use of the highly demanded alternative propellant for launchers and boosters. |
| Nitrogen | 253 s | 142.3 kN | Nitrogen as a propellant may be very niche and is poor in terms of Isp, but it is common in planetary crusts, atmospheres, oceans, and exospheres. |
| Water | 370 s | 107 kN | This is the more economical high thrust option, immediately superior in performance to the likes of the LV-303 and LV-909 LFO engines. |

Classic Stock:

| Propellant | Vac Isp :small_orange_diamond: | Thrust :small_orange_diamond: | Detail |
| -- | -- | -- | -- |
| Propellium | 800 s | 60 kN | This is the highest efficiency, baseline option for NTRs. |
| Raptium | 606 s | 73.9 kN | This option trades a very modest portion of efficiency for thrust but makes use of the highly demanded alternative propellant for launchers and boosters. |
| Water | 370 s | 107 kN | This is the more economical high thrust option, immediately superior in performance to the likes of the LV-303 and LV-909 LFO engines. |
| Fresh Air | 253 s | 142.3 kN | This option is on the weirder and desperate side but whatever works... Pray that it's never needed. |
| Compressed Atmosphere | 283 s | 60 kN | CompressedAtmosphere as a propellant may be very poor in terms of Isp, but any atmosphere is fuel, and that's always good. |
| Stale Air | 283 s | 130.8 kN | Stale Air, right? |




## LANTR Mode
All affected engines which have a second engine mode are ensured to have Hydrogen *(or Propellium)* + Oxidizer as the propellants, with a fixed ratio and 20% Isp buff.


## NTJ
Rational Resources Nuclear Family operates on any atomic jet part that is given the tag `RRNTJ = Yes`. The part is changed to require IntakeAtm + ThermalPower *(or Atmosphere + CoreHeat)* as its propellants. It is also given a stock converter module (the nuclear reactor) and capacity for EnrichedUranium + DepletedFuel *(or NuclearFuel + NuclearWaste)*.

This reactor is required for the production of the added propellant ThermalPower *(or CoreHeat)* but will also produce ElectricCharge and serve as a useful secondary or tertiary power source.



## Nerd Stuff

The reactor configs added to parts in this mod are balanced as follows:
- Reactor and generator capacities are scaled by [this engine's] thrust divided by 130 kN, the value given to the RR Main Coon demo nuclear turbojet.
- Nuclear fuel capacity is scaled by [this engine's] mass divided by 1.8 tons, the value given to the RR Main Coon demo nuclear turbojet.
- The difference (as a multplie) of [this engine's] Isp vs the baseline of 800 seconds is taken and applied to the ThermalPower ratios of the propellant options so that an engine with higher Isp asks for more ThermalPower, not less.
- [This engine] is a gigawatt nuclear reactor so it must produce some thousands of ThermalPower per second but its own generator is very weak and will typically produce a few hundred ElectricCharge per second.
- Every propellant option must require roughly 1/3 of the ThermalPower produced.


The tables assume an RR Fission Reactor (standard resource converter) produces 600 ThP/sec and each propellant asks for 200 ThP/sec:

CRP:

| Propellant | ThP ratio | Thrust multiplier | Isp |
| -- | -- | -- | -- |
| IntakeAtm | 113.153 | 1 | 1500 |
| Hydrogen | 1.8527 | 1 | 800 |
| Ammonia | 5.4644 | 1.68 | 400 |
| Carbon Dioxide | 4.9787 | 2.18 | 283 |
| Carbon Monoxide | 2.7567 | 2.37 | 253 |
| Methane | 6.8545 | 1.23 | 606 |
| Nitrogen | 2.8785 | 2.37 | 253 |
| Water | 6.7948 | 1.78 | 370 |

Classic Stock:

| Propellant | ThP ratio | Thrust multiplier | Isp |
| -- | -- | -- | -- |
| Atmosphere | 113.153 | 1 | 1500 |
| Propellium | 9.2574 | 1 | 800 |
| Raptium | 34.2727 | 1.23 | 606 |
| Water | 14.4598 | 1.78 | 370 |
| Fresh Air | n/a | 2.37 | 253 |
| CompressedAtmosphere | 21.2177 | 2.18 | 283 |
| Stale Air | n/a | 2.18 | 283 |
