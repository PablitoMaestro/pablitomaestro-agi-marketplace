# pablitomaestro-agi-marketplace

A curated marketplace of AGI-grade plugins for Claude Code and Codex, maintained by [PablitoMaestro](https://github.com/PablitoMaestro).

## Install the marketplace

```
/plugin marketplace add PablitoMaestro/pablitomaestro-agi-marketplace
```

Then install any plugin from the catalog:

```
/plugin install <plugin-name>@pablitomaestro-agi-marketplace
```

To refresh after the marketplace is updated:

```
/plugin marketplace update pablitomaestro-agi-marketplace
```

## Plugins in this marketplace

| Plugin | Description | Repo |
|---|---|---|
| `autonomous-appbuilder` | 7-phase orchestrator (idea → PRD → design → scaffold → env → execute → review → smoke), main-loop or two deterministic Workflow engines (`build-app-workflow`, `forge`). Worktree-isolated parallel builds; ships to a private GitHub repo + Vercel with push-to-deploy. Cross-tool (Claude Code + Codex). | [PablitoMaestro/autonomous-appbuilder](https://github.com/PablitoMaestro/autonomous-appbuilder) |
| `immortals` | Autonomous life cycle runner with multi-world orchestration. Spawns Claude agents as mythological beings that explore, work, and pass wisdom across lives. | [PablitoMaestro/claude-immortals](https://github.com/PablitoMaestro/claude-immortals) |

More to come — each plugin lives in its own repo with its own versioning. This catalog points to them via `github` sources, so installing the marketplace gives you access to all of them.

## How this is wired

This repo only holds `.claude-plugin/marketplace.json` — the catalog. It does NOT contain plugin source code. Each entry in the catalog has a `source` pointing to the actual plugin repo. Claude Code clones each plugin source on `/plugin install`.

To submit a new plugin to this marketplace, open an issue or PR with the plugin's repo URL and a short description.

## License

MIT — see [LICENSE](./LICENSE).
