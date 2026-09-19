# Contributing

**Status: Implemented contribution guidance**

## Understand the boundary first

Read the player guide, [architecture](../systems/architecture.md), and [reproducible experiment](../biology/reproducible-experiment.md). Even a small change may affect seeds, GF timing, predator commitment, or save compatibility.

## Code principles

- Keep `sim.js` free of DOM, Phaser, and `localStorage` dependencies.
- Add traits through `TRAIT_INFO → recomputeStats → scene hook`.
- Do not add continuous tracking during the predator's committed lunge.
- Do not let presentation randomness alter world rules.
- Do not describe a planned feature as implemented.
- Give new save fields a safe default.

## Before submitting

1. Run the logic experiment and syntax checks.
2. Manually play the start, forage, escape, result, draft, and next-generation flow.
3. If touch or responsive layout changes, check both desktop and a real mobile device.
4. Update affected public pages and mark the implementation status.

The project license is not final. Confirm the maintainer's authorization arrangement before contributing code or assets.
