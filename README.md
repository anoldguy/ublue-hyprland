# Opinionated atomic Hyprland operating system image

Based on:
- [Fedora](https://fedoraproject.org/) - base OS packages, rpm-ostree system
- [Universal Blue](https://universal-blue.org/) - build system, codecs, additional tools
- [Hyprland COPR](https://copr.fedorainfracloud.org/coprs/solopasha/hyprland/) - Hyprland packages

Additional software/patches:
- [GNOME keyring for Hyprland](config/files/usr/share/xdg-desktop-portal/portals/gnome-keyring-Hyprland.portal)
- GUI/CLI audio controls, alacritty, some of the [modern CLI tools](https://github.com/ibraheemdev/modern-unix), NetworkManager, dunst and [others](config/recipe.yml)

## Install

### On bare metal without anything preconfigured

1. download an ISO file from the [latest release](https://github.com/vfosnar/ublue-hyprland/releases/tag/auto-iso)
2. flash it to your thumb drive
3. install the OS

You can find many guides on the internet on how to flash an ISO
- [https://learn.microsoft.com/en-us/linux/install](https://learn.microsoft.com/en-us/linux/install#create-a-bootable-usb-drive-to-install-bare-metal-linux)
- https://www.wikihow.com/Install-Linux

### From a `rpm-ostree`-based system

If you are already running a `rpm-ostree`-based system, you can just rebase using
```
sudo rpm-ostree rebase ostree-image-signed:docker://ghcr.io/vfosnar/ublue-hyprland
```

## Configuration

You can apply my base Hyprland configuration (keybinds, daemons) by adding the following line in your config:

```
source = /usr/share/ublue-os/hypr/hyprland.conf
```
