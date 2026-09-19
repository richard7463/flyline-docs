# Escape circuit

**Status: Implemented in a simplified game model**

## From motion vision to escape

Flyline's first biology module is organized around a fruit fly's escape response to an approaching threat:

```text
motion vision
   ├─ LC4: a design channel for angular-velocity-related input
   └─ LPLC2: a design channel for looming-related input
                    ↓
             Giant Fiber (GF)
                    ↓
              jump escape
```

The game combines these evidence streams into a thresholded GF response. A faster, larger, or closer threat can make the response more ready; the player still decides whether and when to act.

## Two input channels

- **LC4:** represented here as sensitivity to changes in angular velocity; design anchor: about **2,442 synapses**.
- **LPLC2:** represented here as sensitivity to looming size change; design anchor: about **1,366 synapses**.
- **GF:** represented in the game by readiness, jump distance, cooldown, and energy cost.

These are connection-data anchors, not a deployed cell-level network.

## Why arrangement matters in the game

The real and shuffled configurations use the same predator context and paired trial count while changing the arrangement of input weights. In the fixed baseline, the real configuration is more reliable under the declared metric. That is a testable game-model hypothesis, not a statement that real connectivity is universally superior or that the result transfers directly to animals.

## Limits and extensions

The current mapping reduces rich time-varying visual signals to a small rule set. Potential extensions include finer looming and angular-velocity traces, light and circadian modulation, and olfactory context. Each extension must preserve a clear mapping, a player consequence, and a rerunnable test.
