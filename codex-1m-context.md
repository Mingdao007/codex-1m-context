# /codex-1m-context — Enable 1M context window for Codex CLI

Configure Codex CLI to use 1M token context window with auto-compact at 900K.

## What it does

Adds two lines to `~/.codex/config.toml`:

```toml
model_context_window = 1000000
model_auto_compact_token_limit = 900000
```

## Steps

1. Read `~/.codex/config.toml`
2. Check if `model_context_window` and `model_auto_compact_token_limit` already exist
   - If both exist, inform the user and stop
   - If missing, proceed to add them
3. Insert the two lines right after the `model = "..."` line (top-level, before any `[section]`)
4. Show the user the updated top section of the file for confirmation

## Notes

- This skill only modifies context window settings. It does not touch model selection, MCP servers, trust levels, or any other config.
- If `~/.codex/config.toml` does not exist, inform the user to run `codex` first to generate a default config.
