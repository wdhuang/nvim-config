# Repository Guidelines
This is a personal Neovim configuration focused on code review and small edits.

## Project Structure & Module Organization

`init.lua` is the entry point for options, keymaps, autocmds, and lazy.nvim bootstrapping. Plugin specs and configuration live in `lua/custom/plugins/init.lua`. `lazy-lock.json` pins plugin versions; update it only when intentionally changing plugin state. `README.md` covers usage and external requirements.

Keep the configuration review-oriented:

- Prefer built-in Neovim features unless a plugin materially improves code review flow.
- Default to lazy-loading on keys, commands, or file events; avoid `VimEnter` and unconditional startup plugins unless they are core UI.
- Avoid reintroducing heavy editing stacks such as LSP managers, completion frameworks, format-on-save pipelines, or DAP unless explicitly requested.
- When plugin behavior changes, keep `README.md`, `AGENTS.md`, and `lazy-lock.json` in sync.

## Build, Test, and Development Commands

There is no build step. Development is just running Neovim with this config.

```sh
nvim
```
Inside Neovim, common health and dependency checks:

```
:Lazy
:Lazy sync
:checkhealth
```

## Coding Style & Naming Conventions

Use tabs by default, with a display and indent width of 2 as configured in `init.lua`. `guess-indent.nvim` may still adapt buffers to an existing file's indentation style. Prefer single quotes for strings and `--` for comments. Keep settings and keymaps in `init.lua`; keep plugins in `lua/custom/plugins/init.lua` unless the file grows too large.

When changing plugin setup:

- Keep plugin specs small and cohesive.
- Prefer removing unused plugins over adding toggles for dead features.
- If a plugin is kept mainly for convenience, make sure it does not land on the startup path without a clear reason.
