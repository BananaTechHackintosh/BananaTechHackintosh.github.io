---
title: Create the Installer
parent: OpenCore Guide
nav_order: 7
description: Download macOS recovery files and prepare the USB installer.
permalink: /docs/create-installer.html
prev_step:
  title: Clean config.plist
  url: /docs/config-plist.html
next_step:
  title: Boot and Install macOS
  url: /docs/boot-install.html
---
# Create the Installer

This guide uses OpenCorePkg's `macrecovery.py` and Rufus to create a recovery installer from Windows.

## Download Recovery Files

1. Download the latest OpenCorePkg release.
2. Extract it.
3. Open `Utilities/macrecovery`.
4. Click the address bar in File Explorer, type `cmd`, and press Enter.
5. Run the command for your target macOS version.

Use `py` on Windows. If `py` does not work, try `python`.

```powershell
# Ventura (13)
py macrecovery.py -b Mac-B4831CEBD52A0C4C -m 00000000000000000 download

# Sonoma (14)
py macrecovery.py -b Mac-827FAC58A8FDFA22 -m 00000000000000000 download

# Sequoia (15)
py macrecovery.py -b Mac-7BA5B2D9E42DDD94 -m 00000000000000000 download

# Latest, currently Tahoe (26) in Dortania's guide
py macrecovery.py -b Mac-CFF7D910A743CAAF -m 00000000000000000 -os latest download
```

Older recovery commands are available in Dortania's installer guide and in OpenCorePkg's `macrecovery` data.

## Move the Recovery Folder

When the download finishes, you should get a folder named:

```text
com.apple.recovery.boot
```

Place it beside your `EFI` folder in your project folder ? not inside `EFI`.

Your project folder should look like:

```text
Hackintosh Project/
  EFI/
  com.apple.recovery.boot/
```

## Format the USB with Rufus

1. Open Rufus.
2. Select the correct USB drive.
3. Use a non-bootable/freeDOS-style format that creates a simple FAT32 volume.
4. Start the format.
5. Confirm that all USB data will be erased.

{: .warning }
Formatting deletes the USB contents. Double-check the selected drive.

## Copy Files to USB

After Rufus finishes:

1. Delete any placeholder files Rufus created.
2. Copy `EFI` to the USB root.
3. Copy `com.apple.recovery.boot` to the USB root.

The USB root should contain exactly these two folders for this workflow:

```text
EFI/
com.apple.recovery.boot/
```

Your USB is now bootable.
{% include step_nav.html %}
