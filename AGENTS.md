# Repository Guidelines
This is a personal Neovim configuration.

## Project Structure & Module Organization

`init.lua` is the entry point for options, keymaps, autocmds, and lazy.nvim bootstrapping. Plugin specs and configuration live in `lua/custom/plugins/init.lua`. `lazy-lock.json` pins plugin versions; update it only when intentionally changing plugin state. `README.md` covers usage and external requirements.

## Build, Test, and Development Commands

There is no build step. Development is just running Neovim with this config.

```sh
nvim
```
Inside Neovim, common health and dependency checks:

```
:Lazy
:Lazy sync
:Mason
:checkhealth
```

## Coding Style & Naming Conventions

Use 2-space indentation in Lua files, matching `init.lua`. Prefer single quotes for strings and `--` for comments. Keep settings and keymaps in `init.lua`; keep plugins in `lua/custom/plugins/init.lua` unless the file grows too large.
