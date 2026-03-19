# Neovim Config

Personal Neovim configuration using lazy.nvim.

## Structure

- `init.lua`: options, keymaps, autocmds, lazy bootstrap
- `lua/custom/plugins/init.lua`: plugin specs and configs
- `lazy-lock.json`: plugin lockfile

## Requirements

- Neovim 0.10+ (recommended)
- `git`
- `rg` (Telescope live_grep)
- Nerd Font (icons)
- `make` (optional, for `telescope-fzf-native`)

## Usage

```sh
nvim
```

Inside Neovim:

```
:Lazy
:Lazy sync
:checkhealth
```

Common entry points:

- `\\` to reveal the current file in Neo-tree
- `<leader>sf` to find files
- `<leader>sg` to grep the project
