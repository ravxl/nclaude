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

### Option 1: Symlink (recommended for development)

```bash
ln -sf "$(pwd)/nclaude" ~/.local/bin/nclaude
```

### Option 2: Copy

```bash
cp nclaude ~/.local/bin/nclaude
chmod +x ~/.local/bin/nclaude
```

### Make sure `~/.local/bin` is in your PATH

Add to your `~/.zshrc` (or `~/.bashrc`):

```bash
export PATH="$HOME/.local/bin:$PATH"
```

Then reload: `source ~/.zshrc`

## Usage

```bash
nclaude              # Interactive folder + mode selection
nclaude .            # Launch in current directory (pick mode)
nclaude --here -Y    # Launch YOLO in current directory (no prompts)
nclaude -H -N        # Launch Normal in current directory (no prompts)
```

### Options

| Flag | Description |
|---|---|
| `--here`, `-H`, `.` | Launch Claude in the current directory (skip folder selection) |
| `--yolo`, `-Y` | Use YOLO mode (`--dangerously-skip-permissions`) |
| `--normal`, `-N` | Use Normal mode |
| `-h`, `--help` | Show help |

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
