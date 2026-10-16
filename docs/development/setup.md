# Setup

All mods target **Minecraft 1.20.1, Forge 47.4.x, Java 17** and build with Gradle (ModDevGradle legacy Forge).

```sh
git clone https://github.com/GTInfinityAscension/GTIACore.git
cd GTIACore
./gradlew build
./gradlew runGameTestServer -PgtiaDevOptionalDependencies=true
```

| Command | What it does |
| --- | --- |
| `./gradlew runClient` | Starts a development client |
| `./gradlew runData` | Regenerates data (recipes, models, `en_us.json`) |
| `./gradlew runGameTestServer` | Runs every GameTest headlessly and exits with an error on failure |
| `./gradlew spotlessApply` | Formats the code |

GTIACore needs GTNA and AE2 at runtime. Without them, pass `-PgtiaDevOptionalDependencies=true` so the test server can start.

## The modpack

The pack is managed with packwiz. `manifest/full.lock.json` is the source of truth: `tools/pack.py lock|fetch`, then `tools/packwiz_sync.py`. Quests are generated from `quests-src/` with `tools/questgen.py build` and checked with `tools/questgen.py check`.
