# Yabai + skhd Configuration

Yabai (window manager) and skhd (hotkey daemon) configuration for macOS.

**⚠️ This configuration works WITHOUT disabling SIP (System Integrity Protection).**

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

## Keybindings

### Navigation (vim-style)
- `Alt + h/j/k/l` - Focus windows (left/down/up/right)
- `Alt + Shift + h/j/k/l` - Swap windows

### Spaces/Workspaces
**⚠️ Switching between spaces requires SIP to be disabled. Use macOS native shortcuts instead:**

1. Enable in **System Settings → Keyboard → Keyboard Shortcuts → Mission Control**:
   - ✅ Mission Control
   - ✅ Move left a space
   - ✅ Move right a space
   - ✅ Switch to Desktop 1, 2, 3...

2. Use these shortcuts:
   - `Ctrl + 1, 2, 3...` - Switch to space 1, 2, 3...
   - `Ctrl + Left/Right` - Move between spaces
   - `Ctrl + Up` - Open Mission Control

### Layouts
- `Alt + s` - Toggle split orientation (horizontal/vertical)
- `Alt + f` - Toggle fullscreen
- `Alt + Shift + Space` - Toggle float
- `Alt + Shift + =` - Balance window sizes

### Window Management
- `Alt + Shift + q` - Close window
- `Alt + Shift + c` - Reload yabai configuration

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

## Configuration Details

- **Layout**: Binary space partitioning (BSP)
- **Gaps**: 15px padding and gaps
- **Mouse follows focus**: Enabled
- **Window opacity**: Active 100%, inactive 95%
- **Auto-float apps**: Finder, System Settings, Calculator, Activity Monitor

## SIP Limitations

This configuration is designed to work **without disabling SIP (System Integrity Protection)**.

### What works:
✅ Window navigation and management
✅ Tiling and floating layouts
✅ Window opacity and shadows
✅ Custom gaps and padding

### What doesn't work (requires SIP disabled):
❌ Switching between spaces/desktops via yabai commands
❌ Moving windows between spaces via yabai commands
❌ Creating/destroying spaces programmatically

**Solution**: Use macOS native keyboard shortcuts for space management (see Keybindings section above).

For full yabai functionality with SIP disabled, check the [official guide](https://github.com/koekeishiya/yabai/wiki/Disabling-System-Integrity-Protection).
