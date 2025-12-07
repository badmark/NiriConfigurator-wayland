# NiCoEd - Niri Configuration Editor

**NiCoEd** is a modern, graphical configuration editor for the **Niri** Wayland compositor. Built with **PyQt5**, it provides a user-friendly interface to manage your `config.kdl` file without needing to manually edit raw text for every setting (though a raw editor is included for advanced users).

## Features

* **GUI Configuration:** dedicated tabs for Input, Outputs, Layout, Workspaces, Window Rules, Keybindings, and more.
* **Hardware Detection:** Automatically detects connected monitors, DRM devices, and installed cursor themes to populate dropdown menus.
* **Raw Editor:** A full-featured text editor with line numbers and syntax validation for manual overrides.
* **Backup System:** Automatically creates backups (`config.kdl.bak#`) before saving changes.
* **Theme Support:** Built-in Light/Dark mode toggle that respects GTK/Qt styling.
* **Safe Saving:** Validates syntax before saving to prevent breaking your compositor configuration.

## Prerequisites

To run NiCoEd, you need Python 3 and the PyQt5 library installed on your system.

### Arch Linux
```bash
sudo pacman -S python-pyqt5
```

### Debian / Ubuntu
```bash
sudo apt install python3-pyqt5
```

### Fedora
```bash
sudo dnf install python3-qt5
```

### Pip (Universal)
```bash
pip install PyQt5
```

## Installation

1.  **Download the script:** Save the application code as `NiCoEd.py`.
2.  **Make it executable:**
    ```bash
    chmod +x NiCoEd.py
    ```
3.  **Run it:**
    ```bash
    ./NiCoEd.py
    ```

## Usage Guide

### Main Interface
The application is divided into tabs corresponding to Niri's configuration blocks:

* **Input:** Configure keyboard layout, touchpad gestures (tap to click, natural scroll), and mouse acceleration.
* **Outputs:** Manage monitor resolution, scale, position, and rotation. (Use the tree view to select a specific monitor).
* **Layout:** Adjust gaps, border width, focus ring colors, and tab indicators.
* **Workspaces:** Define named workspaces and bind them to specific outputs.
* **Window Rules:** Set rules for specific applications (e.g., force opacity or floating mode based on App ID).
* **Binds:** Add or edit keybindings. Supports standard actions (close window, quit) and spawning commands.
* **Full Config:** A direct text editor view of your `config.kdl`. Useful for pasting snippets or advanced configuration not covered by the GUI widgets.

### Saving Changes
Click **"Save All"** in the bottom right corner.
* This will write your changes to `~/.config/niri/config.kdl`.
* A backup of your previous config will be created in the same directory.
* You must restart or reload Niri for changes to take effect (depending on the specific setting).

### Loading Backups
The dropdown menu at the bottom allows you to select and load previous backup files immediately into the editor.

## Troubleshooting

* **"PyQt5 not found":** Ensure you have installed the dependencies listed in the Prerequisites section.
* **Wayland Issues:** If the window does not appear or looks incorrect on Wayland, try running with:
    ```bash
    QT_QPA_PLATFORM=xcb ./NiCoEd.py
    ```
    or ensure `qt5-wayland` is installed on your system.# NiriConfigurator-wayland
PyQt5 version of Niri Configuration Editor
