# AeroSpace Configuration

Window manager for macOS with vim-style keybindings. AeroSpace is a modern tiling window manager inspired by i3 and designed specifically for macOS.

## Prerequisites

- macOS 13.0 (Ventura) or later
- [Homebrew](https://brew.sh/)

## Installation

### 1. Install AeroSpace

```bash
brew install --cask nikitabobko/tap/aerospace
```

### 2. Link configuration

```bash
# Replace <path-to-repo> with your actual repository location
mkdir -p ~/.config/aerospace
ln -sf <path-to-repo>/dotfiles.macos/aerospace/aerospace.toml ~/.config/aerospace/aerospace.toml
```

### 3. Start AeroSpace

AeroSpace will start automatically on login (configured in the TOML file).

To start manually:
```bash
open -a AeroSpace
```

## Features

- **Vim-style navigation**: `hjkl` for window focus and movement
- **Multiple workspaces**: Quick switching with `Alt + 1-9`
- **Automatic tiling**: Binary space partitioning layout
- **Custom gaps**: 15px spacing between windows
- **Float exceptions**: System apps automatically float
- **Mouse follows focus**: Cursor moves to focused window
- **Resize mode**: Interactive window resizing with `Alt + r`

## Keybindings

See the [aerospace.toml](aerospace.toml) configuration file for all keybindings.

### Quick reference

| Key | Action |
|-----|--------|
| `Alt + h/j/k/l` | Focus window (left/down/up/right) |
| `Alt + Shift + h/j/k/l` | Move window |
| `Alt + 1-9` | Switch to workspace |
| `Alt + Shift + 1-9` | Move window to workspace |
| `Alt + s` | Toggle split orientation |
| `Alt + f` | Toggle fullscreen |
| `Alt + r` | Enter resize mode |
| `Alt + Shift + c` | Reload configuration |

## Configuration

The main configuration file is [aerospace.toml](aerospace.toml). After making changes:

```bash
# Reload configuration
# Press: Alt + Shift + c
# Or restart AeroSpace from the menu bar
```

## Uninstallation

```bash
brew uninstall --cask aerospace
rm ~/.config/aerospace/aerospace.toml
```

## Resources

- [Official Documentation](https://nikitabobko.github.io/AeroSpace/guide)
- [GitHub Repository](https://github.com/nikitabobko/AeroSpace)
- [Configuration Reference](https://nikitabobko.github.io/AeroSpace/config-ref)

## Notes

- AeroSpace works without disabling System Integrity Protection (SIP)
- Native macOS app with no additional dependencies
- Supports multiple monitors
- Mission Control integration
