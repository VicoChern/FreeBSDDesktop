# FreeBSDDesktop
This repository is for FreeBSD Desktop ISO downloading.

FreeBSD Foundation doesn't provide desktop ISO officially. If the users want to enable the desktop, it needs user to install libaries and configue it. It is time consuming, and for some begginers, they may struggle in enabling the desktop.This project provides the deskop ISO which is based on the same source base as official FreeBSD DISC ISO.

The ISO includes:
  1. FreeBSD DISC ISO base.
  2. Intel/AMD GPU drivers matched with Linux LTS 6.1.
  3. GNOME Desktop.
  4. Fireofx/Chromium preinstalled.
  5. No src and ports (To make the ISO as small as possible since github limit single file size < 2GB.)
     
If you have other requirements, like xfce desktop, mate desktop, etc. Please feel free to publish in "Issues".

To make the USB installer on Linux or FreeBSD:
1. Plugin a USB disk.
2. Check your USB disk device node. Usually, on Linux, it is /dev/sdX, and on FreeBSD, it is /dev/daX.
3. For example,
   On Linux: dd if=./FreeBSD-14.1-RELEASE-p6-amd64-Gnome-Desktop.iso of=/dev/sda bs=4M. (Make sure 'of=xxx' is your USB disk device node)
   On FreeBSD: dd if=./FreeBSD-14.1-RELEASE-p6-amd64-Gnome-Desktop.iso of=/dev/da0 bs=4M. (Make sure 'of=xxx' is your USB disk device node)

By the way, I have created another ISO based on 14.2, which includes GNOME, KDE5, XFCE, MATE, LXQT, and Cinnamon, but the ISO size is more than 3GB, and can't be uploaded to github. If you need it, please reach to me.
Only validate ISOs for Intel platforms.
