# Simplified Real Fuels

A mod pack for Kerbal Space Program.

Simplified Real Fuels (SRF) is an attempt to add many "realistic" features to KSP, in the same time trying to maintain some balance between realism and playability. SRF is balanced for Rescale x6.4 *only*. It's not intended to be used in stock or realistic (RSS) scale.
There are configs for Sigma Dimensions in Extras/RESCALE folder for your convenience. **JNSQ is supported**.

## Features

* **Real-world fuels**
  * LFO engines now use several variants of fuel/oxidizer pairs, which include KeroLOX, HydroLOX, hypergolic pairs like UDMH/NTO and some others.
  * Monopropellant engines use Hydrazine instead of Monopropellant.
  * Air-breathing jet and turboprop engines burn Kerosene, piston engines (like those from AirplanesPlus mod) use AvGas. There are also variants for stock jet engines, burning Lqd. Methane, LH2 and Methanol.
  * Nuclear engines use LH2 or Lqd. Methane as reaction mass, some engines from Kerbal Atomics has additional LOX-augmented (HydroLOX) mode.
  * Electric engines (ion, plasma) mostly left intact, and use their respective propellants: Xenon, Argon, Lithium. Expception is Pulsed Inductive Thrusters from NFPropulsion mod, they have been switched to Liquid Ammonia. Low tech electric engines (arcjet and resistojet from RLA) use Hydrazine.
  * Solid fuel booster also have been switched to real solid fuels (like HTPB or PBAN), however, this is mostly cosmetic feature.
  * RCS thrusters now comes in 3 tiers: helium cold-gas thrusters, monopropellant (hydrazine) and bipropellant thrusters (few fuel/oxidizer options available). Kerbonauts' RCS jet packs use helium.
* **Pressure-fed engines**  
Some engines have no fuel pumps and require fuel/oxidizer to be "pushed" to them from fuel tanks. These mostly are low-thrust orbital hypergolic engines. They are simple, and typically have high rated operation time and ignitions count. The downside is pressure-fed engines require special highly-pressurized fuel tanks, which are much heavier than ordinary fuel tank for pump-fed engines. All RCS thrusters are, in fact, miniature pressure-fed engines, so all RCS thrusters now require proper high-pressurized tanks to function.
* **Fuel tanks rebalance**  
Fuel tanks now have realistic dry masses. Default (standard garden variety) and highly-pressurized tanks are divided into 4 tech levels. Higher tech level tanks have better dry mass and volume utilization (97% volume for tech IV vs 88% volume for tech I tank), but are more expensive. There are also special tanks types:
  * Balloon - very light, but fragile tanks. In real life balloon tanks must be kept pressurized at all times. In KSP, these tanks have very low crash tolerance, low max temp and high price. Volume utilization: 100%.
  * Cryogenic tank - same as balloon tanks, but not so fragile, and with thermal insulation. Used for long-term storage of cryogenic fluids, such as Lqd. Hydrogen. Volume utilization: 99%. Most expensive fuel tank type.
  * Fuselage - heavy tanks with thermal protection. Have high max temp value. Volume utilization: 92%. Intended for spaceplanes and other reentry-capable spacecrafts.
All fuels tanks in game now have tank type switch. Available options depends of technological level of tank and some other part parameters. For example, you can use the same good old Jumbo tank for your KeroLOX first stage, and for HydroLOX upper stage, by simply switching fuel tank type.
* **Engines thrust and ISP rebalance**  
Most liquid fuel engines have about one third of their real-life counterparts' thrust, and same (i.e. realistic) ISP. However, engines patches are individual and in many cases their thrust is set higher for balance reasons (this is especially true for upper stage engines). Engines masses also have been tweaked, and most of engines now have TWR in range of 40 to 55.
* **Vast technology tree**  
Mod comes this it's own technology tree, counting more than 200 tech nodes with total cost of 160 000 science points. Tree has some resemblance to RP-0 tech tree, but not tied to any specific dates (no techs like "1970-1971 Orbital Rocketry"). Some effort have been made to make transitions from one tech to another as logical as possible. Some comments on tree:
  * If some tech node has more than one dependency (preceding techs), they all must be researched prior to this node.
  * Starting node give player nothing but one Thermometer part. So, then you start new career, it's strongly recommended to give yourself some starting scince points (25 should be enough). Otherwise you will not be able to make any progress pass starting tech node.
  * As tech tree is *huge*, you'll definitely need some more science details/experiments, for **moar science**. I suggest DMagic Orbital Science, Coatl Aerospace, Bluedog DB and ScanSat mods.
  * SRF is still work in progress, and all parts, which were not specifically allocated to tech tree node, will be placed in "Orphans" (just below start node). If you can't find you part, try searching where.
* **Various parts mass rebalance**
  * SRBs have 20% reduction of dry mass, some of them received individual tuning. SRBs minimum thrust (configured in hangar) is now 25% of it's max thrust.
  * Crewed parts are also 20% lighter now. The same is true for all solar panels.
  * Some more parts mass tuning - reduction of mass for heat shields, some structural parts, etc.
* **Better parts naming**  
Stackable parts has their titles prepended with part's size (bulkhead profile), for example: "2.5m Rockomax Jumbo-64 Fuel Tank". The same is true for engines, but their titles contain more information: "2.5m KeroLOX Lower Stage RE-M3 "Mainsail" Liquid Engine". This way parts are better sorted in categories and more easily found by player. Filter Extensions configs are on the way.
* **Prices rebalance**  
Most parts prices are left intact, but fuels and oxidizers prices are set realistically low. In early game, you can easily find yourself launching small rocket with zero fuel cost. Like in real life, fuel/oxidizer cost is just a small fraction of launch expenses. Prices of propellants for electric or other high-tech engines (Xenon, Lithium, etc.) are left intact.
* **Kerbalism integration**  
SRF includes custom profile for Kerbalism. It features:
  * Kerbals consume 4 times more food and water, than with Default profile. Oddly enough, oxygen consumption is already okay in Kerbalism (set to 1/4 of human's).
  * Realistic resources for all Kerbalism chemical processes. This includes full support for RealISRU mod, giving player many processes and parts for ISRU purposes.
  * More scrubber types, tied to different technologies. Regenerative scrubbers are relatively far in tech tree.
  * Several types of fuel cells to choose from (available as variants for each fuel cell part): hydrazine + O2, H2 + O2, methanol + O2, LH2 + LOX, ...
  * Four variants for RTGs (available as radioactive material selection for each RTG part, tied to tech tree). Each of them has pros and cons.
  * A little hack to make NFElectrics and FarFuture reactors to generate heat (sadly, Kerbalism disables heat generation). Basically, each reactor now has two different generators:
    1. Default, which is reactor from mod, giving full power and generating much heat - use it to power your hungry plasma engines, do not use it in warp.
    2. Kerbalism's generator, giving only 1/10 of main reactor power, but generating no heat at all. Use this one in warp to power your ship in background (life support, communications, science, etc).
  * Support for some unsupported mods (like Coatl Aerospace).
  * Avionics probe cores. Kerbalism adds hard drive module and configurable unmanned experiments to all probe cores (unmanned control modules) by default. SRF removes those unneeded stuff from probes, marked as "Avionics". Specifically, these are all round probes, like stock "RC-001S Remote Guidance Unit" or 5 m diameter probe core from NF Launch Vehicles mod. Instead, avionics cores receive decent amount of electric charge.
* **TweakScale support**  
Fuel tanks, solar panels can be scaled only from 66% to 150% of their original size. Engines and crewed parts can not be tweakscaled at all, the only exception is pressure-fed engines.
* **Procedural tanks**  
Procedural tanks of each type are available. Default and high-pressurized tanks have 4 tiers, tied to appropriate tech tree nodes. Dry masses are on par with similar non-procedural tanks.
* **4 tech levels of batteries**  
From early Silver-Zinc (which are *worse* than stock batteries in almost every aspect) to modern Li-Ion, which holds 2.5 times more electric charge for the same size, but are quite expensive.
* **Bunch of other tweaks and patches here and where**

## Main differences from RealFuels/RealismOverhaul

* **Universal fuel/oxidizer rates for all specific fuel/oxidizer pairs**  
If two different engines burn, let's say,  Kerosene and Lqd. Oxygen (i.e. are KeroLOX engines), they always burn it in same proportion, disregard of technological differences. It might seem unrealistic (it is, actually), however, fuel/oxidizer ratios for different real-world engines do not differ more than for few percent. SRF implements some "average" ratios for HydroLOX, KeroLOX, etc.
* **No ullage simulation**  
Engines ignitions are handled via Kerbalism mod, which has no ullage simulation implemented.
* **Many engines still have ability to throttle down to 0%**  
For player's convenience, many vacuum-rated engines can be throttled down to zero (i.e. stock behavior). Such engines have "Service" keyword in their title. These are mostly low-power pressure-fed engines, and some high-tech engines: nuclear, electric, etc.  
Lower stage engines (and many upper stage engines), however, can not be throttled down to zero (if at all), and generally have very limited ignitions count.

## Dependencies

These components are absolutely required for the mod to function. They must be downloaded separately:
* [ModuleManager](https://github.com/sarbian/ModuleManager) (preferably last version)
* [CommunityResourcePack](https://github.com/BobPalmer/CommunityResourcePack) (preferably last version)
* [B9PartSwitch](https://github.com/blowfishpro/B9PartSwitch) (recommended 2.14.0 or higher)

## Highly recommended mods
* [Sigma Dimensions](https://github.com/Sigma88/Sigma-Dimensions)  
For RESCALE. SRF is balanced only for x6.4 scaled system, you have been warned.
* [Kerbalism](https://github.com/Kerbalism/Kerbalism)  
Many SRF features (like engines ignitions/reliability, life support, ISRU processes) are actually Kerbalism features and will not work without it.
To use SRFProfile in Kerbalism, change "Profile" setting in GameData/KerbalismConfig/Settings.cfg file:
    > Profile = SRFKerbalism

* [Procedural Parts](https://github.com/jrodrigv/ProceduralParts)  
It's much easier to build a rocket, if you can set fuel tank size and shape for exactly those you need.
* [Cryo Engines](https://github.com/ChrisAdderley/CryoEngines)  
HydroLOX engines for different applications, cryo tanks for long-lasting deep space missions.
* [Near Future Launch Vehicles](https://github.com/ChrisAdderley/NearFutureLaunchVehicles)  
MethaLOX engines for launch vehicles, huge fuel tanks, adapters and more parts for really large rockets.
* [Real Engines Pack](https://spacedock.info/mod/1212/RealEngines)  
Many high-quality (mostly soviet) rocket engines.
* [Bluedog DB](https://github.com/CobaltWolf/Bluedog-Design-Bureau)  
Enormous mod with large amount of high-quality parts to replicate US space program from early Vanguard through Saturns and Titans to Deltas and Atlas V. Highly recommended, although not fully supported yet.
* [Taerobee](https://github.com/Tantares/Taerobee)  
Early AlcoLOX engines and parts to build V-2 rocket.
* [Near Future Propulsion](https://github.com/ChrisAdderley/NearFuturePropulsion)  
Very efficient ion and plasma engines for long-range interplanetary missions.

## Recommended mods
* [Kerbal Construction Time](https://github.com/linuxgurugamer/KCT)  
Vessels construction, KCT upgrades, tech nodes research and some over things now take time to complete.
* [KRASH](https://github.com/linuxgurugamer/KRASH)  
Simulation of craft launches. Must have, if you use KCT.
* [Monthly Budgets](https://github.com/severedsolo/MonthlyBudgets)  
Player receive some budget each month, depending on reputation. Works pretty good with KCT.
* [JNSQ](https://github.com/Galileo88/JNSQ)  
Planetpack of astonishing quality. JNSQ already implements x2.7 rescale, SRF has Rescale configs to make resulting scale x6.4 compared to stock.
* [Outer Planets Mod](https://github.com/Poodmund/Outer-Planets-Mod)  
Adds three outer planets (gas giants) with a large amount of moons. Not compatible with JNSQ, choose one or ahother.
* [Extrasolar](https://spacedock.info/mod/202/Extrasolar:%20Planets%20Beyond%20Kerbol)  
For then you decide to go interstellar. This mod adds small red dwarf star - Valentina - at distant orbit around Kerbol.
* [Far Future Technologies](https://github.com/ChrisAdderley/FarFutureTechnologies)  
Engines and other highly advanced techs to actually get you to another stars. SRF has many tech nodes in research tree specifically for Far Future Tech.
* Basically every Nertea's mod, not limited to already listed. They all are great, really.
* [DeepFreeze](https://github.com/JPLRepo/DeepFreeze)  
Provides the ability to freeze and thaw kerbals for those long space journeys. SRF integrates DeepFreeze with Kerbalism: only DeepFreeze modules now have the ability to cure kerbonauts radiation level, consuming Glykerol in process. Freezers are placed far in tech tree and intended to be and end-game technology.
* [Universal Storage II](https://spacedock.info/mod/1933/Universal%20Storage%20II)  
Set of high-quality parts for service modules of your spacecrafts. SRF implements Kerbalism integration for many USII parts, for example, reconfiguring two of them as external life support system modules.
* [DMagic Orbital Science](https://github.com/DMagic1/Orbital-Science)  
Many, many new science parts and experiments. Integrates with Kerbalism and Universal Storage II. You will definitely need more science points to research huge SRF tech tree.
* [Coatl Aerospace ProbesPlus](https://github.com/raveloda/Coatl-Aerospace)  
Probe expansion pack, includes many science experiments, integrates with DMagic. While technically in development, this mod is full-featured and completely working.

## Incompatible or not recommended mods
* S.M.U.R.F.F. - should not be used together with SRF (although not tested). You probably do not want two mods patching your engines' thrust and tanks' mass at the same time.
* Real Fuels, Realism Overhaul - incompatible for obvious reasons. SRF do the similar things to tanks and engines, but in a different way.
* Modular Fuel Tanks - MFT is not compatible with SRF system for switching fuel tanks content, based on B9PartSwith.
* SSTU - mod use it's own system for switching fuel tanks contents and it's own set of fuels and fuel/oxidizer pairs, not compatible with SRF.
* Interstellar Extended - no support for this mod is present in SRF. It *might* work ok, but it's not integrated in any way in SRF tech tree.

## KSP version support
Simplified Real Fuels is a bunch of module manager configs, no DLLs, so it should work on any KSP version, which is supported by required mods. KSP 1.7.3 and 1.8.1 have been tested. SRF *does* work with Module Manager 3.

## Licensing
Simplified Real Fuels mod is distributed under a Creative Commons Attribution-NonCommercial 4.0 International License (https://creativecommons.org/licenses/by-nc-sa/4.0/).

You are free to share and adapt the materials only for non-commercial purposes and when providing appropriate attribution. Any derivatives must be distributed under the same license.

Simplified Real Fuels includes icons for it's tech tree, taken from:
* [Community Tech Tree](https://github.com/ChrisAdderley/CommunityTechTree)
* [Realistic Progression Zero/One](https://github.com/KSP-RO/RP-0)
Both mods are distributed under the same license (Creative Commons Attribution-NonCommercial 4.0 International License).
