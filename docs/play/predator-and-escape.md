# Predators and escape

**Status: Implemented**

## Three predator phases

1. **Approach:** the predator selects and closes on a target; distance, scent, and traits can affect the situation.
2. **Lunge:** at commitment, it locks a target position and travels along the committed trajectory.
3. **Recover:** after the attack, it recovers and gives the player another decision window.

The lunge is not a homing missile. Once committed, it does not continuously retarget. This makes GF a timing and reading problem rather than a simple speed comparison.

## GF READY

The simplified motion-vision model aggregates threat evidence into a Giant Fiber (GF) escape response. When the HUD or lower-right button says **READY**, press Space or tap **GF ESCAPE**. A successful response can move the fly clear of the committed trajectory, but it consumes energy and enters cooldown.

Pressing too early may spend the response before the threat is committed; pressing too late may leave insufficient room. Mutations can change perception, cooldown, jump distance, or cost.

## If the escape fails

A hit ends the current generation. The result still leads to a mutation choice and the lineage continues. This keeps the predator meaningful without turning one mistake into a total account reset.
