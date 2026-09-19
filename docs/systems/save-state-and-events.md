# Save state and events

**Status: Implemented for local saves; Not currently available for cloud/network saves**

## Local save

The current save record uses the browser key `flyline_v1` and includes generation, player and wild-type mutations, world seed, connectivity mode, lineage eggs, best eggs, and history.

This is browser-local storage, not account synchronization. Clearing the save affects the current browser site data and does not send game content to an external service.

## DOM events

- `flyline:genstart`: a generation starts.
- `flyline:genend`: a generation ends with result and draft information.
- `flyline:log`: a HUD log message.

The Phaser scene owns gameplay state; the DOM overlay displays it. They communicate through events and explicit scene methods.

## Not currently available

Cloud saves, leaderboards, public observation APIs, external-agent state services, and multiplayer state are not implemented. Any future network feature would need a separate data, identity, retention, and security specification.
