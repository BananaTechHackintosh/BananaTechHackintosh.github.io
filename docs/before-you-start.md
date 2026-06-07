---
title: Before You Start
parent: OpenCore Guide
nav_order: 1
description: Requirements, warnings, and setup notes before beginning a Hackintosh install.
permalink: /docs/before-you-start.html
next_step:
  title: Check Compatibility
  url: /docs/check-compatibility.html
---
# Before You Start

Start with the most important truth: you need patience. A Hackintosh install can take a long time, and errors are normal.

## Requirements

You need:

- A compatible x86 desktop or laptop.
- A 16 GB or larger USB drive.
- Reliable internet.
- Ethernet if possible, especially during recovery install.
- A Windows install for the beginner-friendly workflow in this guide.
- Python installed on Windows.
- Time to read, test, reboot, and troubleshoot.

{: .important }
For modern USB mapping, use **Windows 10 or Windows 11 64-bit** when possible. USBToolBox says Windows 10/11 64-bit is recommended, Windows 8 may work, Windows 7 and below are likely to crash, and 32-bit Windows is not supported.

## What You Should Record

Before downloading anything, write down:

- CPU model.
- GPU model, including iGPU and dGPU.
- Motherboard or laptop model.
- BIOS/UEFI version.
- Ethernet chipset.
- Wi-Fi and Bluetooth chipset.
- Storage type: SATA, NVMe, or both.
- Target macOS version.

## Safety Checklist

- Back up important files.
- Do not erase a disk unless you know exactly which disk it is.
- Keep a copy of your working EFI folder on another drive.
- Do not assume one EFI works on every computer.
- Use this guide as a beginner path, but cross-check with Dortania when something does not match your hardware.

## What OpenCore Does

OpenCore is the bootloader. It prepares your PC so macOS can boot by loading ACPI patches, kexts, drivers, boot arguments, and SMBIOS data.

This guide helps you build a practical starter EFI, but the best long-term Hackintosh is one you understand.
{% include step_nav.html %}
