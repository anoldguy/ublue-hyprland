# Opinionated atomic Hyprland operating system image

Based on:
- [Fedora](https://fedoraproject.org/) - base OS packages, rpm-ostree system
- [Universal Blue](https://universal-blue.org/) - build system, codecs, additional tools
- [Hyprland COPR](https://copr.fedorainfracloud.org/coprs/solopasha/hyprland/) - Hyprland packages

Additional software/patches:
- [GNOME keyring for Hyprland](config/files/usr/share/xdg-desktop-portal/portals/gnome-keyring-Hyprland.portal)
- GUI/CLI audio controls, alacritty, some of the [modern CLI tools](https://github.com/ibraheemdev/modern-unix), NetworkManager, dunst and [others](config/recipe.yml)

## Install

### 1. Install any `rpm-ostree`-based system

- [Immutable Fedora with GNOME](https://fedoraproject.org/silverblue/)
- [Immutable Fedora with KDE](https://fedoraproject.org/kinoite/)

### 2. Rebase

Just run the following command in the terminal
```
sudo rpm-ostree rebase ostree-image-signed:docker://ghcr.io/vfosnar/ublue-hyprland
```

## Configuration

You can apply my base Hyprland configuration (keybinds, daemons) by adding the following line in your config:

```
source = /usr/share/ublue-os/hypr/hyprland.conf
```
