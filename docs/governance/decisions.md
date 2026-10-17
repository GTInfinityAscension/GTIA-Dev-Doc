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
