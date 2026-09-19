# Future directions

**Status: Planned / Not currently available**

## Constrained agent control

The pure logic layer could eventually support a limited observation/action schema: a controller would receive only declared sensory and internal state and submit only direction and escape intent. This interface is not available now.

## Same-world evaluation

After the single-player rules, interface, baseline controller, and cross-seed scoring are stable, the project may study human/agent comparisons, read-only state, leaderboards, and benchmark protocols. None is a current online feature.

## Optional service infrastructure

Only after the local rules and public interfaces are stable, Flyline may evaluate a hosted observation, replay, or evaluation service. A possible sequence is `receipt schema → authoritative session → read-only observation → constrained action/evaluation → optional x402 payment`. USDC, Arc, and Circle Facilitator are candidate infrastructure choices, not current dependencies. Any service would need idempotency, replay protection, bounded budgets, failure handling, privacy rules, and security review before launch.

## MurMur as an external reference

MurMur is a separate project whose documented neural receipt and agent-economy patterns may inform research. Flyline has no MurMur SDK, contract, API, payment route, token relationship, or partnership. Its ideas must not be presented as current Flyline functionality.

## Token economics

Token economics remains research only. A token would be considered only if a real protocol utility could not be handled by conventional accounting or a stable settlement asset. It must not buy survival power, mutations, energy, GF timing, or experimental outcomes. No token issuance, supply, price, reward, yield, buyback, airdrop, or investment return is currently defined. See [Future token economics](../economy/token-economics.md).

## More biology

Phototaxis, circadian rhythm, olfaction, pheromones, foraging, and predator learning are possible future modules. Each must change a player choice rather than merely add a scientific label.

## Multiplayer

Multiplayer or battle-royale play is a distant architecture direction, not a current capability. It would require an authoritative server simulation, disconnection and fairness rules, observation permissions, and a security review.
