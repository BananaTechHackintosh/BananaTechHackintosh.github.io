---
title: Check Compatibility
parent: OpenCore Guide
nav_order: 2
description: Use OpCore Simplify and compatibility checks to choose a target macOS version.
permalink: /docs/check-compatibility.html
prev_step:
  title: Before You Start
  url: /docs/before-you-start.html
next_step:
  title: Download Tools
  url: /docs/download-tools.html
---
# Check Compatibility

Use OpCore Simplify as the first compatibility checkpoint. Treat it as a helper ? not as the final authority.

## Use OpCore Simplify

1. Download OpCore Simplify from its GitHub repository.
2. Extract the ZIP.
3. Run the Windows batch file.
4. If Windows warns that the publisher is unknown, only continue if you downloaded it from the real project page.
5. If the tool asks to update, accept the update.
6. Choose the hardware compatibility option from the menu.
7. Let the scan finish.

## Read the Result

Look for **Supported macOS Version** under **Hardware Compatibility**.

Pick the newest macOS version shown as supported for your hardware. Write it down. You will use it when building the EFI and downloading recovery files.

## If Hardware Is Unsupported

If the tool says no compatible CPU, GPU, or other major component was found, stop and research before continuing.

Common blockers:

- Unsupported NVIDIA GPUs on modern macOS.
- Very new or very old iGPUs.
- Unsupported Wi-Fi/Bluetooth chipsets.
- Laptops with unusual trackpads, audio, or firmware behavior.
- AMD systems that need extra kernel patches.

## Reality Check

{: .warning }
No automated tool can guarantee success. If the result seems surprising, compare it with Dortania's OpenCore Install Guide for your CPU generation and GPU.

## Pick a Sensible Target

Newest is not always easiest. If your hardware supports multiple versions, choose the newest version that your GPU, networking, audio, and USB setup can realistically support.

For many builds, a stable current or one-version-back macOS target is less painful than chasing the newest beta-era behavior.
{% include step_nav.html %}
