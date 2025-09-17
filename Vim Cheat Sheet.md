# 🧭 Navigation

## basic

- `h` - Move left
- `l` - Move right
- `j` - Move down
- `k` - Move up

## line

- `w` - Jump to start of next word
- `b` - Jump to start of previous word
- `e` - Jump to end of word
- `0` - Jump to beginning of line
- `^` - Jump to first non-blank character of line
- `$` - Jump to end of line

## paragraph

- `{` — Previous paragraph
- `}` — Next paragraph
- `zz` — Center the current line
- `zt` — Move current line to **top** of screen
- `zb` — Move current line to **bottom** of screen
- `Ctrl + d` — Scroll half a screen **down**
- `Ctrl + u` — Scroll half a screen **up**
- `Ctrl + f` — Scroll **full screen down**
- `Ctrl + b` — Scroll **full screen up**

## file

- `:42` - Go to line `42` (or any number)
- `gg` - Go to top of file
- `G` - Go to bottom of file
- `gd` - Go to definition
- `gf` - Go to file (import)
- `:vsplit file` — Open file in vertical split
- `:split file` — Open file in horizontal split
- `:Ex` or `:Explore` — Open file explorer

## ✏️ Insert Mode

- `i` - Insert before cursor
- `I` - Insert at beginning of line
- `a` - Insert after cursor
- `A` - Insert at end of line
- `o` - Open new line below and insert
- `O` - Open new line above and insert
- `Esc` - Exit insert mode

## 🔁 Undo/Redo

- `u` - Undo
- `Ctrl + r` - Redo

## 🧹 Editing / Deleting

- `x` - Delete character under cursor
- `dd` - Delete current line
- `dw` - Delete word
- `d$` - Delete to end of line
- `d0` - Delete to beginning of line
- `D` - Delete to end of line (same as `d$`)
- `cw` - Change (delete + insert) word
- `cc` - Change entire line
- `C` - Change to end of line (same as `c$`)

## 📋 Copy / Paste (Yank / Put)

- `yy` - Yank (copy) current line
- `yw` - Yank word
- `Y` - Yank to end of line
- `p` - Paste after cursor
- `P` - Paste before cursor

## 📦 Visual Mode

- `v` - Start visual mode (character-wise)
- `V` - Start visual line mode
- `Ctrl + v` - Start visual block mode
- `y` - Yank selection
- `d` - Delete selection
- `.` / `,` - Indent / unindent selection

## 🔍 Search

- `-text` - Search forward for "text"
- `?text` - Search backward for "text"
- `n` - Repeat last search in same direction
- `N` - Repeat last search in opposite direction

## 🪝 Markers & Jumps

- `m[a-z]` — Set a mark (e.g., `ma` sets mark `a`)
- `'a` — Jump to beginning of line with mark `a`
- `Ctrl + o` — Go **back** to previous jump location
- `Ctrl + i` — Go **forward** to next jump location

## ✨ Other

- `.` - Repeat last command
- `:%s/old/new/g` - Replace all "old" with "new"
- `:w` - Save file
- `:q` - Quit
- `:wq` - Save and quit
- `:q!` - Force quit (discard changes)
