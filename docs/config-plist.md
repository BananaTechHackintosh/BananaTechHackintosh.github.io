---
title: Clean config.plist
parent: OpenCore Guide
nav_order: 5
description: Clean a Hackintosh OpenCore config.plist with ProperTree, refresh ACPI, kext, driver, and tool entries, and save the EFI config.
permalink: /docs/config-plist.html
keywords:
  - Hackintosh config.plist
  - OpenCore config.plist
  - ProperTree
  - OC Clean Snapshot
  - EFI config
prev_step:
  title: Map USB Ports
  url: /docs/usb-mapping.html
next_step:
  title: Create the Installer
  url: /docs/create-installer.html
---
# Clean `config.plist`

`config.plist` tells OpenCore what to load and how to behave. If you add or remove kexts, drivers, tools, or ACPI files, the config must match.

## Open ProperTree

1. Go to the ProperTree GitHub repository:
   - [ProperTree](https://github.com/corpnewt/ProperTree)
2. Click the green **Code** button.
3. Click **Download ZIP**.
4. Extract the ZIP.
5. Open the ProperTree folder.
6. On Windows, run `ProperTree.bat`.
7. If Windows blocks it, click **More info** or **Learn more**, then **Run anyway** only if you downloaded it from the real GitHub page.
8. You should see a blank Command Prompt window and the ProperTree window.
9. In ProperTree, open your EFI's `OC/config.plist`.

## Run OC Clean Snapshot

1. Press `Ctrl + R`.
2. Select your `EFI/OC` folder.
3. If ProperTree asks to remove duplicates, accept.
4. If it asks to add missing directories, accept.
5. Close the ProperTree window.
6. When it asks to save, click **Yes**.
7. Save the file as the default `config.plist` in your `EFI/OC` folder.

ProperTree's OC Snapshot walks ACPI, Kexts, Tools, and Drivers, then updates the matching config sections. OC Clean Snapshot starts fresh for those sections, which is usually better after adding USB maps or cleaning a generated EFI.

## What to Check After Snapshot

Open these sections and make sure they look reasonable:

- `ACPI -> Add`
- `Kernel -> Add`
- `Misc -> Tools`
- `UEFI -> Drivers`
- `NVRAM -> Add`
- `PlatformInfo -> Generic`

## Do Not Share Serial Numbers

If your config includes generated serial data, do not post it publicly. Blur or remove serial values before asking for help.
{% include step_nav.html %}
