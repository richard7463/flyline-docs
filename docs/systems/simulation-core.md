# Simulation core

**Status: Implemented**

The pure simulation layer contains the rules needed for:

- seeded random numbers and world initialization;
- GF input, thresholds, and escape trials;
- trait definitions, stat recomputation, and fly initialization;
- the real/shuffled connectivity experiment.

## Rules and presentation are separate

Speed, metabolism, perception, damage, and escape windows are rules. Particles, sound, screen shake, slow motion, and floating text are presentation. Presentation may clarify feedback but must not silently change the assay or consume simulation randomness.

## Why purity matters

A DOM-independent layer makes the current experiment rerunnable and keeps future clients possible. It does not mean that a server, multiplayer mode, or public API exists today; those are **Not currently available**.
