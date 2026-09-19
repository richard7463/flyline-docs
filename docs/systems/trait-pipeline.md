# Trait pipeline

**Status: Implemented for current traits; In progress for additional behavior cards**

## Data flow

```text
TRAIT_INFO
  → recomputeStats(fly)
  → stat fields and behavior flags
  → scene consumers
```

Behavioral traits should be represented through computed fly stats rather than scattered checks for trait names in scene code. This keeps each rule entry visible and testable.

## Consumers

- steering: light preference, intoxicated inertia, and automatic behavior;
- fly update: metabolism, feeding, egg laying, and interactions;
- predator update: mimicry, guarding, dormancy, and target selection;
- dash: jump distance, energy, and cooldown;
- GF update: the escape core and its experimental baseline.

## Acceptance criteria

Each new trait needs a benefit plus a cost or a strong situation, must change a player decision, and must not silently change the published assay. UI text, status summaries, and save fields should use the same key as the simulation layer.
