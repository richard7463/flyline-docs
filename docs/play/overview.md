# Overview

**Status: Implemented**

Flyline is a single-player lineage-survival game. The meaningful unit is not one immortal fly but a lineage that must repeatedly turn energy into eggs while avoiding a committed predator attack. A generation lasts up to 50 seconds and ends when the fly is killed, runs out of energy, or reaches the time limit.

## Four decisions

| Decision | Trade-off |
| --- | --- |
| Where to forage | Food value, travel time, and predator exposure |
| When to keep eating | More energy and eggs versus a more exposed position |
| When to press GF | Preserve the escape resource versus avoid the committed trajectory |
| Which mutation to take | A future way of living, not a universal upgrade |

## A generation's rhythm

- **Early:** establish energy and learn the food layout.
- **Middle:** automatic egg laying begins while predator pressure becomes harder to ignore.
- **Late:** decide whether another risky food run is worth more eggs.
- **Resolution:** compare with the wild type and choose the next mutation.

A death ends the current generation, not the lineage. The intended challenge is to learn which choices work under which risk pattern rather than to discover one dominant build.

## FAQ

**Do I control egg laying?** No. Egg laying is automatic when the energy condition is met; your control is the route and risk that make it possible.

**Does the predator continuously track me?** No. The documented lunge commits to a trajectory. The decision is about reading that commitment and using GF at the right time.

**What does a mutation do?** It changes a rule, cost, threshold, or behavior. The useful question is not “is this stronger?” but “what situation makes this trade-off worthwhile?”

**Is this a biological simulator?** No. It is a connectome-inspired game model. See [Biology boundaries](../biology/biology-boundaries.md).

**Can I play online with others or control it through an API?** Not currently. The shipped scope is single-player and local; future ideas are labeled separately.
