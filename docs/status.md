# Project status

This page separates current behavior from proposals. Status labels are **Implemented**, **In progress**, **Planned**, **Experimental**, and **Not currently available**.

## Implemented

- Single-player dish survival: foraging, energy, automatic egg laying, predator pressure, and a 50-second generation.
- Predator `approach → committed lunge → recover` state machine.
- GF escape response, keyboard/mouse controls, and mobile floating joystick and GF button.
- Lineage progression, three-card Mutation Draft, and player/wild-type egg comparison.
- Multiple numerical and behavioral mutations, day/night variation, sound, particles, and slow-motion feedback.
- Browser `localStorage` saves and a DOM-independent simulation layer.

## Experimental

- A paired comparison between real and shuffled connectivity under the fixed assay described in [Reproducible experiment](biology/reproducible-experiment.md). The published figures are only seed `1337`, `200` paired trials, real `100% / 0.202s`, and shuffled `68% / 0.183s`.

## In progress

- Behavioral implementation and validation for the remaining mutation designs.
- Predator feints, repeated attacks, mid-generation events, and environment rotation.
- Daily seed challenges, a lineage tree, and a fuller onboarding flow.
- Real-device feel, balance, and long-session evaluation.

## Planned

- More biological mechanisms only where they change player observation, action, or cost.
- Better replay and evaluation tooling after the single-player rules and interfaces are stable.

## Not currently available

- AI or external-agent control.
- Multiplayer or battle-royale play.
- Public read-only observation APIs.
- Cross-seed benchmark infrastructure, leaderboards, cloud saves, or network accounts.
- Wallets, payment services, USDC settlement, x402 endpoints, Arc deployment, or Circle Facilitator integration.
- MurMur integration, token issuance, token rewards, yield, or financial products.

Future ideas must not be read as product promises until their rules, interfaces, and validation criteria are implemented and documented.
