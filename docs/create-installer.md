---
title: Create the Installer
parent: OpenCore Guide
nav_order: 6
description: Create a Hackintosh USB installer from Windows with OpenCorePkg macrecovery commands, Rufus, an EFI folder, and macOS recovery files.
permalink: /docs/create-installer.html
keywords:
  - Hackintosh USB installer
  - macrecovery.py
  - OpenCorePkg
  - Rufus Hackintosh USB
  - macOS recovery installer
  - com.apple.recovery.boot
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

1. Go to OpenCorePkg releases:
   - [OpenCorePkg releases](https://github.com/acidanthera/OpenCorePkg/releases)
2. Download the latest release ZIP.
3. Extract the ZIP.
4. Open the extracted OpenCorePkg folder.
5. Open `Utilities`.
6. Open `macrecovery`.
7. Click the File Explorer address bar at the top.
8. Type `cmd`.
9. Press `Enter`.
10. A Command Prompt window should open inside the `macrecovery` folder.
11. Run the command for your target macOS version.

Use `py` on Windows. If `py` does not work, try `python`.

```powershell
# Lion (10.7)
py macrecovery.py -b Mac-2E6FAB96566FE58C -m 00000000000F25Y00 download
py macrecovery.py -b Mac-C3EC7CD22292981F -m 00000000000F0HM00 download

# Mountain Lion (10.8)
py macrecovery.py -b Mac-7DF2A3B5E5D671ED -m 00000000000F65100 download

# Mavericks (10.9)
py macrecovery.py -b Mac-F60DEB81FF30ACF6 -m 00000000000FNN100 download

# Yosemite (10.10)
py macrecovery.py -b Mac-E43C1C25D4880AD6 -m 00000000000GDVW00 download

# El Capitan (10.11)
py macrecovery.py -b Mac-FFE5EF870D7BA81A -m 00000000000GQRX00 download

# Sierra (10.12)
py macrecovery.py -b Mac-77F17D7DA9285301 -m 00000000000J0DX00 download

# High Sierra (10.13)
py macrecovery.py -b Mac-7BA5B2D9E42DDD94 -m 00000000000J80300 download
py macrecovery.py -b Mac-BE088AF8C5EB4FA2 -m 00000000000J80300 download

# Mojave (10.14)
py macrecovery.py -b Mac-7BA5B2DFE22DDD8C -m 00000000000KXPG00 download

# Catalina (10.15)
py macrecovery.py -b Mac-CFF7D910A743CAAF -m 00000000000PHCD00 download
py macrecovery.py -b Mac-00BE6ED71E35EB86 -m 00000000000000000 download

# Big Sur (11)
py macrecovery.py -b Mac-2BD1B31983FE1663 -m 00000000000000000 download

# Monterey (12)
py macrecovery.py -b Mac-E43C1C25D4880AD6 -m 00000000000000000 download

# Ventura (13)
py macrecovery.py -b Mac-B4831CEBD52A0C4C -m 00000000000000000 download

# Sonoma (14)
py macrecovery.py -b Mac-827FAC58A8FDFA22 -m 00000000000000000 download

# Sequoia (15)
py macrecovery.py -b Mac-7BA5B2D9E42DDD94 -m 00000000000000000 download

# Tahoe (26) / latest
py macrecovery.py -b Mac-CFF7D910A743CAAF -m 00000000000000000 -os latest download
```

These commands come from OpenCorePkg's `macrecovery` data. If OpenCorePkg changes the list later, use the current `recovery_urls.txt` in the OpenCorePkg `Utilities/macrecovery` folder as the source of truth.

## Move the Recovery Folder

When the download finishes, you should get a folder named:

```text
com.apple.recovery.boot
```

Open the OpenCorePkg `Utilities/macrecovery` folder again and find `com.apple.recovery.boot`.

Place it beside your `EFI` folder in your project folder, not inside `EFI`.

Your project folder should look like:

```text
Hackintosh Project/
  EFI/
  com.apple.recovery.boot/
```

## Format the USB with Rufus

1. Go to Rufus:
   - [Rufus](https://rufus.ie/)
2. Scroll down to the download section.
3. Download the latest x86/x64 Windows release.
4. Open Rufus.
5. If Windows asks for permission to allow changes, click **Yes**.
6. At the top, select your USB drive.
7. Double-check the selected drive. It must be the USB, not another disk.
8. Use a non-bootable/freeDOS-style format that creates a simple FAT32 volume.
9. Start the format.
10. Confirm that all USB data will be erased.

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
