# Code conventions

These rules apply to every mod in the organisation.

## Size

- **Keep files small.** A Java class over ~500 lines should be split by responsibility. A test class over ~800 lines should be split by system (`multiblock/<machine>/`, `compat/<mod>/`).
- **No giant log files.** Do not keep growing ledgers, journals or "continuity" files in the repository. History belongs in git commits and changelogs; decisions belong in the decisions page.
- One topic per pull request.

## Comments

- Write comments only at **key points**: a non-obvious rule, a balance number with its reason, a workaround for another mod, a mixin target. Code that explains itself gets no comment.
- No comments that repeat the code, no commented-out code, no "added by…", no TODOs without an issue.
- Key comments are written in **English, Portuguese and Chinese**, so any developer can understand why the code is there:

```java
// EN: Bees only open in GregTech machines; the Productive Bees centrifuge is removed.
// PT: O comb só abre em máquinas GT; a centrífuga do Productive Bees foi removida.
// ZH: 蜂巢只能在格雷科技机器中处理；已移除 Productive Bees 的离心机。
```

## Languages

- Every name a player can see ships in `en_us`, `pt_br` and `zh_cn` in the same commit. A GameTest fails when one is missing.
- Commit messages, changelogs and public docs are in English.

## Content

- Content (machines, recipes, materials) lives in Java. KubeJS only removes or blocks recipes.
- Multiblock tooltips follow the GTNA format (D-244).
- The author's textures and art are never replaced without the author's approval.
