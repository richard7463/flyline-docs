# Testing and validation

**Status: Implemented for the current checks; Experimental for the biology assay**

## Logic regression

```bash
node --input-type=module -e "import('./js/sim.js').then(m => console.log(m.runExperiment(1337)))"
```

The published check is `200` paired trials with real `100% / 0.202s` and shuffled `68% / 0.183s`. Do not substitute other experimental figures in public copy.

## Syntax checks

```bash
node --check js/sim.js
node --check js/scene-game.js
node --check js/ui.js
node --check js/scene-boot.js
```

## Browser flow

Check the menu, start flow, HUD, experiment entry point, pause, touch controls, and at least two generations. Browser automation can check page state and JavaScript errors; it cannot replace real-device evaluation of touch damping, button placement, sound, or long-term pacing.

## Documentation checks

Before publishing, verify every relative link in `SUMMARY.md`, every status label, and every scientific boundary statement. Never copy private paths, credentials, debug scripts, or tokens into public pages.
