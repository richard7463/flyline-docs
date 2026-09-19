# Deterministic RNG

**Status: Implemented for the current simulation rules**

The same world seed should produce the same world inputs so that experiments and debugging can be repeated.

## Current discipline

When a world resets, the seed is combined with the generation. Food layout, wild-type traits, and predator spawn positions consume random values in a defined order. New rule randomness must be appended after existing consumption rather than inserted in the middle, or old seeds will produce different worlds.

## Deliberate variation

Mutation Draft presentation retains some run-time freshness, and presentation timing does not define the rule result. A complete replay system is **Planned**; it would separate simulation RNG from presentation RNG and record every simulation input.

## Contribution rule

A rule change must state whether it adds RNG consumption and must rerun the fixed experiment with seed `1337`. Do not use an untracked random source inside the pure simulation layer.
