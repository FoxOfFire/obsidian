# 📝 Neovim + bootstrap.nvim LSP Keybinds Cheatsheet

## 🔍 Go To / Navigation

| Keybind | Action |
|---------|--------|
| `gd` | Go to definition (LSP) |
| `gD` | Go to declaration |
| `gi` | Go to implementation |
| `gr` | List references (LSP) |
| `K` | Show hover documentation |
| `<leader>rn` | Rename symbol under cursor |
| `<leader>ca` | Code action (quick fixes) |
| `[d` | Jump to previous diagnostic (error/warning) |
| `]d` | Jump to next diagnostic |
| `<leader>f` | Format current buffer (LSP format) |

______________________________________________________________________

## 🧰 Workspace / Diagnostics

| Keybind | Action |
|---------|--------|
| `<leader>e` | Show diagnostics in a floating window |
| `<leader>q` | Open location list with diagnostics |
| `<leader>F` | Format buffer asynchronously |

______________________________________________________________________

## 🔗 Telescope Integration (bootstrap.nvim defaults)

| Keybind | Action |
|---------|--------|
| `<leader>gd` | Find definition (via Telescope) |
| `<leader>gr` | Find references (via Telescope) |
| `<leader>gi` | Find implementations (via Telescope) |
| `<leader>ds` | Search document symbols |
| `<leader>ws` | Search workspace symbols |

______________________________________________________________________

## ⚡ Notes / Tips

1. `K` opens hover info — you can also map it to a floating preview with LSP.
1. Diagnostics jumps (`[d` / `]d`) work **across the buffer**.
1. `<leader>` in bootstrap.nvim defaults to `\` unless you changed it.
1. Telescope keybinds are optional but extremely handy for workspace-wide navigation.

______________________________________________________________________

This is a **ready-to-use reference** —
you can keep it open while learning LSP in Neovim.
