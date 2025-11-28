# Yabai + skhd Configuration

Yabai (window manager) and skhd (hotkey daemon) configuration for macOS, converted from the original AeroSpace configuration.

## Installation

### 1. Install yabai and skhd

```bash
brew install koekeishiya/formulae/yabai
brew install koekeishiya/formulae/skhd
```

### 2. Create symlinks

```bash
# Replace <path-to-repo> with your actual repository location
ln -sf <path-to-repo>/dotfiles.macos/yabai/yabairc ~/.yabairc
ln -sf <path-to-repo>/dotfiles.macos/yabai/skhdrc ~/.skhdrc
chmod +x ~/.yabairc
```

### 3. Grant accessibility permissions

1. Open **System Settings → Privacy & Security → Accessibility**
2. Click the lock icon to unlock
3. Click the **+** button and add:
   - `/opt/homebrew/bin/yabai`
   - `/opt/homebrew/bin/skhd`
4. Make sure both checkboxes are enabled

### 4. Start services

```bash
yabai --start-service
skhd --start-service
```

## Keybindings (same as AeroSpace)

### Navigation (vim-style)
- `Alt + h/j/k/l` - Focus windows (left/down/up/right)
- `Alt + Shift + h/j/k/l` - Move windows

### Spaces/Workspaces
- `Alt + 1-9` - Switch to space 1-9
- `Alt + Shift + 1-9` - Move window to space 1-9 (and follow)
- `Alt + Tab` - Switch to recent space

### Layouts
- `Alt + s` - Toggle split orientation (horizontal/vertical)
- `Alt + f` - Toggle fullscreen
- `Alt + Shift + Space` - Toggle float
- `Alt + Shift + =` - Balance window sizes

### Window Management
- `Alt + Shift + q` - Close window
- `Alt + Shift + c` - Reload yabai configuration

### Resize Mode
- `Alt + r` - Enter resize mode
- In resize mode:
  - `h/j/k/l` - Resize window
  - `=` - Balance sizes
  - `Escape` or `Enter` - Exit resize mode

### Extras
- `Alt + r` - Rotate windows 90°
- `Alt + y` - Mirror on Y axis
- `Alt + x` - Mirror on X axis

## Logs and Debugging

View error logs:
```bash
tail -f /tmp/yabai_$USER.err.log
tail -f /tmp/skhd_$USER.err.log
```

View output logs:
```bash
tail -f /tmp/yabai_$USER.out.log
tail -f /tmp/skhd_$USER.out.log
```

## Restart Services

```bash
yabai --restart-service
skhd --restart-service
```

## Stop Services

```bash
yabai --stop-service
skhd --stop-service
```

## Differences from AeroSpace

- **Gaps**: Configured to 15px as in AeroSpace
- **Mouse follows focus**: Enabled
- **Opacity**: Inactive windows at 95% opacity
- **Float apps**: Finder, System Settings, Calculator automatically float

## Note about SIP

This configuration works **without disabling SIP**. The only limitations are:
- You can't move windows between spaces with animations (but it works with the current workaround)
- You can't create/destroy spaces from yabai

For full functionality, check the [official guide](https://github.com/koekeishiya/yabai/wiki/Disabling-System-Integrity-Protection).
