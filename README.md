# Neovim Config

Personal Neovim configuration using lazy.nvim.

## Structure

- `init.lua`: options, keymaps, autocmds, lazy bootstrap
- `lua/custom/plugins/init.lua`: plugin specs and configs
- `lazy-lock.json`: plugin lockfile

## Requirements

- Neovim 0.10+ (recommended)
- `git`, `make`, `unzip`
- `rg` (Telescope live_grep)
- Nerd Font (optional, icons)

## Usage

```sh
nvim
```

Inside Neovim:

```
:Lazy
:Lazy sync
:Mason
:checkhealth
```
