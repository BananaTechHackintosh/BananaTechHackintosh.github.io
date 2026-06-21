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

Before opening OpCore Simplify, install Python from the official Python website:

- [Download Python](https://www.python.org/downloads/)

Several OpenCore tools use Python scripts, so do this first.

When installing Python on Windows:

1. Open the Python installer.
2. Turn on **Add python.exe to PATH** if the installer shows that option.
3. Click **Install Now**.
4. Wait for the installer to finish.
5. Close the installer.

## Download and Open OpCore Simplify

1. Go to the OpCore Simplify GitHub repository:
   - [OpCore Simplify](https://github.com/lzhoang2801/OpCore-Simplify)
2. Click the green **Code** button.
3. Click **Download ZIP**.
4. Open your Downloads folder.
5. Right-click the downloaded ZIP.
6. Click **Extract All**.
7. Open the extracted OpCore Simplify folder.
8. Look for the Windows batch or command file for OpCore Simplify.
9. Double-click it.
10. If Windows warns that the publisher is unknown, click **More info** or **Learn more**.
11. Click **Run anyway** only if you downloaded it from the real GitHub page.
12. If the tool asks to update, type `y` and press `Enter`.

The app opens in a Command Prompt window. That is normal.

## Run the Hardware Scan

1. From the main menu, type `1` and press `Enter`.
2. On the next screen, type `E` and press `Enter` to continue.
3. Wait for the scan to finish.

The scan should show your computer components and the macOS versions your hardware can support.

Do not close the window yet. You still need the result.

## Read the Result

After the scan finishes:

1. Press `Enter` to return to the main menu.
2. Look near the top for **Hardware Compatibility**.
3. Find **Supported macOS Version**.
4. Write down the newest supported macOS version listed there.

You will use that version in the next step when building the EFI and later when downloading recovery files.

If you are not sure what to write down, take a screenshot or phone photo of the result screen before continuing.

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
