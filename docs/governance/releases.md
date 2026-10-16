# Releases

| Channel | How it is made | Who it is for |
| --- | --- | --- |
| **Nightly** | Every push to `main` of the modpack replaces the [`nightly` pre-release](https://github.com/GTInfinityAscension/GregTech-Infinity-Ascension/releases/tag/nightly) | Testers who want the latest build |
| **dev / pre / alpha** | The Package workflow run by hand with a tag such as `0.1.0-dev-5`, `0.1.0-pre-1` or `0.1.0-alpha` | Testers following a milestone |
| **beta** | The same workflow with a `-beta` tag | The first channel published as stable |

Only the newest release of each group is kept (the newest beta and the newest dev/pre/alpha); the nightly is never removed by a versioned release.

Changelogs and release notes are written in English. Mods (GTIACore, GTNA, Agronomica) release on their own and the pack pins exact versions with SHA-256 in `manifest/full.lock.json`.

## Mobile

The pack targets Android through the Amethyst launcher with the `.mrpack` build, the same way GTNH supports mobile. Only the official `.mrpack` with default configs is supported; mobile bugs use the mobile issue form.
