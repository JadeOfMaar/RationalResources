![RRlogo](https://raw.githubusercontent.com/JadeOfMaar/RealisticResources/master/RRlogo.png)
# Rational Resources
Rational Resources is inspired by [Realistic Atmospheres](https://github.com/OhioBob/Realistic-Atmospheres) made by [OhioBob](https://github.com/OhioBob/) and operates on the KSP Community Resource Pack or WBI Classic Stock.
Rational Resources strips out the entirely random resource distributions and applies "distribution templates" (carefully configured groups of resource distributions) according to the logically expected class and composition of a body. While this mod is installed, un-configured bodies will have no resources at all.

This mod enables planet makers to easily assign these distribution templates to their planet packs and skip the headaches of figuring out and writing the individual nodes themselves, and assorting all of their writings into several per-resource config files.

## Resource Distribution Templates
The following templates have been made available. **Unique** entries are templates exclusive to a stock planet, designed either to make that planet resemble a real life celestial body or because it is an extreme oddity.
* Eve, a hybrid class methane + metal world, is not known (to me anyway) to be possible.
* Minmus, an entirely ice world cannot exist in the habitable zone of a star. It is made to possess Nitrogen and no metals.
* Mun, as the real Moon, is made to possess a large fraction of Oxygen and MetalOre.
* Duna, akin to Mars, is given a strong presence of CarbonDioxide, Minerals and MetalOre.

The Star series templates apply resource bands in the vein of [Stellar Populations](https://en.wikipedia.org/wiki/Stellar_population), automatically making them all viable as mining destinations for interstellar vessels. Population 1 is current and rich with many common resources while the later ones retreat in time to a younger universe and become increasingly abundant in only Hydrogen and CRP's Antimatter or Classic Stock's Graviolium.

| Surface | Ocean | Atmosphere | Unique | Exo (Trace) |
| --- | --- | --- | --- | --- |
| Rock | Terra | Default (CO2-rich) | Eve | Rock |
| Silica | Nitrogen | Terra | Mun | Ice |
| Vulcan | Methane | Vulcan | Minmus | |
| Rock-Metal | Ammonia | Ice-Water (Thick, N2-rich) | Duna | |
| Rock-Ice | Lava | Ice-Water (Thin, CO2-rich) | | |
| Ice-Water | MudWarm | Ice-Ammonia | |
| Ice-Methane | MudCold | Ice-Methane | |
| Ice-Nitrogen | | Ice-Nitrogen | |
| | | Gas (Jovian) | |
| | | Gas (Uranian) | |
| | | Gas (Sudarsky II) | |
| | | Gas (Sudarsky III) | |
| | | Star (Population 1) | |
| | | Star (Population 2) | |
| | | Star (Population 3) | |

## Active Resources
With some partial respect to realism, this mod drastically reduces the presence of the stock "Ore" resource in order to starve the use of this omnipotent and exceedingly abstracted resource, and to encourage the use of the distinct and specialized resources, and to encourage creation and use of the part mods that revolve around these. The exact resources used are named below as a heads-up to players:

**Surface and Atmosphere resources**
* Ammonia, CarbonDioxide, ExoticMinerals, Gypsum, LqdHe3, Hydrates, Hydrogen, MetalOre, MetallicOre, Methane, Minerals, Nitrogen, Ore, Oxygen, RareMetals, Rock, Silicates, Substrate, Uraninite, Water.

**Ocean resources**
* Carbon, ExoticMinerals, Gypsum, LqdAmmonia, LqdCO2, LqdMethane, LqdNitrogen, LqdOxygen, MetalOre, MetallicOre, Minerals, RareMetals, Rock, Water.

**Star resources**
* Ammonia, Antimatter, Carbon Dioxide, LqdHe3, Hydrogen, LqdDeuterium, Methane, Nitrogen, Oxygen, XenonGas.

## ISRU
 With omnipotent Ore being stripped of its Godhood, the following ISRU chains are proposed and encouraged for use by seasoned modders. Ore abundance is capped to 5% and its presence chance to 80%. It will be inconvenient for most players... but it will still be around.

Ore tanks will be changed via B9 Part Switch, to hold the cryogenic input resources. The intended ISRU chains that will be provided can be viewed in [Issue #1](https://github.com/JadeOfMaar/RealisticResources/issues/1).

## Compatibility
Rational Resources purges resource distributions placed by most other mods. Untagged resource distributions are all deleted in the ModuleManager `:FOR[zRationalResources]` pass. The whitelisting mentioned below largely only applies to global/universal placements, and nearly no specific/per-planet placements in order to prevent unwanted high concentrations like Karbonite on Eve.

**Whitelisted resources**
* Antimatter, ArgonGas, LqdHe3, LqdDeuterium, LqdHydrogen, XenonGas. (used by at least the Near Future Tech and Far Future Tech mods).
* __Not__ Dirt (used only by USI MKS. Its absence should be but a minor hurdle to MKS players).

Easy and full compatibility is granted between a configured planet pack and the following mods:
* Kerbalism
* TAC Life Support
* Near Future Tech suite
* Cryogenic Engines
* Kerbal Atomics
