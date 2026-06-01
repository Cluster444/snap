# Snap Docs

This directory is a Mintlify documentation root for the Snap architecture concept.

This directory pins Node 24 through `.mise.toml` because the Mintlify CLI does not support Node 25+.

From the repository root, preview the docs locally:

```bash
bun run docs:snap:dev
```

Validate the site:

```bash
bun run docs:snap:check
```

The Bun scripts run Mintlify inside `docs/snap` through mise, which uses the docs-local Node 24 config. Mintlify still requires Node.js 20.17.0 or newer, so the Node 24 mise config is intentional even though Bun is the command runner.

If you are working directly from this directory, install the docs-local toolchain and run Mintlify through mise:

```bash
mise install
mise exec -- bunx mint dev
```

When the docs are ready to publish, connect the repository to Mintlify and set the docs source directory to `docs/snap`.

The current source-of-truth design document is `packages/engine/VISION.md`. These pages split that vision into a public, navigable documentation site with examples and reference pages.
