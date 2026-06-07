---
title: Build the EFI
parent: OpenCore Guide
nav_order: 4
description: Build and save the starter EFI folder.
permalink: /docs/build-efi.html
prev_step:
  title: Download Tools
  url: /docs/download-tools.html
next_step:
  title: Map USB Ports
  url: /docs/usb-mapping.html
---
# Build the EFI

The EFI folder is the heart of the install. It contains OpenCore, drivers, kexts, ACPI patches, and your `config.plist`.

## Generate the Starter EFI

In OpCore Simplify:

1. Choose the macOS version you wrote down during compatibility checking.
2. Start the EFI build option.
3. If asked to scan Wi-Fi profiles, answer yes if you want the tool to detect networking information.
4. When asked for audio codec information, use the value recommended by the tool or your hardware research.
5. Let the tool finish.

## Save the Result

After the tool finishes:

1. Take a screenshot or phone photo of the final summary screen.
2. Open the OpCore Simplify folder.
3. Open the `Results` folder.
4. Copy the generated `EFI` folder into your project folder.

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
