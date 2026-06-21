---
title: Build the EFI
parent: OpenCore Guide
nav_order: 3
description: Build and save the starter EFI folder.
permalink: /docs/build-efi.html
prev_step:
  title: Check Compatibility
  url: /docs/check-compatibility.html
next_step:
  title: Map USB Ports
  url: /docs/usb-mapping.html
---
# Build the EFI

The EFI folder is the heart of the install. It contains OpenCore, drivers, kexts, ACPI patches, and your `config.plist`.

## Select the macOS Version

In OpCore Simplify:

1. Return to the main menu.
2. Type `2` and press `Enter`.
3. Select the macOS version you wrote down during compatibility checking.
4. Type the number beside that macOS version.
5. Press `Enter`.

For example, if the list says `21. macOS 15 Sequoia`, type `21` and press `Enter`.

## Generate the Starter EFI

After selecting the macOS version:

1. Return to the main menu.
2. Type `6` and press `Enter` to build the EFI.
3. If asked to scan Wi-Fi profiles, type `y` and press `Enter` if you want the tool to detect networking information.
4. When asked for audio codec information, use the value recommended by the tool or your hardware research.
5. Let the tool finish.

{: .note }
The original PDF used codec ID `13` as an example. Do not blindly use `13` for every computer. Use the value that matches your hardware.

## Save the Result

After the tool finishes:

1. Take a screenshot or phone photo of the final summary screen.
2. Keep that screenshot. You may need the model identifier later for USBToolBox.
3. Open File Explorer.
4. Make a working folder if you have not already, such as `MacOS Stuff` or `Hackintosh Project`.
5. Open the OpCore Simplify folder.
6. Open the `Results` folder.
7. Find the generated `EFI` folder.
8. Copy the generated `EFI` folder into your working folder.

Do not lose the screenshot. It can include model identifier or SMBIOS information you may need later.

## EFI Folder Layout

A typical OpenCore EFI looks like this:

```text
EFI/
  BOOT/
    BOOTx64.efi
  OC/
    ACPI/
    Drivers/
    Kexts/
    Resources/
    Tools/
    OpenCore.efi
    config.plist
```

## Do Not Mix Random EFIs

A prebuilt EFI from another computer can boot badly, break sleep, disable devices, or expose invalid serial information. Use your own hardware data whenever possible.
{% include step_nav.html %}
