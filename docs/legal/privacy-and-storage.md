# Privacy and local storage

**Status: Implemented for local-only play; Not currently available for network services**

The current release is a single-player front-end game. Lineage progress, mutations, seed, egg history, and connectivity mode are stored in the browser's `localStorage` so the same browser can continue the run.

No login is required, and progress does not depend on a game server. Clearing the save or browser site data can permanently remove the local lineage from that browser.

The current release has no leaderboard, external-agent service, multiplayer service, public observation endpoint, wallet, or payment integration. If any network feature is added, it must receive a separate notice covering data collected, identity, retention, security, and deletion.

A future service might process a wallet address, payment authorization, service receipt, or on-chain transaction reference. Those records must remain separate from the local lineage save. An on-chain record may be difficult or impossible to delete, while a local save can be cleared; future documentation must explain that distinction before collecting either. No specific wallet, facilitator, or retention policy exists today.
