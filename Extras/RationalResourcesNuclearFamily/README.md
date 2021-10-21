# Rational Resources Nuclear Family
This modlet enables all supported atomic rockets to have fuel switching and accept resources other than LiquidFuel or Hydrogen. Support-able atomic rockets must have their primary mode only accept one propellant (please do not tag something that already consumes Hydrogen + EnrichedUranium, like Kerbal Atomics' gas cores). This mod also supports atomic rockets that have LOX-augmented second mode.

![screenshot](https://i.imgur.com/8gNXvRi.png)

> :bulb: This mod involves an opt-in system. Parts must be tagged and correctly in order to be handled.

> All affected engines, in addtion to the details below, also receive Kerbalism radioactivity. This rating scales with the part's dry mass.

> :warning: WBI Classic Stock is not supported.

> :small_orange_diamond: = Given values are for reference and will scale with the original thrust and Isp of the affected engine.

## NTR Primary/Single Mode
Rational Resources Nuclear Family operates on any atomic rocket part that is given the tag `RRNF = Yes`. The affected engine gets its title appended and gets cloned: one instance for oxidating agents (propellants that contain Oxygen) and one for reducing agents (propellants that don't contain Oxygen).


The Oxidating Agent engine receives the following options for its primary mode: 

| Propellant | Vac Isp :small_orange_diamond: | Thrust :small_orange_diamond: | Detail |
| -- | -- | -- | -- |
| Carbon Dioxide | 283 s | 60 kN | Impulse is as good as the average LiquidFuel rocket, and this is the most convenient option due to the great abundance of Carbon Dioxide in some planets' atmospheres. |
| Carbon Monoxide | 253 s | 60 kN | This is the highest thrust option among all RR NTR options and is fitting for use at inner rocky worlds with atmospheres. |
| Water | 370 s | 45.6 kN | This is the more economical high thrust option, immediately superior in performance to the likes of the LV-303 and LV-909 LFO engines. |


The Reducing Agent engine receives the following options for its primary mode: 

| Propellant | Vac Isp :small_orange_diamond: | Thrust :small_orange_diamond: | Detail |
| -- | -- | -- | -- |
| Hydrogen | 800 s | 60 kN | This is the highest efficiency, baseline option for NTRs. |
| Ammonia | 400 s | 120 kN | This may be very niche but is made very available, the Ammonia option trades exactly half the baseline efficiency for double the thrust. |
| Nitrogen | 253 s | 40.2 kN | Nitrogen as a propellant may be very niche and is poor in terms of Isp, but it is common in planetary crusts, atmospheres, oceans, and exospheres. |
| Methane | 606 s | 79.8 kN | This option trades a very modest portion of efficiency for thrust but makes use of the highly demanded alternative propellant for launchers and boosters. |


## LANTR Mode
All affected engines which have a second engine mode are ensured to have Hydrogen + Oxidizer as the propellants, with a fixed ratio. No other changes are made.


This mod also enables any atomic jets to have half-life behavior (requiring IntakeAtm + EnrichedUranium) and adds Kerbalism radioactivity to any supported engine.

## NTJ
Rational Resources Nuclear Family operates on any atomic jet part that is given the tag `RRNTJ = Yes`. The part is changed to require IntakeAtm + ThermalPower as its propellants.. It is also given a stock converter module (the nuclear reactor) and capacity for EnrichedUranium + DepletedFuel. This reactor is required for the production of ThermalPower (the added propellant) but will also produce ElectricCharge and serve as a useful secondary or tertiary power source.