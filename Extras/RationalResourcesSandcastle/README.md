# Rational Resources Sandcastle
This modlet causes parts to have some level of complexity to their WBI Sandcastle print requirements. The resources involved:

## Existing Resources
**Minerals**. This resource is less generic than Ore but is functionally the same. It is similarly wastefully used because it largely consists of several things we want and several thing we don't. This resource alone is used because we cannot assume that all parts are made with metal and that many parts may be made mainly of stone, glass or plastic.

**Metals, RareMetals**. These appear according to some of the part categories where all things there are presumed to be created with some amount of Metal.

**ExoticMinerals, Organics**. These appear according to some tech nodes in CTT, mainly the entire fission and fusion region, most of ion/plasma propulsion and hydroponics. **Organics** may be replaced. It represents the soil used within any greenhouse part.

> :warning: Parts that are made near-entirely of something specific, such as glass for glass parts, should include a `PRINT_RESOURCE{}` config node which declares Minerals and reduces its amount to nearly zero. Not doing this will cause the part to still require a lot of Minerals, but doing this and setting zero will make the part non-printable. As explained by @ProgrammerFailure, the printer won't eat the resource but it will also stall.

## Introduced Resources
The following resources represent functional components found in anything that would produce or respond to a control signal. In concept they are equivalent to themore abstract **Equipment** resource found in WBI, or to the less abstract SpecializedParts or Machinery in USI. We will not attempt to match the level of complexity of USI's fabrication resources (having Polymers, Synthetics and so on) otherwise we'd just use USI and not be here.

- **Actuators**: These represent any moving parts at all and their lubrication (when relevant). Not all parts are digital so not every part that requires actuators will also require electronics.
- **Electronics**: These represent all bits that interact with photons, electrons and magnetism and are made with common metals.
- **Microprocessors**: These represent anything that produces a control signal and can mind its own operations or the operations of other parts. They are made with some amount of rare metals.

