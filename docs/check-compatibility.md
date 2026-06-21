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
  title: Build the EFI
  url: /docs/build-efi.html
---
# Check Compatibility

Use OpCore Simplify as the first compatibility checkpoint. Treat it as a helper, not as the final authority.

## Install Python First

Before opening OpCore Simplify, install Python from the official Python website. Several OpenCore tools use Python scripts, so do this first.

## Download and Open OpCore Simplify

1. Download OpCore Simplify from its GitHub repository.
2. Extract the ZIP.
3. Open the extracted folder.
4. Run the Windows batch file for OpCore Simplify.
5. If Windows warns that the publisher is unknown, only continue if you downloaded it from the real project page.
6. If the tool asks to update, type `y` and press `Enter`.

The app opens in a Command Prompt window. That is normal.

## Run the Hardware Scan

1. From the main menu, type `1` and press `Enter`.
2. On the next screen, type `E` and press `Enter` to continue.
3. Wait for the scan to finish.

The scan should show your computer components and the macOS versions your hardware can support.

## Read the Result

After the scan finishes:

1. Press `Enter` to return to the main menu.
2. Look near the top for **Hardware Compatibility**.
3. Find **Supported macOS Version**.
4. Write down the newest supported macOS version listed there.

You will use that version in the next step when building the EFI and later when downloading recovery files.

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
