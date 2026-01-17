+++
title = "Installation"
description = "How to install Nomacs."
date = 2024-02-08T18:39:07Z
updated = 2026-01-17T18:30:49Z
draft = false
weight = 30
sort_by = "weight"
template = "docs/page.html"

[extra]
lead = ""
toc = true
top = false
+++

nomacs – Image Lounge is licensed under the GNU General Public License v3
© Markus Diem, Stefan Fiel, and Florian Kleber, 2011 – 2020

## 64-bit Windows

- [Installer](https://github.com/nomacs/nomacs/releases/latest/download/nomacs-setup-x64.msi)
- [Portable package](https://github.com/nomacs/nomacs/releases/latest/download/nomacs-portable-win.zip)

## Linux

### Repositories

- [AUR](https://aur.archlinux.org/packages/nomacs)
- [Fedora](https://packages.fedoraproject.org/pkgs/nomacs/nomacs/index.html)
- [openSUSE](https://software.opensuse.org/package/nomacs)
- [Debian](https://packages.debian.org/search?searchon=names&keywords=nomacs)

  Translations can be installed from the package `nomacs-l10n`.

- [Ubuntu](https://packages.ubuntu.com/search?keywords=nomacs&searchon=names)

  Translations can be installed from the package `nomacs-l10n`.

### Distro agnostic

- [Flatpak](https://flathub.org/apps/details/org.nomacs.ImageLounge)
- [AppImage](https://github.com/nomacs/nomacs/releases/download/3.22.0/nomacs-3.22.0-linux-24.04-x86_64-AppImage.zip)

## MacOS

- [arm64](https://github.com/nomacs/nomacs/releases/download/3.22.0/nomacs-3.22.0-macOS-arm64.zip)
- [x86_64](https://github.com/nomacs/nomacs/releases/download/3.22.0/nomacs-3.22.0-macOS-x86_64.zip)

## FreeBSD

- Update your FreeBSD repository and change directory to `/usr/ports/graphics/nomacs`
  (if your repository directory is the default, otherwise change to the particular directory)
- Build and install nomacs by typing:

    ```shell
    make install clean
    ```

## Build from source

Get the source code from [the latest release tarball](https://github.com/nomacs/nomacs/archive/refs/tags/3.22.0.tar.gz)
or clone from the [Git repository](https://github.com/nomacs/nomacs).

Follow the build instruction in the README.md.
