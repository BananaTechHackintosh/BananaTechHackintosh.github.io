---
title: Tool Links
parent: OpenCore Guide
nav_order: 10
description: Tools used by the Banana Tech OpenCore workflow.
permalink: /docs/download-tools.html
prev_step:
  title: Troubleshooting
  url: /docs/troubleshooting.html
next_step:
  title: References and Updates
  url: /docs/references.html
---
# Tool Links

This page is a tool list, not a required step in the middle of the guide. The main guide tells you when to use each tool.

## Required Tools

| Tool | Purpose |
| --- | --- |
| Python | Runs OpenCore helper scripts and ProperTree. |
| OpCore Simplify | Beginner-friendly hardware scan and starter EFI generation. |
| USBToolBox | Maps USB ports and builds a USB map kext. |
| ProperTree | Edits and snapshots `config.plist`. |
| OpenCorePkg | Provides OpenCore files and `macrecovery.py`. |
| Rufus | Formats the USB drive from Windows. |

## Recommended Download Links

- [Python](https://www.python.org/downloads/)
- [Dortania OpenCore Install Guide](https://dortania.github.io/OpenCore-Install-Guide/)
- [OpenCorePkg releases](https://github.com/acidanthera/OpenCorePkg/releases)
- [USBToolBox](https://github.com/USBToolBox/tool)
- [ProperTree](https://github.com/corpnewt/ProperTree)
- [Rufus](https://rufus.ie/)

## Download Safety

- Prefer official GitHub release pages.
- Avoid random reuploads.
- Be suspicious of password-protected ZIP files.
- If Windows Defender warns you, verify the project URL and file name before running anything.

## Why These Tools

This workflow is useful because it lets a Windows user build most of the installer without already owning a Mac. OpenCore changes over time, so current upstream docs still matter.
{% include step_nav.html %}
