---
title: Boot and Install macOS
parent: OpenCore Guide
nav_order: 7
description: Boot the Hackintosh USB installer, choose macOS in OpenCore, enter recovery, format the target disk, and install macOS on a compatible PC.
permalink: /docs/boot-install.html
keywords:
  - boot Hackintosh USB
  - install macOS on PC
  - OpenCore picker
  - macOS recovery
  - Hackintosh install
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

1. Connect ethernet if possible.
2. Plug in the installer USB.
3. Shut down the computer.
4. Power on the computer.
5. Repeatedly press your boot-menu key while the computer starts.
6. Choose the USB drive from the one-time boot menu.
7. Press `Enter`.
8. Wait for the OpenCore picker.

Common boot-menu keys include `F8`, `F9`, `F10`, `F11`, `F12`, `Esc`, or `Del`, depending on the manufacturer.

## OpenCore Picker Options

You may see entries such as:

1. Windows
2. macOS Base System / Install macOS / USB drive name
3. OpenShell.efi
4. Reset NVRAM

If some entries are hidden, press `Space`.

Use the arrow keys to choose the macOS installer or recovery entry, then press `Enter`.

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

The machine may reboot several times. Each time it turns off or restarts:

1. Press the boot-menu key again.
2. Choose the USB again.
3. In OpenCore, choose the macOS installer or installed macOS volume.
4. Continue until normal macOS setup appears.

{: .important }
Do not unplug the USB until post-install is complete. Your internal disk probably cannot boot by itself yet.
{% include step_nav.html %}
