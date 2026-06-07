---
title: Post-Install
parent: OpenCore Guide
nav_order: 9
description: Copy EFI to the internal disk and verify the finished Hackintosh.
permalink: /docs/post-install.html
prev_step:
  title: Boot and Install macOS
  url: /docs/boot-install.html
next_step:
  title: Troubleshooting
  url: /docs/troubleshooting.html
---
# Post-Install

After macOS setup finishes, keep the USB plugged in. You still need to copy the working EFI to the internal drive.

## Mount the Internal EFI

Use an EFI mounting tool or Terminal commands to mount the internal disk's EFI partition.

A manual Terminal approach looks like this:

```bash
diskutil list
sudo diskutil mount diskXsY
```

Replace `diskXsY` with the EFI partition for the internal macOS disk, not the USB.

## Copy the EFI

1. Open the USB drive in Finder.
2. Copy the working `EFI` folder.
3. Open the mounted internal `EFI` volume.
4. Delete the placeholder EFI folder if one exists.
5. Paste your working `EFI` folder.
6. Restart.
7. Remove the USB.

If the computer boots without the USB, the OpenCore install is now on the internal disk.

## Verify Hardware

Test:

- Graphics acceleration.
- Ethernet.
- Wi-Fi and Bluetooth, if supported.
- Audio.
- USB 2 and USB 3 ports.
- Sleep and wake.
- Restart and shutdown.
- Trackpad, keyboard, brightness, and battery status on laptops.

## Keep Backups

Save copies of:

- The working EFI.
- The USB installer EFI.
- Your `config.plist` before major edits.

Never update macOS, OpenCore, or kexts without a known-good backup.
{% include step_nav.html %}
