# Deployment

**Status: Implemented for static hosting; external publishing configuration is Planned**

Flyline can be served by a static host: HTML, CSS, JavaScript, Phaser vendor files, and Markdown documentation can be published together.

Before deployment, confirm:

- ES modules load through HTTPS or a correctly configured HTTP server;
- the Phaser vendor file and all relative paths exist;
- the production page does not depend on a developer machine;
- gameplay regression checks and the fixed `runExperiment(1337)` check pass;
- local saves, development credentials, and debug logs are not published.

The repository is prepared for Markdown/GitBook synchronization, but this page does not claim that an external GitBook site has already been configured or published.
