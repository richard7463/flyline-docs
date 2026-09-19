# Economy and optional services

**Status: Planned / Not currently available**

Flyline currently has no wallet, account system, blockchain connection, payment flow, USDC settlement, x402 endpoint, token, or external-agent API. The game remains a local, single-player browser experience with browser saves.

This section records a possible future service boundary and a research direction. It does not describe shipped functionality, an endorsement of any external project, or a promise that a token or payment system will launch.

## Three separate layers

Any future design must keep these objects distinct:

1. **Game resources** — energy, eggs, traits, generation outcomes, and lineage score. These are local simulation values and are not money.
2. **Service payments** — a possible future way to pay for separately deployed services such as observation, replay, evaluation, or hosted experiments. A payment must not rewrite the local simulation rules.
3. **Protocol token** — a possible future asset that would need a real, non-speculative protocol utility. It must not be used to buy escape success, energy, mutations, or other survival advantages.

USDC, if ever evaluated, would be a candidate settlement asset rather than a synonym for game resources. A token, if ever evaluated, would be a separate protocol decision rather than an automatic reward for playing.

## Why MurMur is relevant as a reference

MurMur is an external fruit-fly-agent project that explores a different direction: neural agents whose internal state can produce economic intent, with metered services and on-chain settlement as part of the surrounding system. Its documented ideas are useful for comparison, including:

- a neural state read-out that can form an economic intention;
- x402-style HTTP payment negotiation;
- USDC and EIP-3009 authorization flows;
- a facilitator that verifies and settles payments;
- neural receipts that bind a decision record to a payment provenance record.

Flyline does **not** currently integrate MurMur, reuse its code, depend on its services, share a token, or claim a partnership. The comparison is architectural research only.

## Proposed readiness sequence

A responsible sequence would be:

```text
local simulation
  → replay and lineage receipt schema
  → authoritative hosted session
  → read-only observation API
  → constrained action and evaluation API
  → optional x402 service payments
  → token evaluation, only if a separate utility survives review
```

Payment belongs outside `sim.js` and outside the local lineage save. It should not become a hidden dependency of the single-player game.

## Design commitments

- No pay-to-win access to energy, mutations, GF timing, escape probability, or predator outcomes.
- No payment-based change to the fixed experiment's rules, metrics, or connectivity comparison.
- No token, reward, yield, price, buyback, airdrop, or investment-return promise.
- No wallet requirement for the current game.
- No public API claim until an interface, threat model, privacy notice, and validation process exist.

See [Payment rails](payment-rails.md) for the possible service settlement design and [Future token economics](token-economics.md) for the constrained research framework.
