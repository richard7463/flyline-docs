# Survival loop

**Status: Implemented**

```text
Move and forage
  → energy changes
  → eggs are laid automatically
  → predator approaches
  → predator commits to a lunge
  → GF escape or impact
  → 50 seconds / energy depletion / death
  → compare with wild type
  → choose one mutation
  → next generation
```

## Micro loop: seconds

You trade speed, energy, position, and exposure continuously. Eating restores energy but may require a vulnerable route. Staying mobile can reduce positional danger while increasing movement and metabolic cost. GF is a limited decision, not a permanent shield.

## Meso loop: one generation

A generation lasts up to 50 seconds. Eggs are the central output. The wild type provides a comparison in the same game context, while death ends only the current generation.

## Macro loop: lineage

Mutations accumulate into different survival styles: cautious foraging, high-risk feeding, lower metabolism, faster movement, or more deliberate escape. Some broader systems—environment rotation, mid-generation events, and more predator behaviors—are **In progress**, not current promises.

## Design test

A new system should answer which loop it serves and what decision it changes. A reward that only adds a number without changing observation, movement, timing, or risk belongs in neither the survival loop nor the lineage strategy.
