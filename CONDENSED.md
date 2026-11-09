# Condensed mirror of `earendil-works/pi`

This repository is a **condensed copy** of [earendil-works/pi](https://github.com/earendil-works/pi),
trimmed from 4,215 files to fewer than 1,000 while keeping the core source tree.

## What is kept

| Package | Role |
|---|---|
| `packages/ai` | Unified LLM API + model catalog |
| `packages/agent` | Agent loop |
| `packages/coding-agent` | Coding agent CLI |
| `packages/tui` | Terminal UI |
| `packages/schema` | Shared schemas |
| `packages/mcp` | MCP client/transports |
| `packages/codemode` | Code-mode runtime |
| `packages/telemetry` | Telemetry |
| `packages/evals` | Evaluation harness |

Plus the root build scripts and configuration needed to build them.

## What was removed

- All test suites, test fixtures and benchmark files.
- Documentation, examples, changelogs and CI/nix configuration.
- `packages/chord`, `packages/durable`, `packages/env` and `apps/p2` — a separable stack that depended on
  `chord`; nothing in the kept packages imports them.
- Generated binary assets and browser-smoke check scripts for the removed packages.

Root `package.json` workspaces, `tsconfig.json` path mappings and the build chain were updated to match.

## License

MIT — see [LICENSE](LICENSE). Original work by the Pi authors at earendil-works.
