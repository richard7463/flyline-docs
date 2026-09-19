# Game/UI boundary

**Status: Implemented**

The DOM overlay handles menus, long text, HUD content, and touch controls. Phaser handles the dish, fly, predator, food, particles, and spatial feedback.

## Input flow

```text
touch joystick / mouse / keyboard
        → UI or scene input
        → GameScene
        → simulation rules
        → Phaser world and HUD
```

Menus and mutation cards should call scene methods rather than directly changing Phaser objects. World rules should not depend on whether a particular DOM element exists; that keeps the logic layer reusable by the current experiment and future clients.

The overlay stays above the canvas. Pause and GF controls remain above the full-screen joystick, and the joystick must not cover critical buttons.
