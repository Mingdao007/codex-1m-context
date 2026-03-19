# Codex 1M Context

Configure [Codex CLI](https://github.com/openai/codex) to use a 1M token context window with auto-compact at 900K. Works with `Claude Code CLI`.

## What ships

| Item | Path |
|---|---|
| Installable command | `codex-1m-context.md` |

## Install / Use

Copy to your Claude Code commands directory:

```bash
cp codex-1m-context.md ~/.claude/commands/
```

Then invoke in Claude Code:

```
/codex-1m-context
```

## Coverage

Adds two lines to `~/.codex/config.toml`:

```toml
model_context_window = 1000000
model_auto_compact_token_limit = 900000
```

The skill only touches context window settings. It does not modify model selection, MCP servers, trust levels, or any other config.

## Trigger examples

- "Open 1M context for Codex"
- "Codex 上下文开到 1M"

## Non-trigger examples

- Changing the Codex model or reasoning effort.
- Configuring MCP servers or trust levels.

## Privacy boundary

This public repository contains no personal identifiers, absolute paths, tokens, or machine-specific configuration.

## Repository layout

```
codex-1m-context/
  codex-1m-context.md   # Claude Code command (entry point)
  README.md             # This file
  LICENSE
```

## Platform support

- macOS
- Linux

Requires `~/.codex/config.toml` to exist. If it does not, run `codex` once to generate a default config.

## License

MIT
