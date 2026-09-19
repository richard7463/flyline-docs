# Local development

**Status: Implemented**

Flyline is a static page with no bundling step. Phaser is loaded from the vendor directory and the entry page loads the JavaScript modules directly.

```bash
cd /path/to/flyline
python3 -m http.server 8124
```

Then open `http://127.0.0.1:8124/`. Do not open the entry page with `file://`; browsers commonly restrict module loading in that mode.

## Important files

- `index.html`: game DOM structure.
- `style.css`: page and HUD styling.
- `js/sim.js`: pure simulation and experiment.
- `js/scene-game.js`: Phaser gameplay orchestration.
- `js/ui.js`: menu, HUD, mutation draft, and touch input.
- `js/scene-boot.js`: procedural textures.
- `js/audio.js`: WebAudio effects.

Local development does not require an account, database, or external API.
