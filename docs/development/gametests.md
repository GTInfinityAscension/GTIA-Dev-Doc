# GameTests

Every mod runs its GameTests in CI with `./gradlew runGameTestServer`. The rules below follow the [Horizon-QA principles](https://github.com/GTNewHorizons/Horizon-QA/blob/master/PRINCIPLES.md) used by GTNH.

1. **Functional tests, not mocks.** Place real blocks and run the real machine.
2. **Mock supply, not validation.** A test may give a machine its inputs any way it likes, but it never bypasses recipe logic.
3. **Wait on state, not ticks.** Tick counts are only timeouts.
4. **Negative tests matter.** For every new multiblock, add at least a "forms" test and a test that it does not form, or does not run, when it should not.
5. **Leave no trace.** Remove any block placed outside the template, and never leave a synthetic recipe registered.
6. **Failures explain themselves.** The message says what went in, what was expected and what happened.

## Sweep tests

Each mod has tests that sweep over everything it registers, so new content is checked the day it is added:

- every multiblock forms from its own preview;
- no GT recipe has an empty input or output, or a duration of 0;
- every machine tooltip builds without a raw translation key;
- every name exists in en_us, pt_br and zh_cn.
