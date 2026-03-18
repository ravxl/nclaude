# nclaude

Interactive CLI launcher for [Claude Code](https://claude.ai/claude-code) with project folder navigation.

## Features

- **Mode selection** — Choose between Normal or YOLO (`--dangerously-skip-permissions`) mode
- **Folder management** — Save frequently used parent folders, add new ones on the fly
- **Project picker** — Automatically lists subfolders inside your selected parent folder
- **Paginated navigation** — Arrow keys, number keys (0-9), and page navigation (left/right)
- **Fuzzy search** — Press `/` to search through any list
- **Breadcrumb trail** — Color-coded trail showing your selections as you go

## Dependencies

- [gum](https://github.com/charmbracelet/gum) — used for the fuzzy search feature

```bash
brew install gum
```

## Install

```bash
# Copy the script to your PATH
cp nclaude ~/.local/bin/nclaude
chmod +x ~/.local/bin/nclaude

# Make sure ~/.local/bin is in your PATH
export PATH="$HOME/.local/bin:$PATH"
```

## Usage

```bash
nclaude
```

### Controls

| Key | Action |
|---|---|
| `↑` / `↓` | Navigate items |
| `←` / `→` | Previous / next page |
| `0`-`9` | Select numbered item on current page |
| `/` | Open fuzzy search |
| `Enter` | Confirm selection |
| `Ctrl+C` | Quit |
| `Ctrl+D` | Quit |

### Configuration

Saved folders are stored in `~/.config/nclaude/folders.txt` (one path per line).

## License

MIT
