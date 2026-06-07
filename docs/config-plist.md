---
title: Clean config.plist
parent: OpenCore Guide
nav_order: 6
description: Use ProperTree to refresh OpenCore config entries.
permalink: /docs/config-plist.html
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

1. Download ProperTree.
2. Extract it.
3. On Windows, run `ProperTree.bat`.
4. Open your EFI's `OC/config.plist`.

## Run OC Clean Snapshot

1. Press `Ctrl + R`.
2. Select your `EFI/OC` folder.
3. If ProperTree asks to remove duplicates, accept.
4. If it asks to add missing directories, accept.
5. Save the file.

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
