# Rational Resources Plasma Family
This addition within Nuclear Family provides for any engine type involved with plasma, therefore, several types such as Ion, Fusion and Antimatter.

## Fusion
Engines opted in for RR Fusion can choose between Magnetic Confinement (will ask for Deuterium + Helium3) or Inertial Confinement (will ask for FusionPellets) and gain a B9 selector for the ratio of additional Hydrogen or Water (the afterburner resource) inspired by the concept of gear-shifting as listed on [Atomic Rockets](https://www.projectrho.com/public_html/rocket/engines.php#id--Shifting_Gears). Dual-mode fusion engine parts are highly preferred as this means the secondary mode can be set to a higher gear or less higher gear with full convenience vs the edge case where a player, using a single mode engine, may feel the need to switch gears mid-burn, especially during a suicide burn.

Gear-shifting allows the player to choose their optimal afterburner ratio and exchange high Isp for high thrust. For System Heat users, waste heat production also goes down with Isp. The following screenshots show the exchange of thrust, Isp, required fusion fuel, required afterburner resource and waste heat produced while wet mass and delta-V don't change much.
![1st gear](https://i.imgur.com/RPogN0L.png)
![5th gear](https://i.imgur.com/8XZYLJF.png)

Nearly any orbital slow-boat should become a capable lander with this kind of functionality. Strong suggestion: Let's not apply this to -every- fusion engine, namely any early tech ones. Also, other sorts of fusion engine tech such as Magneto-Inertial or Magnetized Target are not compatible with gear-shifting.


### Nerd Stuff
Idealized ratios (namely for Hydrogen) of afterburner resource to fusion fuel by gear. Reference engine spec is 350 kN @ 35000 sec for 1 kg/sec of fusion fuel resource consumption. These ratios may be subject to change later.

| Gear | Afterburn (kg/sec) | Hydrogen (ratio) | Water (ratio) |
| -- | -- | -- | -- |
| 1 | 0 | 0 | 0 |
| 2 | 1.1086 | 3.38 | 0.239 |
| 3 | 2.95208 | 9 | 0.638 |
| 4 | 5.53024 | 16.86 | 1.195 |
| 5 | 8.85625 | 27 | 1.914 |
| 6 | 12.9236 | 39.4 | 2.791 |
| 7 | 17.7125 | 54 | 3.825 |
| 8 | 23.2559 | 70.9 | 5.022 |