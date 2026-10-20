# Approved decisions

Product decisions have stable IDs (`GTIA-D-NNN`) that are never reused. Only the pack author approves a decision; a proposal is not a decision because it appears in a document. Revoked decisions keep their ID and are marked as revoked.

This page lists the approved product decisions that shape development. Internal drafts, audits and studies are not published.

| ID | Decision |
| --- | --- |
| D-141 | Greenhouse and Pyrolyse Oven arrive early in MV. The Greenhouse is optional and starts sun-dependent; the Pyrolyse Oven is strongly recommended but does not gate HV. |
| D-221 | Vertical, generated quest book (`questgen.py`) with chapters per tier, fixed meaning for side lanes and shapes per role, and automatic checks. |
| D-226 | No research tree. The pack is about building and running megafactories. |
| D-227 | Megafactory in depth and width. In the first 20 hours, new machines every session. 1–2 rebuilds per tier. The factory goes wherever the player wants. |
| D-228 | Processing lines grow with the tier (Steam 2–3, LV/MV 4–6, HV/EV 6–10, IV+ 10+), with by-products, closed loops, waste treatment and branching mid-line. |
| D-229 | Real chemistry without requiring a PhD, in the order Steam wood/coal and lime → LV chlor-alkali and steel → LV/MV Bayer + Hall-Héroult → MV Contact, Haber-Bosch + Ostwald, Solvay → HV refining. |
| D-230 | Resources: wells with purity, infinite sources per tier, planetary gases, renewables as real routes, mobs only from the Slaughterhouse, rare elements only as by-products. |
| D-231 | Energy: real fuel lines, heat as a resource, chemical and thermal storage, losses on wireless energy. |
| D-232 | Logistics: no throughput limits, AE2 storage at the end of LV and autocrafting in MV, no Create. |
| D-233 | Multiblocks: upgrades by parts, Mega for everything, no limit, parallelism explained with numbers, modules through hatches and the GTNA module system, no luck-based progression. |
| D-234 | Danger: GTCEu explosions and hazards, cleanrooms, inert atmospheres, safety gear. |
| D-237 | Grind is solved with more factory. Own recipes for key items plus automatic shortcut checks. Modes chosen at world creation and locked. |
| D-238 | Chosen unique ideas: process conditions, two routes per molecule, closed loops, wells with purity, heat as a resource, factory dimension, planetary gases, rare elements only as by-products. |
| D-244 | Standard multiblock tooltips in the GTNA format: a real fact, then Main Function, Auxiliary Module and Running Requirements. |
| D-246 | Better versions of the real-chemistry multiblocks (rotary kiln, membrane cell…) come from IV/LuV onwards. |
| D-254, D-256 | GTIA Rules: Journey, Normal and Custom presets; 44 rules in 7 groups; rules never change registries. |
| D-257 | Crafting Chain (separate mod) replaces Fabricate. |
| D-259 | Bees arrive in HV through Productive Bees with its base recipes removed. |
| D-260 | Agronomica: our own crop mod, separate repository, LGPL-3.0. |
| D-261 | Ore boost with a reagent: 1 crushed + 1 leaf + reagent → 3 purified. |
| D-262 | GTIA Lib is the org's foundation library (depends on GTCEu); GTNA, GTIACore and Agronomica require it. GTOLib ideas are reimplemented from scratch, never copied. |
| D-263 | Ascension Optimizer (`ascopt`, no GT dependency): spawn chunks 441 → 25; server ready in 31 s instead of 47 s. |
| D-264 | Client uses ModernFix `dynamic_resources`; LeanObject is server-only (menu heap −37 %). |
| D-265 | EMI multiblock previews built on demand and GTNA shape cache in SoftReference: EMI reload 20.6 → 12.2 s, client runs with 1.5 GB. |
| D-266 | Draconium belongs to GTNA only; GTIACore's copy was removed. |
| D-267 | Agronomica core: crop sticks, four Steam/LV crops, Growth/Gain/Resistance (soft cap above 20), cross-breeding with mutations, NPK soil and fertilisers. |
| D-268 | HV bee line: all Productive Bees recipes and nests disabled; caged metal bees come from the Chemical Reactor, the Industrial Apiary (HV–UV) makes combs, combs give a small dust or, with HCl, purified ore. |
| D-269 | Recommended client flags: G1 periodic GC with free ratios 10–30 % and `MALLOC_ARENA_MAX=2`; client RSS 6.0 → 4.4 GB with the same live heap. |
| D-270 | No batched `@Synced` for now: a player next to 500 working LV furnaces receives about 1.3 KB/s; LDLib sync is not a network bottleneck. |
| D-275 | HV quest chapter v6 approved: every dependency has a recipe reason checked against a GTNH 2.9 / GTO 0.6 quest atlas; tier machines are side quests unless a goal needs them; the circuit ladder (HV → EV → IV) lives inside the tier; the EV circuit comes right after the Cleanroom because HV multiblocks need it. |
| D-276 | Start–MV quest chapters v7 in game, built like HV v6: recipe reason on every dependency, tier motor and turbine as central hubs, LV motor before the LV turbine, separate components, MV PVC board and CPU chip line, HV gets an HV steam turbine. Hidden lines use FTB's per-quest flags on either side; crossings and long lines are notes in `questgen check`. |
| D-277 | Rocket Assembler (HV): 15 × 15 × 20 launch complex (twin stepped service towers, scaffold, umbilicals, crane bridge, flame trench), own casing with LDLib connected textures; the tier 1 rocket and its Ad Astra parts are made through GT and Ad Astra's own recipes for them are dropped. |
| D-278 | Mode-only quests: GTIACore tags the player `gtia_journey` or `gtia_normal` from the world preset (Custom counts as Normal); a hidden `modes` chapter turns the tag into an FTB Quests stage, and quests marked with a mode stay hidden in the other one. The Start chapter's strong tool rewards become the Journey Starting Kit; Normal gets steel tools and an LV prospector. |
| D-279 | Organ system ported from GTO 0.6 into GTIACore: 9 organ types × tiers 0–4, steel/fairy/mechanical wings, Organ Modifier screen (9 organ + 8 wing slots), organs kept in persisted player data. Effects as in GTO (leg speed scaled to +10/30/60/100 %, +5 armor and toughness per set tier, +4 reach, liver and lung perks, no hunger at set 3, flight at set 4). Ad Astra planets hurt players below set tier (t−1)/2+1 (Moon and Mars: 1). GTO assembler recipes; phantom membranes replace Botania in the cheap wings. GTO's "nano wall" is left out (GTOLib only). |
| D-280 | GTIA Rules grow from 44 to 52 for parity with GTO Rules: rubber tree chance, infinite bedrock fluids, require GT tools (restart), material hazards, extra regeneration (food threshold and strength), planets need organs, organ cost. GTO rules without a GTIA mechanic stay out (see the table below). |
| D-281 | MV/HV chemistry lines: Ostwald Converter (MV, cobalt oxide gauze; HV platinum gauze), Claus Unit, Kroll Reactor and Siemens Reactor (HV), Czochralski boule from 16 polysilicon in the EBF. Real stoichiometry and closed loops (NO, Mg/Cl₂, HCl). |
| D-282 | Main menu with FancyMenu 3.9.12 (Konkrete, Melody) instead of PackMenu: animated emblem plus the author's text logo recoloured in purple, animated pixel-art space-factory background, buttons Singleplayer, Multiplayer, Mods, Settings, Quit and Discord. |
| D-283 | Quest book highlight images: isometric renders of 19 multiblocks from the real textures (`modpack/tools/iso_render.py`). The Moon quest is a dimension task and the reachability model knows Ad Astra's own Moon blocks, so no lunar quest is pending. |

### GTO Rules left out of GTIA Rules (D-280)

| GTO rule | Why |
| --- | --- |
| Recipe / mod recipe / ore processing difficulty, fluid resource difficulty, tech tree difficulty | GTO-specific recipe sets; GTIA has one recipe set per pack, tuned by the recipe rules |
| Scan duration, repeated scan factor, energy data hatch warm-up | No research tree (D-226) |
| Space elevator, ME hatch energy, ME simple pattern buffer, ME muffler amplifier, virtual coin | Machines that only exist in GTO |
| Generator array, wind turbine, magic generator, mega turbine, flow fuel cell, bio stimulation, wireless energy tower, lightning rod | Generators that only exist in GTO |
| Large steam circuit assembler, large solar boiler, large steam storage tank, dual chamber | Steam machines that only exist in GTO; GTIA's steam rules cover the GTNA steam multiblocks |
| Fluid pipe throughput, maintenance wear rate, random maintenance failures, configurable maintenance bounds, parallel hatch tier bonus, processing plant parallels, field generator amount, time twister, shut down on power loss, generators burn fuel when full, reset progress on low energy | No setting in GTCEu 7.5.3 to drive them |
| Tiered casings | Kept off in both presets by an earlier pack decision |
| Mob enhancement | No mob changes in GTIA |
| Circuit assembly line component amount | No circuit assembly line in GTIA |
| D-284 | GTIA's own chemistry rules (54 rules in all): catalyst wear (Normal: 1 % chance per run that the Ostwald/Claus catalyst wears out; Journey: never) and heat recovery (Journey: 1.5× the steam of the chemistry plants). Organ textures redrawn; Organ Modifier screen shows the slots on a body outline with an effect readout. Main menu: one row of four textured buttons (Singleplayer, Multiplayer, Settings, Quit) and a Discord icon. |
| D-285 | The Android `.mrpack` ships from 0.1.0-dev-5: Modrinth links where the exact file exists, every CurseForge-only jar inside the pack with the author's permission (owners informed; removed at once on request). Built locally with `tools/mrpack.py` and attached to the release. |
| D-286 | Space age direction: the station lives in Ad Astra's orbit, starts in HV and is modular (a core plus connectors and modules that grow the station, with GTIA-only modules); the extreme-gravity destination is an Ad Astra planet (datapack). Three community stations (ABFielder "Space Station fiop", Toppat Orbital Station, Icarus), cleared for use by the author, replace Ad Astra's default station structures with GTNA ABS casings and Ad Astra plating, doors and lamps. Fouling and vein purity rules are approved. |
| D-287 | Quest book layout in the GTNH way: `tools/quest_layout.py` places Steam, LV, MV, HV, Agriculture and Bees in dependency columns ordered to minimise crossings, with leaf quests in a ring around the quest they hang from and large collections as a grid block; tier-wide hubs (7+ dependents) do not place quests and their lines are hidden; long lines, lines over a quest and lines crossing twice per line are hidden. Every dependency stays (reachability). Visible crossings: Steam 102 → 5, LV 78 → 4, MV 35 → 6, HV 31 → 4. Book theme: opaque dark background, thick red/green lines. Era banners as chapter images. |
| D-288 | Creating a world whose preset changes a startup rule asks for a restart first, like GTO's difficulty: "Save and Quit" writes the rules, closes the game and keeps the choice for the next create-world screen. Opening a saved world with other startup values asks too (Save and Quit / Play anyway). |
| D-289 | Agriculture (21 quests) and Bees (13 quests) chapters in the Systems group. New recipes for the empty Bee Cage, the Honey Treat (Mixer) and the Greenhouse controller, which had none; a GameTest now checks that every GTIA machine has a recipe. |
| D-290 | Mode quests are visible from the start in worlds of their mode: the Starting Kits complete with their Start step's task, and one opening quest per mode explains what it changes. |
| D-291 | The Start splits GTO-style into **Welcome** (reading, the world's mode, rules, community, EMI and Crafting Chain tips) and a **step-by-step Start** that snakes from the first log to the first Coke, with tips next to the steps that need them; the author's 29 quests keep ids, text, tasks and rewards. Steam supplies become per-mode kits. Tips in LV, MV and HV. **Multiblock Goals** chapter after GTNH's: all 254 multiblocks in a grid, columns by family, rows by the voltage their controller recipe needs, text from each mod's own tooltip. |
| D-292 | Multiblock renders leave the quest map and quest text (EMI's preview stays, press R); the era banner sits in the free space nearest the chapter's entry quest. |
| D-293 | Steam, LV, MV and HV take the **GTNH 2.9 chapter structure**: a quest with a GTNH equivalent goes to its place, GTIA-only quests sit next to the quest they depend on, no quests added; dependencies thinned by the reachability check to 1–2 per quest. Every chapter has its own low-contrast pixel-art background tile: Steam bronze, LV grey, MV blue, HV light steel, EV light purple, IV dark blue; Welcome dark brick, Start stone, Agriculture farmland, Bees honeycomb, Energy coils, Wireless circuit traces, reference chapters a neutral grid. |
| D-294 | **No competing chemistry routes.** 47 GTCEu/GTNA direct syntheses that skipped GTIA's chemistry lines are removed in both modes: aluminium (bauxite, sapphire, kyanite, clay and aluminium sulfite electrolysis; the bauxite sludge chain), sulfuric acid, ammonia, nitric acid, membrane-less chlor-alkali, soda ash, titanium tetrachloride and its reduction outside the Kroll Reactor, quicklime, chemical ethylene (cracking stays) and log pyrolysis. By-products (ores, distillation, recycling, silicate decomposition) stay. The GTCEu silicon boule stays because the HV Siemens Reactor needs HV circuits, which need wafers. Quests that relied on the old routes now point to GTIA's plants. |
| D-295 | Each Multiblock Goals quest gives a small pack of its row's metal (4 bronze, steel, aluminium, stainless steel, titanium or tungstensteel ingots; 2 of the LuV–UV metal; 1 neutronium), checked by the reachability tool. |
| D-296 | Steam, LV, MV and HV go back to the v7 layout (each quest's own x/y) until the new GTNH layout is approved: the D-293 layout hid the lines of 36–58% of the quests in each chapter and left 15–29 quests per chapter with no line at all. |
| D-297 | The GTNH layout is redone by the generator around GTNH's hubs: checked GTIA↔GTNH pairs; where a GTIA quest takes a GTNH hub, the quests under it depend on it (implied dependencies only); a GTNH hub with no GTIA pair becomes a GTIA milestone quest (imported or checkmark); the GTNH grid is compacted; GTIA-only quests branch in straight rows; quests move before lines are hidden; sizes 1/2/3. Targets: no quest without a line, at most 10% with hidden lines, no overlaps or lines over quests. |
| D-298 | Work moves to mechanics, processing lines and performance; the quest book comes last, before the public release. Changes target critical, specific points: GTCEu machines and multiblocks stay and get recipes with new materials, and a new machine is added only when no existing one can do the step. Alternative routes follow GTNH's model (for example three routes to aluminium ingots). |
| D-299 | Nothing from GTNA or GTIA is removed (lines, recipe types, machines). Late GTNA machines are gated by their controller recipe: the Integrated Ore Processor around IV/LuV, the PCB Factory after LuV. |
| D-300 | Reusable machines and mechanics live in GTIACore (revises part of D-206). |
| D-301 | Multiblock structures are proposed by the assistant at the level of detail of GTNA's structures and approved by the author, starting with the Wood Retort, Lime Kiln and Diaphragm Cell. |
| D-302 | Chemistry slice 01 structures replace the D-251 boxes: Wood Retort as a brick bench with a wrought-iron retort, condenser and decanter (12×12×8); Lime Kiln as a banded shaft kiln with a hoist tower (7×14×5); Diaphragm Cell as a row of 3 to 9 Hooker cells, one parallel per cell, still limited by energy. |
| D-303 | The Integrated Ore Processor controller moves from the EV Assembler to the IV Assembly Line (7,680 EU/t). |
| D-304 | GTNH-style electrolyzer: 26 silicate and clay decompositions cost MV, 18 give Alumina instead of Aluminium (for the Hall-Héroult Cell), bastnasite gives Rare Earth instead of cerium; recycling and source ores stay. |
| D-305 | Dust-to-fluid extraction is removed for 13 EBF-only materials (Extractor and Liquefaction Furnace); parts and ingots still melt. Greenhouses, Tree Growth Simulator and Atomization stay as they are. |
| D-306 | Pig iron steelmaking with existing machines: PBF/EBF make Pig Iron and Slag from hematite or magnetite, coke and calcite; the LV Arc Furnace turns pig iron and oxygen into steel; slag replaces stone dust in concrete. |
| D-307 | Air separation stays as it is (LV Centrifuge, Vacuum Freezer, Distillation Tower). |
| D-308 | Three aluminium routes: dust in the EBF at HV (480 EU/t); dust pressed into Crude Aluminium and melted at MV, slowly; alumina and carbon in the EBF at MV, at half the Hall-Héroult yield. |
| D-309 | Naquadah reactor ladder in GTNA: the Large Naquadah Reactor (ported from GregTech Odyssey, UHV) and the Naquadah Hyper Reactor (GTNA original, UEV, four times the EU per mB, oxygen or nitrogen plasma boosters). GTNA adds Naquadah Fuel and Enriched Naquadah Fuel with simple default recipes; GT:IA will replace the fuel chain later. |
