---
title: Troubleshooting
parent: OpenCore Guide
nav_order: 10
description: Common OpenCore install problems and next steps.
permalink: /docs/troubleshooting.html
prev_step:
  title: Post-Install
  url: /docs/post-install.html
next_step:
  title: References and Updates
  url: /docs/references.html
---
# Troubleshooting

Hackintosh troubleshooting is mostly careful observation. Do not randomly toggle settings without writing down what changed.

## Start With Verbose Mode

If you are stuck at boot, enable verbose mode by adding this boot argument:

```text
-v
```

The text on screen helps identify where boot stops.

## USB Does Not Boot

Check:

- USB contains `EFI` and `com.apple.recovery.boot` at the root.
- BIOS is set to UEFI mode.
- Secure Boot is disabled.
- The USB was formatted correctly.
- `EFI/BOOT/BOOTx64.efi` exists.

## OpenCore Picker Missing Entries

Try pressing `Space` to show auxiliary entries. Also check `Misc -> Boot` settings in `config.plist`.

## Installer Has No Internet

Use ethernet if possible. If ethernet does not work, confirm your NIC chipset and kext.

## Boot Loops

Common causes:

- Wrong SMBIOS.
- Missing or mismatched kexts.
- Incorrect ACPI patches.
- Bad USB map.
- Unsupported macOS version for the hardware.
- Broken `XhciPortLimit` assumptions on macOS 11.3+.

## Black Screen

Common causes:

- Unsupported GPU.
- Wrong iGPU platform ID.
- Display connected to an unsupported output.
- Missing WhateverGreen settings.

## Kernel Panic

Take a photo of the panic text. Search the exact last lines and compare with Dortania's troubleshooting sections.

## When to Stop and Rebuild

Rebuild the EFI from scratch if:

- You copied a random EFI from another computer.
- You no longer know what was changed.
- ProperTree snapshot entries do not match the files in `OC`.
- The config was generated for the wrong macOS version or hardware.

## Where to Get Help

When asking for help, include:

- Hardware specs.
- Target macOS version.
- OpenCore version.
- Photos of verbose errors.
- A redacted config or EFI tree.
- What you already tried.
{% include step_nav.html %}
