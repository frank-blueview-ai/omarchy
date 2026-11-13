# Blue View desktop integration

This optional integration brings the Blue View theme, live sky and screensaver, movable settings window, taskbar appearance controls, and per-window opacity controls to Omarchy. It is maintained in [Blue-View-Window-Theme-Omarchy](https://github.com/frank-blueview-ai/Blue-View-Window-Theme-Omarchy); this directory contains the Omarchy-specific installable source and its original license.

On an existing Omarchy installation, run `./install.sh` from this directory. It builds the Hyprland title-bar and snapping plugins, installs the Blue View shell plugins, and adds the Blue View settings icon to the bar. Use `./install.sh --no-theme` to keep the current theme. Restart the session if the title-bar plugins do not load immediately.

The settings window controls the live desktop, screensaver, location, clock, window corners, and taskbar appearance. Use the ◐ title-bar button to adjust an individual window, optionally remembering its opacity for the application. Application opacity also affects text. The Blue View settings window remains readable and has its own background-opacity control.

User preferences are saved under `~/.local/state/bvos/`, `~/.config/hypr/bvos-*.lua`, and `~/.config/omarchy/shell.toml`. The uninstaller retains user preferences. The optional BlueView Desktop launcher is separate from this integration.

Run `python3 tests/install_smoke.py` and `python3 tests/appearance_test.py` for the isolated installer and helper checks. These tests do not replace graphical verification.
