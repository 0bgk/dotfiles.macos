# dotfiles.macos

Personal macOS configuration files for a minimal tiling window manager setup.

## Overview

This repository provides vim-style tiling window manager configurations for macOS. Choose between two options based on your needs:

| Feature | AeroSpace | yabai + skhd |
|---------|-----------|--------------|
| **Easy Setup** | ✅ Simple | ⚠️ Requires permissions |
| **SIP Required** | ❌ No | ❌ No (with limitations) |
| **Native macOS** | ✅ Yes | ✅ Yes |
| **Maturity** | 🆕 Newer | 🏆 Established |
| **Configuration** | TOML | Shell scripts |
| **Performance** | ⚡ Fast | ⚡ Fast |

### Choose Your Window Manager

#### Option A: AeroSpace (Recommended for beginners)
Modern tiling window manager designed for macOS. Easy to configure with TOML files.

👉 [See AeroSpace setup guide](aerospace/README.md)

#### Option B: yabai + skhd (Power users)
Highly customizable tiling window manager with extensive scripting capabilities.

👉 [See yabai setup guide](yabai/README.md)

## Prerequisites

- macOS 13.0 (Ventura) or later
- [Homebrew](https://brew.sh/) package manager

Install Homebrew if needed:
```bash
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
```

## Optional Components

### Borders
Visual borders for active windows (works with both window managers):

```bash
brew tap FelixKratz/formulae
brew install borders
brew services start borders
```

## Quick Start

1. Choose your window manager (AeroSpace or yabai)
2. Follow the installation guide in the respective folder
3. Link the configuration files
4. Start using your new tiling setup!

## Shared Keybindings

Both window managers use the same vim-style keybindings:

### Window Navigation
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
- `h/j/k/l` - Resize directions
- `=` - Balance sizes
- `Esc` or `Enter` - Exit resize mode

### Utilities
- `Alt + Shift + =` - Balance window sizes
- `Alt + Shift + c` - Reload configuration
- `Alt + Shift + q` - Close window

For more detailed keybindings, see the individual configuration files.

## License

MIT License - Feel free to use and modify as needed.
