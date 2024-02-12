+++
title = "Installation"
description = "How to install Nomacs."
date = 2024-02-08T18:39:07Z
updated = 2024-02-08T18:39:07Z
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

## Windows (7/8/10)

- [installer (64 bit)](https://github.com/nomacs/nomacs/releases/latest/download/nomacs-setup-x64.msi)
- [multi-user installer (64 bit)](https://github.com/nomacs/nomacs/releases/latest/download/nomacs-setup-x64.exe)
- [nomacs portable .zip package (64 bit)](https://github.com/nomacs/nomacs/releases/latest/download/nomacs-portable-win.zip)

## Windows (2000/XP/Vista)

- [nomacs portable .zip package](https://github.com/nomacs/nomacs/releases/download/2.4.6/nomacs-2.4.6-x86-WinXP.zip)

[Click here for older versions](https://github.com/nomacs/nomacs/releases)

## Flathub

We maintain a [flathub](https://flathub.org/apps/details/org.nomacs.ImageLounge) app.
We recommend installing nomacs from there if you want to have the latest version.

## Ubuntu and Linux Mint

nomacs is available in the “universe” repository of Ubuntu.
Just install it using your favorite package manager.
Translations can be added with `sudo apt-get install nomacs-l10n`.
Install the heif plugin to load heif images.

## Debian/Fedora

nomacs is included in the official repositories.

## Arch Linux

nomacs is available as [an AUR package](https://aur.archlinux.org/packages/nomacs).

## openSUSE

[repositories](https://software.opensuse.org/download/package?project=X11:QtDesktop&package=nomacs) (Tumbleweed, Factory, 12.1, 11.4)

## FreeBSD

- Update your FreeBSD repository and change directory to `/usr/ports/graphics/nomacs`
  (if your repository directory is the default, otherwise change to the particular directory)
- Build and install nomacs by typing:

    ```shell
    make install clean
    ```

## OS/2

[.7z package](ftp://ftp.netlabs.org/pub/qtapps/nomacs-2.4.6-os2.7z)

## Other Linux distribution

If there is no package available for your favorite distribution,
you can download the [sources](http://github.com/nomacs/nomacs/releases/latest)
and compile nomacs according to the compile instructions.

## Source

- [Git repository](https://github.com/nomacs/nomacs.git) (containing the source code of nomacs and all dependencies)
- [Tarball](https://github.com/nomacs/nomacs/releases/)

## nomacs uses these libraries

- OpenCV
- Qt
- LibRaw
- Exiv2

## Herbie – Diagnostics

Herbie is a small cpu monitoring tool.
[Download](https://github.com/diemmarkus/Herbie/releases/download/0.2/herbie-setup.exe)
