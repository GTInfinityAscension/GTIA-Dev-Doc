# Performance

The pack targets **under 4 GB of RAM** on servers and clients, and Android through the Amethyst launcher. Every optimization goes in with numbers from before and after, measured the same way.

## How we measure

`tools/perf_bench.py` in the modpack boots a dedicated server with exactly the locked mods (median of 3 runs) and records:

| Metric | Meaning |
| --- | --- |
| `wall_s` | Seconds from launch until the server is ready |
| `done_s` | Minecraft's own "Done (…)" time (world preparation) |
| `heap_after_gc_mb` | Live heap after a forced full GC (class histogram) |
| `mspt` | Average server tick time while `/gtialib bench` keeps a grid of GT machines running |

```sh
python3 tools/perf_bench.py my-label --runs 3 --extra DIR_WITH_CANDIDATE_JARS \
    --tick gtceu:lv_electric_furnace:2000:minecraft:raw_iron --replace gtna=path/to/gtna.jar --off gtcovers
```

Results are appended to `~/MineProjects/GTIA-arquivo/perf/<label>.jsonl`. Profiles use JFR (`--jvm "-XX:StartFlightRecording=..."`).

## Results so far (GTIA, 129–134 mods, dedicated server)

| Change | Where | Before | After |
| --- | --- | --- | --- |
| Spawn chunks 441 → 25 (`spawnchunks`) | Ascension Optimizer | ready in 47 s, world prep 21.0 s, live heap 887 MB | 31 s, 5.9 s, 625 MB |
| Infinity cover check without building lists | GTNA | 8.37 ms/tick (2,000 working LV furnaces) | 3.74 ms/tick |
| Allocation-light `getCovers()` (`gtcovers`) | Ascension Optimizer | 8.37 ms/tick | 3.93 ms/tick |
| ModernFix `dynamic_resources` on, LeanObject server-only | Pack config | client live heap at the menu 1,030 MB (4 GB limit) | 650 MB |

## Rules

1. Measure before writing the optimization; profile to find the real hotspot.
2. Keep the optimization switchable (Ascension Optimizer features can be turned off in `config/ascopt-mixins.properties`).
3. Run the mod's full GameTest suite after the change.
4. Record the numbers in the commit, the changelog and this page.
