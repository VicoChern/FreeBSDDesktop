# FreeBSDDesktop
This repository is for FreeBSD Desktop ISO downloading.

FreeBSD Foundation doesn't provide desktop ISO officially. If the users want to enable the desktop, it needs user to install libaries and configue it. It is time consuming, and for some begginers, they may struggle in enabling the desktop.This project provides the deskop ISO which is based on the same source base as official FreeBSD DISC ISO.

The latest ISO includes GNOME, KDE5, XFCE, MATE, LXQT, and Cinnamon, and is splitted to 2 parts:
  1. Part A: FreeBSD-14.2-Desktop-RELEASE-amd64.iso-aa
  2. Part B: FreeBSD-14.2-Desktop-RELEASE-amd64.iso-ab
   
How to conmbine them to one ISO:
> cat FreeBSD-14.2-Desktop-RELEASE-amd64.iso-* > FreeBSD-14.2-Desktop-RELEASE-amd64.iso

After files combined, please makesure sha256 value is matched. It is only validated on Intel platforms (Intel GPU).

The ISO includes:
  1. FreeBSD DISC ISO base.
  2. Intel/AMD GPU drivers matched with Linux LTS 6.1.
  3. GNOME, KDE5, XFCE, MATE, LXQT, and Cinnamon.
  4. Chromium preinstalled.
  5. No src and ports.
  6. Only one desktop can be selected while installing.
     
To make the USB installer on Linux or FreeBSD:
  1. Plugin a USB disk.
  2. Check your USB disk device node. Usually, on Linux, it is /dev/sdX, and on FreeBSD, it is /dev/daX.
  3. For example,
     1. On Linux:
     > dd if=./FreeBSD-14.1-RELEASE-p6-amd64-Gnome-Desktop.iso of=/dev/sda bs=4M. (Make sure 'of=xxx' is your USB disk device node)
     2. On FreeBSD:
     > dd if=./FreeBSD-14.1-RELEASE-p6-amd64-Gnome-Desktop.iso of=/dev/da0 bs=4M. (Make sure 'of=xxx' is your USB disk device node)

