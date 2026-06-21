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

1. Go to the USBToolBox GitHub repository:
   - [USBToolBox](https://github.com/USBToolBox/tool)
2. Click **Releases** on the right side of the page.
3. Download the latest `Windows.exe`.
4. If your browser blocks the file, choose the option to keep or download anyway only if you are on the real GitHub page.
5. Run `Windows.exe`.
6. If Windows blocks it, choose **Learn more** or **More info**.
7. Click **Run anyway** only if you downloaded it from the real project page.

## Follow the USBToolBox Menu Flow

The PDF's flow is:

1. Type `D` and press `Enter` to discover ports.
2. Wait a moment for the port discovery screen to load.
3. Type `B` and press `Enter` to go back.
4. Type `C` and press `Enter` to configure ports.
5. Type `N` and press `Enter`.
6. Type `B` and press `Enter` to go back.
7. Type `S` and press `Enter` to select ports.
8. Choose the ports you actually use.
9. Adjust port types if needed.
10. Type `K` and press `Enter` to build the kext.

If USBToolBox asks for a model identifier because legacy class is enabled, use the exact model identifier from your OpCore Simplify summary screenshot.

Type the model identifier exactly. Do not add quotation marks.

{: .note }
USBToolBox says Windows can usually infer companion ports, so one USB 3 device may be enough for USB 3 ports. On macOS, you typically need both USB 2 and USB 3 devices for each USB 3 port.

## Add the Kext

After USBToolBox builds the map:

1. Copy the generated file path USBToolBox shows.
2. Open File Explorer.
3. Paste that path into the File Explorer address bar.
4. Press `Enter`.
5. Copy the generated `.kext` folder.
6. Open your working `EFI` folder.
7. Open `EFI/OC/Kexts`.
8. Paste the generated `.kext` folder there.
9. If the map uses USBToolBox.kext, also add the matching USBToolBox kext release.
10. Remove `UTBDefault.kext` if it is present.
11. Update `config.plist` with ProperTree's OC Clean Snapshot.

## Common Mistake

If you ever see `EFI/OC/Kekts`, treat it as a typo. The correct folder is:

```text
EFI/OC/Kexts
```

## macOS 11.3 and Newer

Dortania warns that `XhciPortLimit` is broken on macOS 11.3 and newer. For modern macOS, map USB ports properly instead of relying on that quirk.
{% include step_nav.html %}
