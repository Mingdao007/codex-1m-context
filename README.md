# codex-1m-context

A Claude Code skill that configures [Codex CLI](https://github.com/openai/codex) to use a 1M token context window.

## What it does

Adds two settings to `~/.codex/config.toml`:

```toml
model_context_window = 1000000
model_auto_compact_token_limit = 900000
```

This allows Codex to use the full 1M context window instead of the default, with auto-compaction triggered at 900K tokens.

## Installation

Copy `codex-1m-context.md` to your Claude Code commands directory:

```bash
cp codex-1m-context.md ~/.claude/commands/
```

Then use it in Claude Code:

```
/codex-1m-context
```

## Requirements

- [Claude Code](https://docs.anthropic.com/en/docs/claude-code) CLI
- [Codex CLI](https://github.com/openai/codex) installed with `~/.codex/config.toml` present
