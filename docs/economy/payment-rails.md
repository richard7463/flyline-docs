# Payment rails

**Status: Planned / Not currently available**

Flyline does not currently accept payments or expose a network service. This page describes a possible future service layer, not a current integration.

## What a future payment would pay for

A payment rail would only be considered for a separately deployed service: for example, a hosted replay, a reproducible evaluation job, a read-only observation feed, or a constrained agent request. It would not pay for a stronger local fly, a mutation, extra energy, a higher GF success rate, or a different experimental result.

The service would need a stable request and response contract before payment was added. The local browser game should remain playable without a wallet and without a network connection.

## MurMur as an external case study

MurMur documents a useful reference pattern for connecting neural decisions to economic actions without making a language model the decision-maker. In that design, a neural state can be read out into an intention such as what to buy, how much to pay, and which seller to use. A receipt can preserve the relevant buyer and seller state, a decision hash, and payment provenance.

That pattern is not Flyline functionality. Flyline currently has no neural-agent economy, wallet, settlement contract, or neural receipt registry. It also does not claim a relationship with MurMur.

## Possible x402 flow

If Flyline later exposes a paid HTTP service, an x402-compatible flow could be evaluated:

1. A client requests a declared resource.
2. The service returns HTTP `402` with payment requirements.
3. The client signs a payment payload, potentially using an EIP-3009 `transferWithAuthorization` authorization for USDC.
4. The service verifies the payload with a facilitator before doing billable work.
5. The service performs the work only after the verification policy passes.
6. The facilitator settles the authorization, and the service returns the result with settlement status or a pending reference.

Verification and settlement are separate concerns. A successful HTTP response must not be treated as proof that an on-chain transfer is final: a settlement can be pending or fail. The service would need explicit retry, timeout, refund, and user-visible status rules.

## Candidate roles for Arc, USDC, and Circle Facilitator

- **USDC** could be evaluated as a unit of account and settlement asset for a future service. Flyline does not currently custody, accept, transfer, or distribute USDC.
- **Arc** could be evaluated as a candidate network or settlement environment. Flyline is not currently deployed on Arc.
- **Circle Facilitator** could be evaluated as an external component for payment verification and settlement orchestration. No Facilitator integration is currently deployed.
- **x402** could be evaluated as a request-level payment negotiation protocol. Flyline does not currently expose an x402 endpoint.

The final choice would depend on network availability, fees, confirmation behavior, liquidity, operational controls, privacy, regional requirements, and security review. Naming a candidate is not a product commitment.

## Required controls before launch

A real service would require, at minimum:

- a stable resource identifier and price policy;
- idempotency keys and replay protection;
- a clear distinction between authorization, verification, settlement, and finality;
- bounded budgets, rate limits, kill switches, and abuse monitoring;
- handling for pending, failed, duplicated, and partially completed requests;
- a defined custody boundary and no hidden private-key dependency;
- receipts that can be audited without exposing unnecessary gameplay or wallet data;
- a privacy and retention notice;
- security, legal, accounting, and operational review.

Payment receipts and wallet identity must remain separate from the current `localStorage` lineage save. A future service may issue its own receipt record, but it must not silently turn a local game save into a financial account.

## References for future evaluation

These are external references, not Flyline dependencies or endorsements:

- [x402 documentation](https://docs.x402.org/)
- [x402 reference implementation](https://github.com/coinbase/x402)
- [Circle USDC developer documentation](https://developers.circle.com/stablecoins)
- [Circle x402 documentation](https://developers.circle.com/x402)
- [Arc](https://www.arc.network/)
- [Arc documentation](https://docs.arc.network/)
- [MurMur on GitHub](https://github.com/EvolutionDeep/murmur)
