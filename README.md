# FreeBSDDesktop
This repository is for FreeBSD Desktop ISO downloading.

FreeBSD Foundation doesn't provide desktop ISO officially. If the users want to enable the desktop, it needs user to install libaries and configue it. It is time consuming, and for some begginers, they may struggle in enabling the desktop.This project provides the deskop ISO which is based on the same source base as official FreeBSD DISC ISO.

The ISO includes:
  1. Official FreeBSD DISC.
  2. Intel/AMD GPU drivers matched with Linux LTS 6.1.
  3. GNOME Desktop.
  4. Fireofx/Chromium preinstalled.
     
If you have other requirements, like xfce desktop, mate desktop, etc. Please feel free to publish in "Issues".

To make the USB installer on Linux or FreeBSD:
1. Plugin a USB disk.
2. dd if=./FreeBSD-14.1-RELEASE-p6-amd64-Gnome-Desktop.iso of=/dev/sda bs=4M
