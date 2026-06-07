---
title: Boot and Install macOS
parent: OpenCore Guide
nav_order: 8
description: Boot the USB, enter recovery, format the target disk, and install macOS.
permalink: /docs/boot-install.html
prev_step:
  title: Create the Installer
  url: /docs/create-installer.html
next_step:
  title: Post-Install
  url: /docs/post-install.html
---
# Boot and Install macOS

Before booting, connect ethernet if possible. Recovery installs often need network access.

## Boot From USB

1. Shut down the computer.
2. Plug in the installer USB.
3. Power on and repeatedly press your boot-menu key.
4. Choose the USB drive.
5. Wait for the OpenCore picker.

Common boot-menu keys include `F8`, `F9`, `F10`, `F11`, `F12`, `Esc`, or `Del`, depending on the manufacturer.

## OpenCore Picker Options

You may see entries such as:

1. Windows
2. macOS Base System / Install macOS / USB drive name
3. OpenShell.efi
4. Reset NVRAM

If some entries are hidden, press `Space`.

Choose the macOS installer or recovery entry.

## Recovery Screen

After booting recovery, you may see:

- Restore from Time Machine
- Reinstall macOS
- Safari
- Disk Utility

## Format the Target Disk

If the disk is empty or you are intentionally erasing it:

1. Open **Disk Utility**.
2. Choose **View -> Show All Devices**.
3. Select the physical target disk, not a partition.
4. Erase as:
   - Format: `APFS`
   - Scheme: `GUID Partition Map`
5. Confirm only when you are sure it is the right disk.

## Install macOS

1. Choose **Reinstall macOS**.
2. Continue through the prompts.
3. Agree to the terms.
4. Select the target disk.
5. Let the installer run.

The machine may reboot several times. Each time, boot back through the USB and choose the macOS installer or installed macOS volume until setup completes.

{: .important }
Do not unplug the USB until post-install is complete. Your internal disk probably cannot boot by itself yet.
{% include step_nav.html %}
