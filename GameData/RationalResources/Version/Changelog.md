# Rational Resources

## 3.4
* Updated `RationalResources`:
  * Added EL ScrapMetal resource and fixed density and cost of EL Metal.
* Updated `RationalResourcesCompanion`:
  * Added Fluorine tank options.
  * Added System Heat boiloff config for Procedural Parts.
  * Added Omniconverter recipe for RocketParts production.
  * Fixed edge case issue of duplicate LqdMethane tank option for Procedural Parts (+ SMURFF + CryoTanks).
  * Made stock drills always have MetalOre option.
  * Moved MetalOre resource placement to Template Agnostic.
* Updated `RationalResourcesKerbalism`:
  * Added missing Uraninite SETUP node. The lack of this caused drills to break.
  * Added tag for RR Chill-O-Tron to receive heater slots.
  * Adjusted balancing for crustal drills and atmo scoops. Lowered minimum required resource abundance and scaled throughput by 10x.
  * Adjusted balancing for exo scoops. Scaled throughput by 10x. Added missing resource options.
  * Adjusted balancing for ocean pumps. Lowered minimum required resource abundance and scaled efficiency by 100x.
* Updated `RationalResourcesNuclearFamily`:
  * Added Fusion Family. Engines opted in can use B9PS to accept increasing ratios of Hydrogen or Water and trade Isp and waste heat for thrust.
  * Added condition: solid core rockets and thermal nozzles don't ask for ThermalPower when System Heat installed.
  * Changed gas core rockets to hold 3x EnrU and always sip on EnrU. The mass flow should be constant across propellant selection.
  * Changed solid core rockets and thermal nozzles to remove heat, not add it.
  * Fixed thermal nozzles ignoring the Require ThermalPower toggle.
  * Fixed thermal nozzles thrust curves following the propellant fill rate.
  * Revised formulas and heat curves for System Heat engines.

## 3.3.2
* Updated `RationalResources`:
  * Adjusted Xenon storage density. It seemed excessive.
* Updated `RationalResourcesCompanion`:
  * Fixed broken configs for Argon and Xenon (primarily affecting NF Propulsion installs) due to renaming gas tank types.
* Updated `RationalResourcesParts`:
  * Added Argon and Xenon to gas tanks.
  
## 3.3.1
* Updated `RationalResources`:
  * Added missing buff to Methane (gas) storage density.
* Updated `RationalResourcesCompanion, RationalResourcesSSPXRTanks`:
  * Fixed broken Ore tank config due to renaming gas tank types.

## 3.3.0
* Updated `RationalResources`:
  * Added and sorted/renamed gas tank types for RR gas tanks.
  * Fixed previous storage density problems with gas tanks.
* Updated `RationalResourcesCompanion`:
  * Fixed actually terribly bugged recipe for FFT Orion Pulses.
  * Removed old config that was no longer needed but excessively de-powered stock 1.25m refinery. It should now be 4x what it erroneously was.
  * Updated boxed ISRU, nerfed power scaling to better fit 2.5m stock refinery.
* Updated `RationalResourcesParts`:
  * Fixed dry masses of gas and cryo tanks. (Finally??? I really hope so.) They now compare very well with Procedural Parts' gas tank.
  * Updated boxed ISRU, added missing mass to boxed ISRU to better fit/compare with 2.5m stock refinery.

## 3.2.3
* Updated `RationalResourcesKerbalism`:
  * Restored (missing?) Minerals Splitter and ExoticMinerals Splitter recipe.
* Updated `RationalResourcesNuclearFamily`:
  * Fixed engineID error with thermal nozzles.
  * Ensured System Heat module wiring only interacts with Rational Resources' own instances and not instances of those modules placed by other patches.
  * Re-added Sterling Engines. (Finally made up my mind with this one.)

## 3.2.2
* Updated `RationalResourcesCompanion`:
  * Removed erroneous detection that hid FFT Orion pulse recipe from refineries.
* Updated `RationalResourcesNuclearFamily`:
  * Fixed Atomic Age lightbulb not tagged as a gas core.

## 3.2.1
* Updated `RationalResourcesParts`:
  * Made System Heat Boiloff optional.
  
## 3.2.0
* Updated `RationalResources`:
  * Added basic support for all intakes (so they will hold CRP's IntakeAtm or CSR's Atmosphere). Should have added this way back when CRP stopped placing resources.
* Updated `RationalResourcesParts`:
  * Added Configurable Containers support. Cannot be affected by B9PS so wrapper tank height variants are cosmetic only.
  * Updated Main Coon NTJ to fit with RRNF overhaul below.
  * Updated tanks to use System Heat Boiloff when System Heat installed.
* Updated `RationalResourcesNuclearFamily`:
  * Added gas core NTR support;
  * Added tweak config so player can choose to: Replace (or not) SH-specific reactor behavior with RR-specific reactor behavior. On by default.; Increase generator powers to make negines more usable as main reactors; Enable (or not) ThermalPower demand in the propellant options. Off by default due to dV calculator issues.
  * Added known engines from mods: Kerbal Atomics; SpaceTux Recycled Parts: FTmN, FTmN Improved, LVN Clusters.
  * Fully tested/developed Classic Stock Resources compatibility.

## 3.1.3
* Updated `RationalResourcesKerbalism`:
  * Undid removal of stock fuel cell options.
* Updated `RationalResourcesSquad`: 
  * Fixed missing mesh name keys for the service tanks in Mk2 & Mk3 Expansion.
  * Excluded service bays in Mk2 & Mk3 Expansion from getting tank options.

## 3.1.2
* Added/Updated detection of Classic Stock Resources vs Community Resource Pack in `RationalResourcesJetFamily`, `RationalResourcesNuclearFamily`.
* Added System Heat integration for engines on Classic Stock Resources in `RationalResourcesNuclearFamily`.
* Fixed texture path error with SolidFuel ramjet in the demo parts.
* Fixed major issue with mass and volume of inline cryo tanks and inline gas cache tanks.
* Fixed issues due to providing for Sterling Systems Kerbalism: Removed those things so they can be a modlet by themselves.
* Fixed issues with engine detection in `RationalResourcesJetFamily`: 
  * Should not care about engineID when ignoring multimode engines.
  * Only respect ModuleEnginesFX and ignore other variants of this module.
* Updated detection for Kerbal Star systems 2: Aethera system.

## 3.1.1
* Removed mentions of Aurum resource. It caused unexpected problems for SSPXr users.

## 3.1.0
* Added extra/empty folder toggle: `RationalResourcesOmniConverters`:
  * Makes refineries and fuel cells use WBI Omniconverter module vs PAW spam.
* Updated `RationalResourcesCompanion` (Classic Stock):
  * Added Omniconverter recipe: Fizzy Boom. Produces Cider resource.
  * Added Omniconverter recipe: Water Splitter. Produces Propellium and Oxium.
  * Added Omniconverter recipe: Zeonium Splitter. Produces XenonGas and Metal.
  * Added Sterling Systems template tags to Omniconverter recipes.
  * Removed Zeonium from B9 subtypes injection. This is not a cryogen.
* Updated `RationalResourcesNuclearFamily`:
  * Removed Bluedog Design Bureau from opt-in. Conflicts with the affected engines' own B9 toggles.
* Updated `RationalResourcesParts`:
  * Added missing specular map to MISPLACED harvesters.
  * Added CCK tags.
* Updated `RationalResourcesParts` (Classic Stock Resources):
  * Added missing CRP detection. Fixed major and fatal issues.
  * Updated Gas Cache Tanks to become OmniStorage when CRP not installed.

## 3.0.4
* Fixed unbalanced brackets in Far Frontiers support config.

## 3.0.3
* Updated RationalResources:
  * Added Far Frontiers support. (Authored by 3rd party.)
* Updated RationalResourcesCompanion, RationalResourcesKerbalism:
  * Added recipe for FFT Orion's pulse units.
  * Added recipe ExoticMinerals Splitter. Outputs are of value to certain other mods.
  * Added recipe Minerals Splitter. 

## 3.0.2
* Removed 000_RationalResources:
  * Restored things as they were before.
  * Introduced `:FOR[RationalResourcesTemplateCustom]`. Modders can use this to preclude all built-in templates so only their own will apply to planets.
  * Introduced `:FOR[RationalResourcesNoCRP]`. Modders can use this to preclude just the CRP templates and the CRP functions in RationalResourcesCompanion. Classic Stock functions in RationalResourcesCompanion are now inactive without it.
  * Introduced `:FOR[RationalResourcesAU]`. This will cause RationalResources to not attempt to apply resources to the stock planets. This is useful for system replacers, especially the re-skin kind like JNSQ or Techo's stock overhaul. (This was always around, though somewhat unused.)
  * Introduced TemplateTag key in the resource placement configs. Modders may find it useful to be able to target these configs by their associated resource library.

## 3.0.1
* Updated 000_RationalResources:
  * Removed non-optional folder to make less for the player to need to remember.
* Updated RationalResourcesNuclearFamily:
  * Fixed missing engineID issue with single-mode nukjet engines.

## 3.0.0
* Created `000_RationalResources`. Split resource templates out of `RationalResources` folder and took a new approach to play modes. Allows for modders to easily change what the temapltes contain and are applied to planets.
* Created extra, `RationalResourcesSandcastle`. Still experimental. Classic Stock not yet fully supported.
  * Removed placeholder config from `RationalResourcesELUtilities`.
* Updated RationalResources:
  * Added asteroid and comet resource configs.
  * Added asteroid and comet analysis module to RR Ground Scanner.
  * Fixed tank ratio for D+3He.
* Updated RationalResourcesCompanion:
  * Added Sterling Systems refinery tags to Omniconverter recipe configs.
  * Updated Monazite Splitter process. Added Thorium to outputs.
  * Updated processes that output Deuterium to dump Hydrogen when Deuterium is wanted more than Hydrogen.
* Updated RationalResourcesNuclearFamily:
  * Added System Heat compatibility.
  * Fixed errors with thermal nozzles patch. Methane mode targeted wrong mode of dual mode engines and there was a very large inconsistency with air-breathing mode. Thanks @Velcroish
* Updated RationalResourcesParts:
  * Added missing Deuterium to gas tank options.
  * Removed deploy/retract step for exo scoops since they do not animate.
* Updated RationalResourcesSquad:
  * Disabled Structural subtype on request (hopefully). Tanks should now always hold the original fuel mix.

## 2.0.7.1
* Updated RationalResources:
  * Added ExoticMinerals option to Ore tanks.
* Updated RationalResourcesKerbalism:
  * Hopefully fixed Chill-O-Tron issues of resource switching and KerbalismSystemHeat.

## 2.0.7
* Updated RationalResources:
  * Added missing hotspots for pure Water on Kerbin, Duna, Laythe, Moho.
  * Updated biome templates (CRP only).
* Updated RationalResourcesBlacksmith:
  * Created/Fixed SystemHeat integration.
* Updated RationalResourcesELUtilities:
  * Added protection against possible duplicate SystemHeat module.
  * Updated SystemHeat efficiency curves.
* Updated RationalResourcesKerbalism:
  * Fixed atmo scoops seeking gas form resources when liquid forms are placed.

## 2.0.6.1
* Updated RationalResources:
  * Fixed JNSQ support.

## 2.0.6
* Updated RationalResources:
  * Added Kerbal Star Systems 2 support.
  * Updated JNSQ support.
  * Removed an odd need of RationalResourcesCompanion that resulted in B9PS fatal errors.
* Updated RationalResourcesKerbalism:
  * Added MaterialKits prcoess.
* Updated RationalResourcesParts:
  * Added boiloff configs to RR CryoTanks for a rather wide array of cryo resources.
* Updated RationalResourcesNuclearFamily:
  * Removed Sterling Engines. RRNF will be baked into Sterling Engines.

## 2.0.4
* Updated RationalResources:
  * Added missing Spodumene scanner option.
  * Updated exo templates' Rock resource provisions.
* Updated RationalResourcesJetFamily:
  * Added cryofuel switcher for rocket engines. (Required by OPT spaceplane and possible other mods.)
  * Added provisions for air-breathing engines that run LFO + deoxygenated IntakeAtm. (Required by OPT spaceplane.)
* Updated RationalResourcesNuclearFamily:
  * Added provisions for dual-mode thermal nozzle engines (with toggle for fan-based or rocket-based air-breathing mode).
  * Fixed thrust curve issue with thermal nozzle fuel options.
* Updated RationalResourcesParts:
  * Fixed patch problem with Wrapper Intake.

## 2.0.3
* Updated RationalResources:
  * Fixed atmo scanner not detecting "liquid" resources.
* Updated RationalResourcesCompanion:
  * Added missing LqdDeuterium output to RealFuels Water Splitter process.
  * Doubled the resource flows (except for ElectricCharge) of Methalox, Hydrolox and Water Splitter processes.
* Updated RationalResourcesKerbalism:
  * Added missing Uraninite drill option.
  * Doubled the resource flows of Water Splitter process.
* Updated RationalResourcesNuclearFamily:
  * Added `RRTN` key to opt-in for targeting thermal nozzle parts.
  * Moved Sterling Systems' thermal nozzles under this.
* Updated RationalResourcesParts:
  * Adjusted part costs (thanks to @Vaskritaya).
* Updated RationalResourcesSquad:
  * Fixed CryoTanks detection: Do not add own switcher setup to stock tanks if CryoTanks installed.
  * If CryoTanks not installed, ensure stock tanks have boiloff module.

## 2.0.2
* Updated RationalResourcesKerbalism:
  * Deleted Squad nuke reliability patch. This should be in the `KerbalismSidePatches` mod.
  * Fixed all B9PS problems.
* Updated RationalResourcesNuclearFamily:
  * Restored fix for B9PS warnings with BDB nuke engines and Skyhawk Science mod.
* Updated RationalResourcesParts:
  * Updated descriptions and stats (mass, cost, tech node). Thanks in part to @Vaskritaya.
  * Added wrapper intake to opt-in as ocean harvester.
  * Un-deprecated and un-nerfed boxed converters. Made these less heavy too.

## 2.0.1
* Added KerbalismSystemHeat detection to the Cryomat.

## 2.0
* Added LqdHe3 to atmo scoops options.
* Added patch that adds options to the stock drills: Alumina, CarbonDioxide, Hydrates, Monazite.
* Added parts:
  * "MISPLACED" series ram air harvesters for LACE type engines.
  * "Chill-O-Tron" 2.5m freezer which replaces the boxed freezer.
  * "Therm-O-Tron" 1.25m heater which replaces the boxed heater.
  * 5m exosphere scoop with 100m funnel span.
  * "Giga-Tron" 3.75m refinery which produces (only) FusionPellets.
  * Gas Cache tanks (inline, 1.25m, 2.5m, 3.75m, 5m) for use with harvesters or refinery edge cases.
  * Discount CryoTanks (inline, 1.25m, 2.5m, 3.75m, 5m) for use with RationalResourcesNuclearFamily and the Giga-Tron.
  * Wrapper tanks, intake and Convert-O-Tron (1.25m ~ 2.5m size).
* Changed some remaining atmosphere and exosphere resources from gas to liquid form for consistency.
* Changed harvesters' options to follow suit.
* Deprecated RR Parts: Hydroscoop beta, Boxed heater, Boxed freezer.
* Removed integration of Squad radial intake.
* Reduced atmospheric LqdHe3 presences as most Helium presence is the regular inert kind.
* Updated parts integration to require WBI Pathfinder, not Classic Stock, for insertion of WBI OmniStorage, OmniConverter or "Omni-" harvester modules into parts. WBI integration on the whole is on the fence for now.
* Updated Kerbalism integrations:
  * Reduced drills' output and ElectricCharge demand to 1/5 previous values. this should be the proper scaling for them.
  * Do not remove WBI custom harvester module from WBI Pathfinder's Lasso series parts.

## 1.61
* Fix EL System Heat problems.
* Replace Carbon Extractor process with Ore Splitter which outputs Oxygen and Carbon.
* Split ion engine reliability buffs from `RationalResourcesKerbalism` into new modlet, `KerbalismSidePatches`.
* Split nuke engine reliability buffs from `RationalResourcesNuclearFamily` into new modlet, `KerbalismSidePatches`.

## 1.60.1
* Added mods to the opt-in of `RationalResourcesJetFamily, RationalResourcesNuclearFamily, RationalResourcesRCSFamily` where appropriate:
  * Mk2 Expansion, Mk3 Expansion, SXT, WaterDrinker.
  * Excluding RCS parts that are also engines or have multiple RCS module.
  * Excluding pure electric jet engines.
* Updated `RationalResourcesKerbalism`:
  * Added SolidFuel ion detection. This covers the Supplementary Electrical Engines mod.

## 1.60
* Added extra: `RationalResourcesJetFamily`.
  * Please updates `RationalResourcesSquad` if you use it, to delete its SquadJets configs (or just delete these manually).
  * Increases ElectricCharge demand on electric engines.
* Added rebalance patches for Kerbalism reliability:
  * `RationalResourcesKerbalism` now provides this to ion engines, stock and mod. (Detection logic is currently basic: If the engine eats Xenon, Argon or Lithium, it is assumed to be an ion engine. Mis-catches may occur) Ion engines now have 3 years MTBF and a few years of burn time.
  * `RationalResourcesKerbalism` now provides this to Squad NERV and Restock+ Cherenkov. Atomic engines now have 1 year MTBF and 2+ days burn time.
  * `RationalResourcesNuclearFamily` now provides this to all tagged engines. These engines now have 1 year MTBF and 2+ days burn time.

## 1.51
* Added engines to opt-in of `RationalResourcesNuclearFamily`:
  * NF Aero's J-N160 'Fireflash.'
* Localized Ore tank option titles.
* Updated behaviors and balancing of `RationalResourcesNuclearFamily`.

## 1.50
* Rebalanced Uraninite conversion in `RationalResourcesBlacksmith`.
* Added FusionPellets to squad tanks via `RationalResourcesSquad`.
* Updates to`RationalResourcesCompanion`:
  * Added Minerals tank option to Ore tanks for use by RR's EL recipes.
  * Minor tooltip fix.
* Added engines to opt-in of `RationalResourcesNuclearFamily`:
  * NF Aero's Project Eeloo.
  * Sterling Systems' SULEU NTRs.
* Updates to `RationalResourcesELUtilities`:
  * Added elementary config for SandCastle recipes.
  * Changed some EL tanks to use B9 resource switching and hid the rest.

## 1.49.1
* Updated `RationalResourcesNuclearFamily`:
  * Removed BDB Nerva II from opt-in as it caused conflict with RealFuels Stockalike
* Updated `RationalResourcesCompanion`:
  * Allowed Ore tank patch when RealFuels installed. Answered request for Carbon storage when producing Kerosene under RealFuels.

## 1.49
* Added **Konstruction** (Equipment, Minerals, Metals) storage template for WBI template system. This goes with RR Equipment formula.
* Added RR MaterialKits option for Convert-O-Trons. (This currently only appears if Global Construction installed.)
* Fixed ElectricCharge scaling issue in Convert-O-Trons.
* Renamed some converter options (added "RR" prefix) to add distinction vs standard/other formulas.
* Updated `RationalResourcesELUtilities`:
  * Added EL-to-CRP handling for WBI template system. Written by **@ 0xE1E10** on GitHub.
* Updated Kcalbeloh resource placement config: A planet was internally renamed.

## 1.48
* Added (missing) Freeze Deuterium option to omniconverters.
* Added Carbon Monoxide fuel tank options in `RationalResourcesSquad`.
* Added Explodium (Classic Stock) resource definition to cure fatal issue when Classic Stock does not define this resource because Far Future Tech is installed.
* Updated energy demand in EL System Heat converters in `RationalResourcesELUtilities`.
* Updated Ore tank integration (to do nothing) when InterstellarFuelSwitch installed.
* Updated Silicates and ISRU chains to reflect SiO4.
* Updated: `RationalResourcesBlacksmith`:
  * To apply its changes late in MM runtime in order to allow NTRs affected by `RationalResourcesNuclearFamily` to get nuclear fuel refill and nuclear waste disposal options.
  * To prevent inserting duplicate work or furnace factor tags into parts (in case of parts that specify their own factor).
  * Rebalances with respect to System Heat mechanics and ThermalPower now being treated as Megajoules or Megawatts by Rational Resources.
  * Updated detection of CRP vs Classic Stock.
* Updated `RationalResourcesNuclearFamily`:
  * Added Bluedog Design Bureau to opt-in. (selection by @ dangaffa )
  * Added SpaceTux Recycled Parts: FTmN Atomic Rockets to opt-in.
  * Added SpaceTux Recycled Parts: LVN Clusters to opt-in.
  * Moved CO propellant option to Reducing Agent side.
  * Updated detection to only apply to engines that use ModuleEnginesFX.

## 1.47
* Housekeeping...
* Added support for Kcalbeloh.
* Added support for OWR.
* Added ExoFire template for Io-like worlds. Partially placeholder.

## 1.46
* Added Extra: `RationalResourcesELUtilities`.
* Added detection for On Demand Fuel Cells (do nothing to fuel cells; prevent conflict).
* Added KPBS Ore and LFO tanks support.
* Balance pass on Kerbalism drills. Apparently they were at 20% of baseline performance.
* Deprecated Extra: `RationalResourcesELCRP`.
* Fixed unforeseen problems with Squad drills and Kerbalism.

## 1.45.1
* Fixed unforeseen problems with KPBS and Kerbalism.
* Fixed minor problem with Ore tanks and SMURFF.

## 1.45
* Added KPBS ISRU support by @ CoriW on the forum.
* Added detection for InterstellarFuelSwitch (do nothing) and SMURFF (required compatibility) to `RationalResourcesSquad`.

## 1.44
* Added compatibility (excluding template adaptation) for The Gold Standard.
* Balance pass in `RationalResourcesNuclearFamily`. Lower Isp propellants are ensured greater thrust and oxidating agent NTRs have greater baseline thrust due to default lower Isp.
* Changed (most if not all) exo resources to liquid form and exo scoop modules to suit.
* Deleted redundant CO2 generators.
* Fixed RR_MetallicOre issue when CRP not installed (hopefully).
* Fixed issues with Kerbalism + WBI Pathfinder.
* Rewrote and divided RR Omniconverter recipes between basic, CRP and Classic Stock.
* Tagged all engines except the open cycle one in Kerbal Atomics for `RationalResourcesNuclearFamily`.

## 1.43
* Changed requirement of harvesters and refineries from Classic Stock to WBI Pathfinder. When Pathfinder is installed, harvesters can use one module to produce all resources, refineries become switchable and decluttered.
* Fixed excessive Water demand of Hydrolox production (increased Hydrolox outputs).
* Fixed MetalOre and Metal subtypes not showing in Ore tanks. Yay typoes.
* Deleted legacy Kerbalism config that caused repeat modules on, and breakage of the stock drills.
* Updated handling for stock drills and refineries to cover for RO Kerbalism which does not handle the stock parts.
  
## 1.42
* Added Air Maker OmniConverter option for the presence of WBI Snacks! with Air!
* Fixed output resource flow mode in RR Boxed Compressor and Decompressor.
* Fixed template error with JNSQ Lindor.
* Updated (hopefully) Extras/RationalResourcesELCRP to catch any resource converters that consume/produce Metal to do Metals instead; consumes MetallicOre to consume MetallicOre instead.
* Updated Extras/RationalResourcesNuclearFamily so integrated nuclear jets produce and consume more ThermalPower, and convert to ElectricCharge without needing to throttle up the engine.
* Updated Extras/RationalResourcesSquad to handle Kerbondyne branded parts that hold LiquidFuel but not Oxidizer. The presence of Buffalo 2's bioreactor caused an error where MM will not save the config cache.
* Updated Extras/RationalResourcesSSPXRTanks to catch all such tanks and replace Metal subtype with Metals.
* Updated Procedural Tanks (thanks to @ VeronikaKerman):
  * Alphabetically sorted tank types.
  * Added Helium and/or Helium3 gas form tank types.
  * Added boiloff config for Deuterium and Helium-3.
  * Fixed (hopefully) Ore reappearing after selecting another tank type.

## 1.41
* Added Extras/RationalResourcesELCRP/RR_EL-RF.cfg
  * This firstly changes the default resource link and resource recipe from LFO to Kerosene + LqdOxygen.
  * This secondly adds other (hopefully popular) resource links and recipes.
* Added support for Quack Pack (planet pack).
* Added support for Real Exoplanets (planet pack).

## 1.40
* Fixed tag issue with opt-in system in `RationalResourcesNuclearFamily`.
* Added `Advanced Jet Engine` detection to `RationalResourcesSquad` jet engine patch to prevent a significant conflict.
* Added LqdDeuterium + LqdHe3 options to ProcTanks.
* Fixed SSPXr TACLS patch in `RationalResourcesTACLS`. An error in root node configs was the cause of serious problems. Thanks to @ Vexxel on the forum.
* Fixed "duplicate subtypes: Methane, Methalox" B9 issue.
* Fixed repeat tank types in ProcTanks (causes game-breaking bug): MetallicOre, Metals
* Major change: Rational Resources now favors MetallicOre and Metals instead of Extraplanetary Launchpads' own MetalOre and Metal. Authored by @ Veronika Kerman on the forum.
  * Added extra: `RationalResourcesELCRP`. Forces Extraplanetary Launchpads to use MetallicOre and Metals instead of its own MetalOre and Metal.


## 1.33
* Added Configurable Containers detection to Ore tanks opt-in to cure related MM errors.
* Added stock inventory volumes for RR parts except for tanks and engines.
* Changed Metal, MetalOre resources to be defined with no concern for the presence of EL itself or other mods that may also declare them. Leave redundancy handling entirely to MM's code. This answers edge cases where these resources still don't get defined at all, and consequent issues like B9PS-SSPXr fatal errors.
* Fixed duplicate subtype issue for Mk2 Expansion (in the `RationalResourcesSquad` extra.) Spotted by @ Eberkain.
* Fixed inconsistent Oscar B volume with respect to other Oscar tanks added by Restock+. Spotted by @ Eberkain.
* Updated Procedural Parts integration (entirely by @ VeronikaKerman):
  * Added boiloff with handling for a couple of resources.
  * Added Deuterium gas.
  * Reduced capacity of very dense resources (MetallicOre, Metals, Monazite, RareMetals)...
  * SMURFF compatibility.
  * Tank volume consistency fixes.
* Updated `RationalResourcesNuclearFamily` to handle atomic jet/rocket engines.
* Updated `RationalResourcesSquad`'s fusion fuel options to detect CRP to prevent fatal B9 errors.
* Kerbalism fixes:
  * Added "empty" option for when you want to leave slots open (and hopefully save some funds) on a made-compatible Convert-O-Tron. Thanks to @ Gordon Dry.
  * Added conditional Graviolium option to exo harvesters, and tech limit to this and Antimatter.
  * Fixed double-patching of Chemical Plant. Thanks to @ Gordon Dry.
  * Increased slot counts on integrated exo harvesters (from 1 to 8) so multiple resources can be scooped at once, as it should be. Each slot that is not needed can have an empty loaded into them. Thanks to @ TR_HYDR4.
  * Reduced EC demand in atmo and exo harvesters.

## 1.32
* Bulk fixes for Classic Stock Resources:
  * Added missing surface templates.
  * Added missing Antimatter and Graviolium in gas planet templates.
  * Added missing gas planet, ocean and surface templates.
  * Buffed GrayWater presence (to be partially treated like Hydrates).
  * Fixed Ore presences.
  * Nerfed Rock presence.
  * Removed old gas planet templates.
  * Changed Zeonium abundances (to be partially treated like Substrate).

## 1.31
* Added WBI Play Mode UI configs for some Extras.
* Added Classic Stock Only tank switch to Extras/RationalResourcesSSPXRTanks/ for whoever may find that useful. (Not tested with CRP installed.)
* Fixed Boxed Compressor and Decompressor. They were being treated as Convert-O-Trons. This issue bricked players hoping to take advantage of CO and CO2.
* Fixed missing flow mode parameter in all instances in WBI OmniConverter integration.
* Nerfed the Mk1 and Mk2 SMX generators. They were quite OP.
* Updated Procedural Gas Tank options to not have so much dry mass.
* Updated Procedural Gas Tank options to try to be equivalent with short 2.5m tanks for NFP ArgonGas and CryoTanks LH2.
* Updated Procedural Liquid Tank option to include LqdMethane (unpaired)... CryoTanks does not provide this.

## 1.30
* Assorted and consolidated extras into mod (sub) folders for more CKAN compatibility.
  * Updated `RationalResourcesNuclearFamily` to:
    * Apply 20% Isp buff to LOX mode on tagged atomic rockets. This mod conflicts with `KerbalAtomicsLH2NTRModSupport`.
    * Have complete Classic Stock compatibility.
  * Updated `RationalResourcesRCSFamily` to:
    * Handle all integration of RCS parts, especially the stock ones. This is no longer partially contained/forced by `RationalResourcesCompanion`.
    * Have complete Classic Stock compatibility.
    * Have some RealFuels compatibility.
    * Properly calculate SL Isp.
  * Created `RationalResourcesTACLS` to contain any and all TAC LS configs.
    * Updated TAC LS integration for Airline Kuisine: Air Filter now only extracts Nitrogen, Oxygen and Water, and not everything provided to typical RR atmo harvesters.
    * Updated TAC LS integration for SSPXr following the template style complete rewrite done for, and released in, SSPXr itself.
  * Updated `RationalResourcesSquad` to:
    * Add fuel switching to the Panther, Whiplash, Rapier; Classic Stock supported.
    * Contain the MoreTankSwitches config that supports various parts mods/ their agencies
    * Contain the TankswitchFusionFuel config that adds Deuterium & Helium-3 options to Squad tanks and CryoTanks.  
* Minor adjustments to OmniConverters options.
  * Fixed missing flow mode parameter on ElectricCharge.
  * Changed convert ratio on WBI ElectroPlasma to ElectricCharge from 1:8 to 1:20.

## 1.20
* Added KerbalChangelog support.
* Added support for RealFuels:
  * Applies to any opted-in Convert-O-Trons (including any WBI OmniConverters), Kerosene ocean harvesting and a CarbonMonoxide + Oxidizer option for fuel cells.
  * Does not add fuel cell options to Kerbalism.
  * Does not include configs for tanks, RCS or engines.
  * Renamed some prior converter options to prevent conflict or confusion.
* Added/Adjusted support for RealFuels In Kerbalism.
  * Added profile/mod folder: `RationalResourcesKerbalismRF`.
  * Changed the 4 built-in processes that involve stock propellants to instead involve equivalent real propellants and include blue "RealFuels edition" in the description.
  * Enabled missing Alumina, Hydrates, Spodumene Splitters since they don't involve non-CRP Metal/MetalOre.
  * Enabled slot count (as per the opt-in system) to +1 when upgrades applied. If a mod part opts in with, example: 4 slots, it will automatically have 5 when upgraded.
  * Ensured that the micro-sized Kerbalism Chemical Plant part gets all RR processes and properly scaled.
* Adjusted throughputs in some converters. Some are faster. Some are slower.
* Added Opt-in system for fuel cells:
  * Fills in some nasty blanks that were left open in the previous fuel cells patch for Stockalike Mining Extension.
  * Preserves and extends the re-balance given in Extraplanetary Launchpads.
  * Provides for RealFuels.
  * Will not apply to tagged parts if CryoTanks is installed due to CryoTanks having this system also.
* Fixed Procedural Parts patch:
  * It added a tank option (XenonGas) that already existed and caused that mod to break the ship editors.
  * It added cryofuels options and was not aware of CryoTanks doing the same.
* Moved demo parts into their own folder: `RationalResourcesDemoParts` so players can opt out of having them.
* Moved JNSQ config out of JNSQ and into this mod's package.
* Renamed original `RationalResourcesParts` to `RationalResourcesCompanion`. RationalResourcesParts is now home to only added parts and can be more easily ignored.
* Updated Extras/RR_NuclearFamily:
  * Added CarbonMonoxide NTR option.
* Updated Extras/RR_TankswitchForSquad:
  * Added CarbonMonoxide + Oxidizer option.
  * Does not support RealFuels.

## 1.19.1
* Added support for planet pack: GPP.
* Added to Uraninite abundance in Vulcan template.
* Added template: **AtmPandora** which is akin to **AtmTerra** but has roughly 7% composition reserved for undefined toxic chemicals.
* Added Uraninite to drills and Ore tanks.
* Added Silicates Splitter (+1 path to Oxygen).
* Added Extras/RR_Aluminium.cfg. 
  * This causes Alumina and Spodumene splitters to produce Aluminium instead of Metal; reveals this tank type in propellant tanks; changes the hybrid SRBs to consume this.
* Fixed Kerbalism upgrade slot amount in Freezer and Heater boxes.
* Minor adjustments to Spodumene Splitter.
* Removed Extras/RR_EveLiquidFuelOcean.cfg. Any supported ocean harvester parts will gain LiquidFuel harvester module.

## 1.19
* Added Graviolium Ping experiment. This will appear in any part that is a Graviolium scanner.
* Changed resource whitelist system to only target the resources that RR handles, and no longer purge Handwavium resources. Their owners no longer need to tag them to protect them. This reduces incompatibility with USI on the whole.
* Added support for planet pack: Galaxies Unbound:
  * Graviolium placement and experiment. (Complete.)
  * Majority resource placement (Carried in GU itself, actually.)
  * Planetary Classification experiment (Virtually complete. Will lag behind due to that mod trickling out updates with new planets.)
* Added support for planet pack: MPE (Minor Planets Expansion) in part from forum user @ AtomicRocketBooster.
* Added support for planet pack: RSS (Real Solar System). Science and planet level configuration done. Pending biome-specific configuration.
* Fixed missing Deuterium in Default, Terra atmo templates.
* Fixed for Kerbalism:
  * Enabled Hydrates Splitter and Spodumene Splitter without Metal outputs.
  * Procedural Tanks config will not provide Metal and MetalOre options.
* Reduced abundance values of LqdHe3, Graviolium.
* Replaced Hydrogen with LqdHydrogen to reduce incompatibility with mods that involve mining of this resource.
* Restored and nerfed Dirt resource abundance to reduce incompatibility with MKS.
* Regularized Ore presence so it can be found everywhere. Note: Abundance still nerfed by default.
* Update Extras/RR_TankswitchForSquad:
  * Isolate parts that are tank + engine and allow them to only hold certain bi-propellants and immediately use the chosen bi-propellants.
  * This affects the stock Twin-boar and Restock+ Pug.
  * Supports Classic Stock.
* Updated support for planet pack: JNSQ:
  * Added results for splashed on Huygen.
  * Changed Nara's assigned templates.
  * Changed experiment results to templated form.

## 1.18.1
* Minor fixes to dictionary and Graviolium templates.

## 1.18
* Added acid world templates: **AtmAcidC, AtmAcidN, OcnAcid**. Note that no actual corrosives resources are introduced as no popular mods use them for anything important, or at all, as far as I know.
* Added ocean template: **OcnKerosene**.
* Added more support for Graviolium placement.
* Added templating system for science results and updated support for the following planet packs to comply: Beyond Home, Extrasolar, Grannus Expansion Pack, Outer Planets Mod.
* Added integration for Procedural Tanks.
* Added missing drill options.
* Fixed broken targeting of converter parts for adding modules (non-Kerbalism).
* Fixed some Kerbalism issues that sprung up... Again. Thanks to **@ Clamp-O-Tron**
* Fixed redundancy issue with Methalox tank options when CryoTanks installed since Methalox changed from optional to always available.
* Updated gas planet templates:
  * Completed Sudarsky based template series (AtmGasI through AtmGasV).
  * Deprecated **AtmGasJovian, AtmGasUranian**. Replaced these with **AtmGasI, AtmGasIII** respectively.
* Updated planetary classification experiment to work while splashed (but not while flying or landed).
* Updated surface templates:
  * Changed "specific" stock planet templates to general templates fit for use on any mod planets: [Eve, Mun, Minmus, Duna] to **SrfRockMineral, SrfAlumina, SrfMetalSulfur, SrfMetalCarbon** respectively.
* Updated Extras/RR_StripStockConverters.cfg

## 1.17.1
* Added Graviolium module to RR Scanner Green.
* Adjusted CoreHeat curve for Stockalike Mining Expansion's 3.75m (RefineOre Y-3000) Convert-O-Tron.
* Fixed Ore Tank patch problems. (Includes file-deletion.)
* Fixed double-addition of modules to Squad Convert-O-Trons.
* Other adjustments to Squad and RR Convert-O-Trons.
* Some of these fixes by forum user **@ flart**.

## 1.17
* Added water vapor atmosphere templates: **AtmSteam** (pure), **AtmSteamC** (featuring Carbon compounds), **AtmSteamN** (featuring Nitrogen compounds).
* Adjusted stock Mun's polar water presence: moved from Polar Crater to Polar Lowlands. This will break water miners landed in Polar Crater.
* Minor adjustment to SCANsat resource color overlays.
* Fixed filename issue: **AtmVulcan** was accidentally named **AtmSulfur**.
* Fixed Deuterium issue in **AtmIceNitrogen** template.

## 1.16.2
* Added Restock+ APU to, and removed CryoTanks from RR CCK.
* Added drill support for the standalone "Ventral Drill for stock ISRU" mod.
* Added integration for Snacks! LS: Create Snacks from Hydrates (CRP) or Rock (Classic Stock).
* Added Extras:
  * RR_BlacksmithFamily.cfg which allows for parts to opt-in and have Blacksmith style furnace or workshop (compatible with EL) and does opt-in on EL workshops and smelters.
* Changed part desc heads-up color from green to blue.
* Enabled Convert-O-Trons that opt-in to have configurable efficiency multiplier and configurable slot count (for mod plugins that facilitate module switching such as Kerbalism and WBI OmniConverters).
* Fixed (inaccessible) bug with LqdHe3 placement in Mun (specific) template.
* Fixed and revised Kerbalism integration.
* Revised opt-in patches for converters, harvesters and Ore tanks.
* Updated Extras:
  * RR_ScienceLabBlacksmith.cfg: Added 4th level (not available in stock tech tree) and added support for nuclear material tanks for use when NF Electric not installed; Added Classic Stock support.
  * RR_BlacksmithFamily.cfg: Added Classic Stock support.
* Updated NEEDS and filenames concerning CRP vs Classic Stock to reduce fatal errors concerning WBI Play Mode switching.

## 1.15.0
* Added Extras:
  * RR_RCSFamily.cfg with modlet `RationalResourcesRCSFamily` to add fuel switching to RCS thrusters whether MonoProp, LFO, or MonoProp (WBI Classic Stock). Has default support for NF Aero, NF Spacecraft, most of NFLV, MKIV Spaceplane, KRE.
* Added ISRU options (specific to other mods or parts in them):
  * Water-consuming NSW production to FFT 3.75m smelter part.
  * Blacksmith (Ablator refurbishment) to FFT 3.75m smelter part.
  * EL recipe for KerbalHealth Radiation Shielding.
  * Blacksmith based Shielding refurbishment to all parts equipped with KerbalHealth Radiation Shielding.
* Added/Updated WIP tank options for NF Propulsion (Lihtium,Argon,Xenon).
* Added opt-in ISRU options:
  * Deuterium: Freezer option to RR Boxed Compressor/Freezer.
  * Deuterium: as byproduct of Water Splitter.
  * Glykerol production (for DeepFreeze users).
  * KerbalHealth Lead Extractor.
* Added opt-in ISRU options (stock mode only, should already be provided by Kerbalism):
  * NFE Uraninite Harvester.
  * NFE Uraninite Enricher (converter).
* Fixed missing Kerbalism MRE Rock definition.
* Moved Kerbalism patches to their own mod folder to prevent their config nodes loading when they need not (when Kerbalism not installed). Due to how Kerbalism operates, configs are parsed before MM runs, making MM conditions irrelevant, and which is the cause of RR processes involving Metal and MetalOre to cause cascade problems because these resources' definitions Kerbin't gotten to load at the time the processes are parsed.
* Updated Extras:
  * RR_ScienceLabBlacksmith.cfg: Blacksmith is now its own modlet `RationalResourcesBlacksmith` so it can be targeted by patches or used as a dependency. Its converters are SystemHeat compatible.
* Updated Water Splitter to produce proper amounts of H2 and O2 gas (was broken and would produce 20%) and to produce Deuterium (gas).

## 1.14.1
* Added Spodumene Splitter ISRU. Its primary output is Lithium, used by Near Future engines.
* Added Spodumene-related B9 tank options.
* Added Spodumene presence to planets. Most abundant in vulcan and metal worlds and warm mud and lava oceans.
* Changed some engines to be inoperable when submerged.
* Rewrite converter options/configs to use Kerbalism side profile system.
* Rewrite ISRU mod integration system, create opt-in system to more easily integrate other ISRU mods.
* Updated Extras:
  * RR_NuclearFamily.cfg to handle bimodal rockets and assume their secondary mode, if present, is Lox-Augmented.
  * RR_NuclearFamily.cfg to handle nuclear jets and give them characteristics like the example "Maine Coon" NTJ.
  * RR_NuclearFamily.cfg to handle Restock+ Cherenkov and the Space Tux/Atomic Age engines by default.
  * RR_NuclearFamily.cfg to to add Kerbalism radioactivity.
  * RR_SSPXr_ContainerTypes.cfg to not activate when WBI Classic Stock active.

## 1.13.0
* Added Antimatter presence to gas giant templates.
* Added LqdDeuterium presence to ice atmospheres.
* Added templates associated with Event Horizon: **WormHole**.
* Added templates associated with Galaxies Unbound: **AtmOxygen** (not for gas giants), **AtmGasHelium, BlackHole, StarNeutron, StarCarbon, StarDyingRedGiant**.
* Added templates for LOX oceans: **OcnOxygen** (pure), **OcnOxygenC** (with CO2 and various traces), **OcnOxygenN** (with Nitrogen).

## 1.12.0
* Added cold gas RCS thrusters with 9 RCS modes (including MonoPropellant).
* Added patch for Hydrolox and Methalox to stock vernier LFO RCS. (Is not an extra.)
* Added Extras:
  * RR_ColdGasRCSStock.cfg to add all cold gas options to all stock and Restock+ MonoPropellant RCS.
  * RR_NuclearFamily.cfg causes Reducing Agent and Oxidating Agent versions to appear for compatible NTRs. Simply tag such engines that you like. Insutructions in config. Can run stand-alone.
* Added support for these in WBI Classic Stock.
* Added support for GEP (Grannus Expansion Pack). Includes experiment blurbs. This may change later-on and upset landed mining vessels, with new templates that may come.
* Added support for Grounded - Modular Vehicles.
* Added template: **AtmGasIV** for use by some Hot Jool type planets. Produced by forum user: **@ Clamp-O-Tron**.
* Added variant select for RR Ocean Scoop. Choose between: white + brown; all white.
* Added engines: 
  * MAPT "Microwave Air Plasma Thruster" built on stock J-20 Juno.
  * SFRJ "SolidFuel Ramjet" built on stock RT-10 Hammer SRB.
* Renamed engines: water ion and hybrid SRBs. May break craft.
* Updated Extras:
  * RR_TankswitchForSquad.cfg to not activate when Modular Fuel Tanks installed.

## 1.11.0
* Added Extras:
  * RR_TACLS.cfg changes TAC Life Support: To use the proper resources (Hydrogen, Methane, Carbon) and cease abstracting them with Waste in its converters; Its Air Filter becomes an all purpose atmo harvester; affect TAC patches for Airline Kuisine and Station Parts Redux.
  * RR_TACLS_AirlineKuisine.cfg to similarly affect Airline Kuisine's Mk2 and Mk3 converters.
  * RR_TACLS_SSPXr.cfg to similarly affect Nertea's station parts.
* Added LqdNitrogen propellant option to Reducing agent NERVA clone.
* Added missing Rock extraction options to RR exoscoop and for Kerbalism.
* Added support for Deep Sky Core intakes.

## 1.10.0
* Classic Stock focus
  * Added support for CryoTanks.
  * Added options for stock fuel cells.
  * Disabled most tank types for fuel tanks as they are mostly not fuels, and enabled Ore tanks to hold them all.
  * Fixed resources for RR atomic engines.
  * Fixed removal of stock converter modules for Boxed Convert-O-Trons (where OmniConverter modules are added).

* Fixed Configurable Containers detection.
* Updated Extras:
  * RR_TankswitchForSquad.cfg to stop detecting CryoTanks. This is handled elsewhere.

## 1.9.0
* Added RareMetals B9 tank option to Ore tanks.
* Added stock/Restock Ore tanks to RR category.
* Added Extras:
  * RR_MoreTankSwitches.cfg adds tank options for tanks of various manufacturers/mods including Fuel Tanks Plus, USI, Mk2 & Mk3 Expansion, KNES, Munar Industries, Charyol, DaMichael's, NovaPunch, NF Launch Vehicles... (List not made by me, contributed by @ Iodyne on the forum.)
  * RR_NTRReactorPatch.cfg adds the reactor engine functionality (demonstrated in the Main Coon jet engine) to the RR NERVA clones.
  * RR_KCTFuelResources.cfg registers RR eccentric propellants with Kerbal Construction Time.
  * RR_KerbalismEmitters.cfg adds Kerbalism radioactivity to the RR NERVA engines.
* Updated Extras/RR_EveLiquidFuelOcean.cfg to add LiquidFuel harvesting to the RR Hydroscoop, not the stock air scoop.
*This update brought to you by Iodyne! A little is plenty, plenty is deadly! but it's super rare and valuable!*

## 1.8.3
* Fixed Alumina issue (shortage) on specific stock body templates. (Mun, Minmus, Eve, Duna).

## 1.8.2
* Fixed a small issue with CCK config.
* Fixed some issues with stock tanks patch. (Didn't catch LF-only and Mono-only tanks when CryoTanks installed; Was not providing Methane and Methalox in some places it should.)
* Updated patch to not provide MonoPropellant to CryoTanks.

## 1.8.1
* Fixed some Kerbalism issues that sprung up.

## 1.8.0
* Added Community Category Kit (thanks to @Iodyne on forum).
* Added feature patches (where applicable) and stock subcategories akin to CCK for the following mods:
  * CryoTanks.
  * Far Future Tech.
  * Stockalike Mining Expansion.
  * WBI Airships (its Convert-O-Tron).
  * WBI Buffalo (its drill and Convert-O-Tron).
  * WBI Pathfinder (Arcology drilling rig, Castillo Factory, and the Lasso series harvesters).
* Added Water option for fuselage fuel tanks (for use with the Water NTR and Water ion engine).
* Added WBI OmniConverter modules.
* Balance pass on harvesters cloned from stock parts. They cost more, may weigh more, some may perform less than before.
* Fixed Configurable Containers detection in squad tanks patch.
* Fixed missing Kerbalism drills config.
* Fixed shroud style selection on NERVA clones.
* Replaced Extras/TankswitchExtras.txt with Extras/RR_TankswitchFusionFuel.cfg for increased use of the common ground between Far Future Tech and Galaxies Unbound.

## 1.7.0
* Added RR Hydro Scoop part for dedicated and more befitting ocean harvester. Related modules no longer populate the XM-G50 intake.
* Added RR Boxed Decompressor (red ZZZ box) for thawing/heating resources and reversing the processes of the RR Boxed Compressor/Freezer.
* Kerbalism integration:
  * Added Alumina, CarbonDioxide, Hydrates, MetalOre, Monazite to crustal drills.
  * Added LqdDeuterium, LqdMethane (and changed Ammonia to LqdAmmonia; Nitrogen to LqdNitrogen) to ocean drills.
  * Added all harvester options of the Kerbalism ocean drills to RR Hydro Scoop.
  * Added [Alumina, Hydrates, Monazite] Splitters to Convert-O-Trons. These don't seem to be fully functional yet. Will add remaining RR converter setps but this issue waits to be sorted out.
  * Changed Boxed Convert-O-Trons to always populate with stock method resource converter modules and to respect Kerbalism's interpretation of LF and OX (and adjust these fundamental options accordingly).
  * Changed: Stock Convert-O-Trons will not be populated with RR's extraneous converter modules. This cannot be done properly with creating and maintaining a new Kerbalism profile and KerbalismConfig package.
  * Enabled stock XM-G50 intake to use Kerbalism for atmo harvesting.
  * Enabled RR Exo Scoop to use Kerbalism for space harvesting.
* Updated units per volume in Classic Stock B9 tank types: Propellium, PropLox.

## 1.6.0
* Added templates: **AtmVulcan, SrfVulcan, OcnMudCold, OcnMudWarm**.
* Added support for Extrasolar (planet pack).

## 1.5.0
* Added calculator for engine propellant flow. (Not in download.)
* Added calculators for ISRU (in kilos and in molar masses). (Not in download.)
* Added hybrid SRMs (clones of the Flea and Hammer).
* Added LqdDeuterium presence.
* Added Water MET (Microwave ElectroThermal Thruster, clone of Dawn ion engine).
* Allowed scoop patches to run when KSPI installed.
* Updated Alumina Splitter and Ore tank types concerning their needs.
* Updated Hydrates Splitter outputs more, thanks to @ Muetdhiver on forum.
* Updated other conversion chains using newly available calaculators.

## 1.4.1
* Fixed a big error with the NEEDS in the Beyond Home config.

## 1.4.0
* Added `RationalResourcesAU` pseudo-mod for planet packs that rename or purge the stock planets.
* Added some resources to ground scanner.
* Added support (resource distributions and science) for Beyond Home (planet pack).
* Added templates for gas giants (Sudarsky class II, III) and lava oceans.
  * Updated sky and sea scanners accordingly.
* Fixed Hydrolox converter outputs (huge waste of Water).
* Fixed Xenon, Argon outputs in Hydrates Splitter (way too high).
* Nerfed Oxygen presence in Mun, buffed Alumina presence.
* Updated mine-able exo resources for AtmceWaterThick template.

## 1.3.1
* Fixed resource definition issue with SimpleConstruction.

## 1.3.0
* Added converters: 
  * Carbon Extractor
  * CO2 Fuser
* Added detection of Configurable Containers (stops the Ore tank B9PS problem for some players).
* Enabled "dump excess" on outputs of other converters (namely: Hydrates Splitter)

## 1.2.0
* Added missing Water splitter.
* Added Kerosene (LH2 + Carbon --> LiquidFuel) converter.
* Fixed missing outputs in Hydrates Splitter.
* Fixed Alumina and Monazite drills consuming 5x ElectricCharge for their 5x efficiency.
* Made Carbon output available in CO2 splitter.
* Made Blacksmith patch only activate if RR Parts is installed.
* Moved Carbon and CarbonDioxide tank types to be immediately beside each other for Ore tanks.
* Renamed and rearranged some converters.

## 1.1.0
* Added input fuel switch to fuel cells. (Not available for Classic Stock due to OmniConverters.)
  * LFO, Hydrolox, Methalox for stock.
  * MonoProp, Ammonia for Restock+ APU.
* Added Silica surface template.
* Added splitter (converter) for Alumina and Monazite.
* Added B9 tanks types for Alumina, Carbon, Monazite, Phosphorus (visible to Ore tanks).
* Added CryoTanks detection for fuel cell patch.
* Added Kerbalism detection (Do not activate patches for drills, converters, fuel cells if Kerbalism is installed). WIP config exists to add ISRU chains to Kerbalism processes.
* Added Phosphorus resource. Phosphorus is a vital element in life as we know it, but is incredibly hard to come by and will be priceless in generation ships. Fairly rewarding to produce for funds.
* Added resource distributions: Alumina and Monazite.
  * Their max abundances are heavily nerfed to fit this mod's pie charts for resource compositions.
  * Their harvesters in the stock drills have been buffed to compensate.
* Fixed variants in Restocked cloned bread tanks.
* Removed support for Karbonite and Karborundum as they are handwavium and not rational.
* Stopped purging KSPI resources. They should coexist now and should appear in SCANsat's resource overlay selection.
* Updated **Extras/** configs:
  * Added "Blacksmith" facility for refilling non-transferable resources. Introduces pseudo EVA work resource. Has upgrades. Converter inputs switchable.
  * RR Blacksmith currently caters to heatshields' Ablator and SRBs for SolidFuel.
  * Disabled LqdHe3 tank type as it upset some players.
* Updated Ore tank types (certain heavy resources have reduced capacity due to their mass differences being an order of magnitude apart for other resources).

## 1.0.3
* Added Restock+ new Ore tanks (KSP 1.8) to Ore tank resource switching.
* Fixed missing Water in Duna and Laythe polar regions without JNSQ.
* Fixed specific restrictions at Mun Polar Crater without JNSQ.
* Fixed missing NEEDS in OPM patch.

## 1.0.2
* Updated SSPXr extras config. Caught redundant/overlapping subtypes.
* Added WBI logistics module to all stock parts when TankSwitchForSquad patch is active and Rational Resources is in Classic Stock play mode.
* Tiny adjustments to nuclear engines.

## 1.0.1
* Moved B9 tank definitions to core folder to prevent breakage of established mods containing RR tank type patches.

## 1.0
* Split all added parts and active stock part modifications (except the experiment and the scanners) into their own mod, `RationalResourcesParts`. This allows RR itself to be a resource placement mod and absolutely nothing more, for those who want to bundle it or those who just don't want parts.
* Added nuclear engines:
  * "Panther" clone "Main Coon" nuclear turbojet with built-in nuclear reactor.
  * "NERVA" clones. The "O" edition is high thrust and can choose between Carbon Dioxide and Water. The "R" edition is high Isp and can choose between Hydrogen, Ammonia and Methane. Their mode switch feature requires **B9 Part Switch 2.10** or later.
* Added/Updated LqdHe3 presence via ExoRock, ExoIce, Mun templates.
* Added LqdHe3 to RR Ground Scanner.
* Added Water to Duna.
* Reduced MetalOre tank volume. A full tank weighed far, far too much.
* WBI Classic Stock:
  * Changed nuclear engines to use Classic Stock resources.
  * Added OmniConverters for cycling Atmosphere and CompressedAtmosphere.
  * Provided tank types. Most of Pathfinder's tank types available to all stock tanks through the Extras config.
* Fixed small error in OPM science config.
* Fixed XM-G50 intake patch to use harvester modules for ocean filtering. Intake modules showed very undesired behavior.
* Changes concerning Eve oceans and Kerosene/LiquidFuel:
  * Added large Ore presence to Eve Shallows biome to compensate for a lack of proper heavy hydrocarbon resource outside of RealFuels.
  * Added **Extras**: RR_EveLiquidFuelOcean.cfg -- what it says on the tin. Also adds a LiquidFuel harvester module to the XM-G50 air scoop. The idea of this is both very necessary on one hand and very silly on the other hand so it will not be active by default and will not be endorsed for use elsewhere.
  * Removed CRP LqdMethane from Eve oceans as this is cryogenic and should not exist at a hot inner planet. It will still appear at any decent world with hydrocarbon oceans-- cold outer worlds.
  * Classic Stock Hydrokerbon presence is unchanged as it meets the mark.


## 0.9.1
* Added support for the Outer Planets Mod.
* Added Extras folder with optional configs.
  * Moved stock Ore converters remover here.
  * Added `RationalResourcesSquad`. This extra applies B9PS and all fuel options to all stock tanks. This also adds non-redundant tank types to CryoTanks if that is installed. (Does not affect CryoTanks if installed alongside WBI Classic Stock.)
  * Added patch for Nertea's SSPXr.
  * Added LqdHe3 tank type which only appears for Galaxies Unbound (a planet pack).
  

## 0.9.0
* Added atmo edge distributions for Default and Terra templates.
* Added ExoRock and ExoIce templates for airless worlds.
* Added Hexagen to Mun crust (Helium presence for CRP pending).
* Added MetallicOre presence.
* Added MetalOre and Oxium to scanners for Classic Stock.
* Added Ore tank types for SimpleConstruction.
* Added Planet Classification experiment.
  * Added to stock M4435 Narrow-Band Scanner.
  * Supports JNSQ.
* Added several stock scanner modules to RR Scanners:
  * GPS to all.
  * KerbNet to all.
  * Biome scanner to ground and sea.
  * Asteroid analysis to ground.
  * (Per) Resource Analysis via CRP, Classic Stock (I might revert this one. Possible PAW spam.)
* Added temporary clones of the stock 'Bread' tanks with B9PS and Tweakscale patch. These can hold all RR tank types. Better tank models and sizes coming.
* Changed Ore tanks patch to only target stock Ore tanks.
  * Added Hydrates, Rock options.
* Fixed distributions settings for worlds changed by JNSQ.
* Fixed gas giant Hydrogen, Helium presence.
* Fixed mini drill abundance threshold, leave it unchanged.
* Finish balancing ISRU chains.
* Removed CO2 multimode patch for stock NERV engine. It was found to conflict with the Kerbal Atomics multimode patch. This patch may return as an example for making other CO2 NTR configs.
* Treated stock Oxidizer as LqdOxygen, remove LqdOxygen -> Oxidizer option. Due to balancing reasons, these two have a redundancy problem.
* Treated LiquidFuel as Dodecane.

## 0.8.6
* Added CarbonDioxide and Hydrates splitters to ISRU.
  * These and other ISRU chains pending balance pass.
* Added Star exo band templates (Population 1 ~ 3) with decreasing amounts of most things but Hydrogen and Helium.
* Added Water to Mun and Minmus polar biomes.
* Added MetalOre to stock Drill-O-Matics.
* Added small MetalOre presence to Minmus to help with base-building.
* Change SimpleConstruction ISRU to consume MetalOre.
* Fixed Ore tank patch to only active if CRP present.
* Fixed intake harvester patch to only active if CRP present.
* Enabled several non-MKS resources to appear in SCANsat resource overlay selection.

## 0.8.5
* Added parts:
  * ZZZ box Convert-O-Trons (will hold OmniConverters in Classic Stock mode). These are temporary parts and not to be used on permanent or long-term crafts. They are for testing the ISRU chains.
  * HECS-shaped resource scanners for: Surface; Sky (Atmo+Exo); Ocean.
  * Exo scoop. Supports Antimatter, karborundum, LqdHe3, Hydrogen, LqdDeuterium.
* Added features:
  * Atmosphere harvester and splashed-only intake modules to the stock XM-G50 radial intake.
  * Resource options to the stock Drill-O-Matics.
  * Mini Convert-O-Tron and Drill-O-Matic are no longer borderline unplayable. They are as terrible as they are on purpose and some of us don't like that.  
  * LqdCO2 secondary mode for stock NERV. Requires ReStock.
  * Atmo/exo harvester modules will not appear if KSPI is installed.
* No longer add resource scanners to stock parts (the ones that will still appear in the Surface Scanner are those added by CRP, not this mod).
* Added Easy Mode `RationalResourcesEasy` pseudo-mod. This prevents deletion of the stock fuel options in the Convert-O-Trons and causes Ore to not be nerfed as harshly. Ore remains available everywhere but will not pass 8% max (vs the default 15%).
* Added `RationalResourcesOverride` pseudo-mod. This provides for planet mods that change Kerbin and Sun and will want alternate resource templates for them.
* Buffed Minerite/Mineral abundance in Duna. Reduced RareMetal abundance in exchange.
* Changed all LqdHydrogen presence to Hydrogen and tuned abundances and ranges.
* Added yellow star atmo template (only provides exo resources).

"Pseudo-mods" in this context are mods whose purpose are only to activate extra patches. to activate a pseudo-mod, create a folder with its name in GameData or create a patch with a `:FOR[]` targeting the pseudo-mod.

## 0.8
* Pre-release
* CRP supported
* Classic Stock supported
* No ISRU configs
