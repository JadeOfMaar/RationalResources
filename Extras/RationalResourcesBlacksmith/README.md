# Rational Resources Blacksmith
This modlet provides an upgrade-able pseudo industrial furnace in the unused crew space of the stock science lab and makes use of the pseudo resource "RRWork" and the CRP "ThermalPower" resource. RR Blacksmith is a stock modules involved mechanism for enabling kerbals to refill certain resources that generally cannot be refilled.
![screenshot](https://i.imgur.com/7iP3z9m.png)

## Blacksmith Stats

The Blacksmith module is upgrade-able via B9 PartSwitch but the highest level requires supported tech tree mods as the stock tech tree is not tall enough.

The input and output resources are per second and multiplied by crew capacity of the part. The outputs on each higher level are exactly 3x that of the lower level but the input of the higher level is roughly 40% that of 3x of the same part at the lower level.

| Level | Inputs | Outputs | TechRequired |
| -- | -- | -- | -- |
| 1 | 15 EC | 0.2 RRWork + 0.1 ThermalPower | N/A |
| 2 | 20 EC | 0.6 RRWork + 0.3 ThermalPower | advMetalworks |
| 3 | 25 EC | 1.8 RRWork + 0.9 ThermalPower | nanolathing |
| 4 | 30 EC | 5.4 RRWork + 2.7 ThermalPower | exoticAlloys :small_blue_diamond: |

> :small_blue_diamond: This node does not exist in the stock tech tree. This upgrade currently only appears if Community Tech Tree is present.


## Resources

Since these resources cannot be pumped around, converter modules are added to these parts and consume RRWork to simulate the kerbals doing the needed manual labor to transfer them. Some, but not all of the cases below additionally require ThermalPower which is used to simulate the need to have these "freshly produced" resources in a liquid state for transfer before they dry.

> :bulb: WBI Classic Stock is supported. The resources: **EnrichedUranium, DepletedFuel, ThermalPower** are substituted with **NuclearFuel or NuclearWaste, CoreHeat** respectively.

Resources supported:

### Ablator
Very straightforward in intention: This allows for refreshing the ablative material on any part that holds this resource. I envisioned this support being necessary for the niche case where a player may want to deploy a craft with "reusable heatshields" from one place to another.
Its required resource combos are:
* Ore + ThermalPower + RRWork
* Carbon + Water ThermalPower + RRWork

### SolidFuel
Demand is pretty solid for a mechanism for refueling solid rockets. Based on the real and plusible concept of recovering and reusing solid rockets, this case goes without further explanation.
Its required resource combos are:
* Ore + RRWork
* Alumina + RRWork
* LqdAmmonia + LqdNitrogen + LqdOxygen (Assuming Ammonium Nitrate composition)

> :warning: Note that no means is provided for making sold rockets able to shutdown and restart.

### NuclearFuel
In the absence of Near Future Electric, the following are applied to any part that holds EnrichedUranium:
* A refill converter which consumes Uraninite + ThermalPower + RRWork
* A disposal converter which consumes Ore + DepletedFuel + RRWork (simulating a means of burying the waste. Please only use this while landed.)



## Rational Resources Blacksmith Family
A secondary config produced by someone else. This adds a derivative of:
* The Blacksmith "RRWork" function to any part that has EL Workshop productivity of at least 1, and scales the RRWork production rate with the EL Workshop rating.
* The Blacksmith "ThermalPower" function to any part that has EL Smelter module, and scales  ThermalPower production with the EL Smelter's conversion rate.