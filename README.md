# dotfiles.macos

Personal macOS configuration files for a minimal tiling window manager setup.

## Setup

This configuration provides a vim-style tiling window manager experience on macOS without disabling SIP.

### Components

- **AeroSpace** - Tiling window manager with vim keybindings
- **Borders** - Visual borders for active windows

### Installation

1. Install Homebrew if not already installed:
```bash
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
```

2. Install AeroSpace:
```bash
brew install --cask nikitabobko/tap/aerospace
```

3. Install Borders:
```bash
brew tap FelixKratz/formulae
brew install borders
brew services start borders
```

4. Copy configuration:
```bash
mkdir -p ~/.config/aerospace
cp aerospace/aerospace.toml ~/.config/aerospace/
```

5. Start AeroSpace (or logout/login)

## Keybindings

### Window Navigation (Vim style)
- `Alt + h/j/k/l` - Focus left/down/up/right
- `Alt + Shift + h/j/k/l` - Move window left/down/up/right

### Workspaces
- `Alt + 1-9` - Switch to workspace
- `Alt + Shift + 1-9` - Move window to workspace
- `Alt + Tab` - Toggle between current and previous workspace

### Layouts
- `Alt + s` - Toggle split horizontal/vertical
- `Alt + f` - Fullscreen toggle
- `Alt + Shift + Space` - Toggle floating/tiling

### Resize Mode
- `Alt + r` - Enter resize mode
- `h/j/k/l` - Decrease width / Increase height / Decrease height / Increase width
- `=` - Balance sizes
- `Esc` or `Enter` - Exit resize mode

### Utilities
- `Alt + Shift + =` - Balance window sizes
- `Alt + Shift + c` - Reload configuration
- `Alt + Shift + q` - Close window

## License

MIT License - Feel free to use and modify as needed.
