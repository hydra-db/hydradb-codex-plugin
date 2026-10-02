# HydraDB Codex Plugin

Persistent, cross-session memory for [Codex](https://developers.openai.com/plugins/build/plugins),
powered by [HydraDB](https://hydradb.com).

It recalls relevant notes when you send a prompt, syncs your markdown docs into
HydraDB, and saves conversations as durable memories - the same behavior as the
HydraDB Claude Code plugin, on the same underlying engine (`scripts/plugin.mjs`).

## Prerequisites

- Node.js >= 18 and npm
- A HydraDB account (API key + tenant ID) - [hydradb.com](https://hydradb.com)
- Codex

## Quick start

```bash
make bootstrap
export HYDRADB_API_KEY="your-api-key"
export HYDRADB_TENANT_ID="your-tenant-id"
```

Add a local marketplace entry in your project's `.agents/plugins/marketplace.json`
pointing at this folder, then enable the plugin in `.codex/config.toml`. See the
[Codex plugin docs](https://developers.openai.com/plugins/build/plugins) for the
current install flow.

## Configuration & usage

Config keys, environment overrides, capture/search/ingest modes, and the slash
commands are identical to the Claude Code plugin - see [docs/usage.md](docs/usage.md)
and `config.example.json`.

## License

[Apache 2.0](LICENSE) - Copyright (c) 2026 HydraDB
