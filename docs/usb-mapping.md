---
title: Map USB Ports
parent: OpenCore Guide
nav_order: 5
description: Use USBToolBox to create a USB map kext for the EFI.
permalink: /docs/usb-mapping.html
prev_step:
  title: Build the EFI
  url: /docs/build-efi.html
next_step:
  title: Clean config.plist
  url: /docs/config-plist.html
---
# Map USB Ports

USB mapping matters because macOS has port limits and expects USB ports to be described correctly. Bad USB mapping can cause broken ports, installer failures, Bluetooth issues, sleep problems, or random instability.

## Use USBToolBox on Windows

1. Download USBToolBox.
2. Prefer the latest `Windows.exe` from releases, or use `Windows.zip` if antivirus blocks the self-extractor.
3. Run the tool.
4. Choose **Discover Ports**.
5. Plug a USB device into each physical port and wait for it to appear before moving to the next one.
6. Go to **Select Ports**.
7. Select the ports you actually use.
8. Adjust port types if needed.
9. Press `K` to build the kext.

{: .note }
USBToolBox says Windows can usually infer companion ports, so one USB 3 device may be enough for USB 3 ports. On macOS, you typically need both USB 2 and USB 3 devices for each USB 3 port.

## Add the Kext

After USBToolBox builds the map:

1. Copy the generated `.kext` folder.
2. Paste it into `EFI/OC/Kexts`.
3. If the map uses USBToolBox.kext, also add the matching USBToolBox kext release.
4. Remove `UTBDefault.kext` if it is present.
5. Update `config.plist` with ProperTree's OC Clean Snapshot.

## Common Mistake

If you ever see `EFI/OC/Kekts`, treat it as a typo. The correct folder is:

```text
EFI/OC/Kexts
```

## macOS 11.3 and Newer

Dortania warns that `XhciPortLimit` is broken on macOS 11.3 and newer. For modern macOS, map USB ports properly instead of relying on that quirk.
{% include step_nav.html %}
