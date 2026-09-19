# Game loops

**Status: Implemented for the first two loops; In progress for macro systems**

## Four layers

- **Micro loop:** movement, foraging, energy, automatic eggs, and GF escape.
- **Meso loop:** a 50-second generation, wild-type comparison, and a three-card mutation choice.
- **Macro loop:** environment change, predator development, and mid-generation events; **In progress**.
- **Meta loop:** lineage records and future daily seeds or lineage-tree features; partly **Planned**.

Every new system should state which loop it serves and which player decision it changes. A feature that merely adds a reward should not silently become a meta-progression system.

## Per-frame order

```text
input → updateFly → GF / movement / feeding / egg laying
      → updatePredator → generation resolution → presentation → HUD
```

The committed lunge rule, GF assay, seed-consumption order, and DOM-independent simulation boundary are system invariants for the current implementation.
