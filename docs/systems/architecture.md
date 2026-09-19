# Architecture

**Status: Implemented**

## Layers

```text
index.html + style.css + ui.js
  DOM menu, HUD, mutation draft, and touch input
          ↕ events / scene methods
scene-game.js
  Phaser world, gameplay orchestration, predator, and generations
          ↓ imports pure functions
sim.js
  constants, seeded RNG, GF, experiment, traits, and stats
```

Supporting modules provide procedural textures, WebAudio, Phaser startup, and responsive canvas sizing.

## Public boundaries

- `sim.js` has no DOM, Phaser, or `localStorage` dependency and can run as a logic layer.
- `scene-game.js` is the orchestration point connecting pure rules to world objects.
- `ui.js` displays state and collects input; it should not duplicate rules.
- World coordinates remain independent of screen pixels through Phaser's game-size scaling.

## Event bridge

The game reports generation and HUD events to the DOM, while menus call explicit scene methods to begin a run, move to the next generation, or set a seed. The current public architecture is local and single-player; an external-agent interface or server is not implemented.

## Optional service boundary

If a future hosted service is built, it should sit outside the local simulation and event bridge. A possible HTTP observation, replay, or evaluation service could later be paired with x402 request payments, USDC settlement, an Arc network deployment, or Circle Facilitator-assisted settlement. None of these components exists in the current release, and MurMur is an external reference rather than a Flyline dependency.

The service boundary must not pull wallets, payment SDKs, chain state, or facilitator responses into `sim.js`. Payment receipts and wallet identity must remain separate from the current lineage save. A successful payment must not silently alter GF rules, experiment metrics, mutation outcomes, or the fairness of the local game.

## Extension rule

New environments, events, or traits should enter the existing layers without letting UI code mutate simulation state directly or pulling Phaser objects into the pure logic layer.
