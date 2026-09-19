# Future token economics

**Status: Planned / Research only / Not currently available**

Flyline does not currently have a token, token contract, wallet integration, rewards market, yield program, or financial product. No issuance date, symbol, supply, allocation, price, return, buyback, airdrop, or listing is promised.

The correct starting question is not “how can gameplay emit a token?” It is “what protocol problem would require one?” If a service can work with ordinary accounting or USDC, a separate token may add complexity without adding utility.

## Keep the economies separate

The game already has meaningful internal values:

- **Energy** is a survival constraint.
- **Eggs** represent automatic reproduction within a generation.
- **Traits** alter the lineage's rules and trade-offs.
- **Lineage score and generation outcomes** describe play, not ownership.

These values should remain simulation variables. They must not become cash balances, transferable assets, or purchasable advantages merely because a future service layer exists.

A future service could charge for a bounded hosted action, replay, observation, or evaluation. That is a service-price question, not proof that a token is needed. A protocol token would need a distinct utility, such as a narrowly defined coordination, quota, or governance function, and that utility would need to survive a non-token alternative analysis.

## Candidate utility tests

A token proposal would need to answer all of these questions before implementation:

1. What operation cannot be handled by ordinary database accounting or a stable settlement asset?
2. Who needs the token to perform that operation, and why is holding it necessary?
3. What prevents speculation from overwhelming the intended utility?
4. How are budgets, quotas, abuse, and automated activity controlled?
5. How can a user exit without being trapped by an illiquid or custodial system?
6. What data is recorded on-chain, and what must remain private or deletable off-chain?
7. What happens if the service, facilitator, network, or token contract is unavailable?

A negative answer should stop the token work rather than produce a token by default.

## Guardrails for a possible model

Any future economic design should preserve the following invariants:

- no token purchase increases energy, eggs, mutation quality, escape probability, or GF readiness;
- no token payment changes the real-versus-shuffled connectivity assay or its metrics;
- the base single-player game remains usable without a wallet;
- paid services are opt-in, metered, and bounded;
- rewards, if ever studied, compensate a verifiable service or contribution rather than sell survival power;
- allocation, treasury spending, emissions, and governance have public rules and auditable limits;
- anti-sybil and abuse controls do not require collecting more personal data than necessary;
- the system has a shutdown, migration, refund, and user-exit policy.

Possible non-financial sinks such as service quotas, experiment credits, reputation, or access scheduling should be tested in simulation before any transferable asset is considered.

## Review gates

A token design should not move beyond research until all of the following exist:

1. A stable product need that cannot be met by the local game or conventional service accounting.
2. A written economic model with supply, sinks, budgets, failure cases, and sensitivity analysis.
3. Security review for contracts, signatures, replay protection, oracle inputs, custody, and admin controls.
4. Privacy, legal, tax, accounting, and regional compliance review.
5. A non-transferable or testnet prototype that can be stress-tested without real user funds.
6. An independent review of pay-to-win, market manipulation, sybil resistance, and user-exit risks.
7. Explicit approval to move from research to implementation.

Until then, “future token economics” means a documented design question, not a product roadmap promise.
