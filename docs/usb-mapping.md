---
title: Map USB Ports
parent: OpenCore Guide
nav_order: 4
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
4. If Windows blocks it, choose **Learn more** and only continue if you downloaded it from the real project page.

## Follow the USBToolBox Menu Flow

The PDF's flow is:

1. Type `D` and press `Enter` to discover ports.
2. Wait a moment.
3. Type `B` and press `Enter` to go back.
4. Type `C` and press `Enter` to configure ports.
5. Type `N` and press `Enter`.
6. Type `B` and press `Enter` to go back.
7. Type `S` and press `Enter` to select ports.
8. Choose the ports you actually use.
9. Adjust port types if needed.
10. Type `K` and press `Enter` to build the kext.

If USBToolBox asks for a model identifier because legacy class is enabled, use the exact model identifier from your OpCore Simplify summary screenshot.

{: .note }
USBToolBox says Windows can usually infer companion ports, so one USB 3 device may be enough for USB 3 ports. On macOS, you typically need both USB 2 and USB 3 devices for each USB 3 port.

## Add the Kext

After USBToolBox builds the map:

1. Copy the generated `.kext` folder from the path USBToolBox shows.
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
