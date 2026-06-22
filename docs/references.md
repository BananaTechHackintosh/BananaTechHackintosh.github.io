---
title: References and Updates
parent: OpenCore Guide
nav_order: 11
description: Hackintosh and OpenCore reference links used to keep the Banana Tech guide current, including Dortania, OpenCorePkg, USBToolBox, ProperTree, and Rufus.
permalink: /docs/references.html
keywords:
  - Hackintosh references
  - OpenCore references
  - Dortania guide
  - OpenCorePkg
  - Hackintosh updates
prev_step:
  title: Tool Links
  url: /docs/download-tools.html
---
# References and Updates

Current upstream references should win whenever details change.

## Primary References

- [Dortania OpenCore Install Guide](https://dortania.github.io/OpenCore-Install-Guide/)
- [Dortania macOS 26 Tahoe notes](https://dortania.github.io/OpenCore-Install-Guide/extras/tahoe.html)
- [Dortania installer guide with macrecovery commands](https://dortania.github.io/OpenCore-Install-Guide/installer-guide/linux-install.html)
- [OpenCorePkg releases](https://github.com/acidanthera/OpenCorePkg/releases)
- [USBToolBox](https://github.com/USBToolBox/tool)
- [ProperTree](https://github.com/corpnewt/ProperTree)
- [Rufus](https://rufus.ie/)
- [Python downloads](https://www.python.org/downloads/)

## Updated Notes

- Dortania's guide currently lists OpenCore guide support around OpenCore 1.0.6, while OpenCorePkg releases may be newer. If there is a mismatch, use the latest stable release only after checking the matching docs and config sample.
- Dortania includes macOS 26 Tahoe-specific notes. Tahoe has extra caveats around audio, SMBIOS support, Wi-Fi, Bluetooth, OTA updates, and WhateverGreen on some AMD GPU setups.
- USBToolBox recommends Windows 10/11 64-bit for the full Windows feature set.
- ProperTree's OC Snapshot and OC Clean Snapshot are still useful for keeping `config.plist` aligned with the files inside `EFI/OC`.

## Guide Map

The guide is organized across these docs pages:

- Prerequisites and beginner warnings: [Before You Start]({{ '/docs/before-you-start.html' | relative_url }})
- OpCore Simplify compatibility: [Check Compatibility]({{ '/docs/check-compatibility.html' | relative_url }})
- Tool downloads: [Download Tools]({{ '/docs/download-tools.html' | relative_url }})
- EFI generation: [Build the EFI]({{ '/docs/build-efi.html' | relative_url }})
- USBToolBox flow: [Map USB Ports]({{ '/docs/usb-mapping.html' | relative_url }})
- ProperTree flow: [Clean config.plist]({{ '/docs/config-plist.html' | relative_url }})
- macrecovery and Rufus: [Create the Installer]({{ '/docs/create-installer.html' | relative_url }})
- Boot picker and recovery install: [Boot and Install macOS]({{ '/docs/boot-install.html' | relative_url }})
- Internal EFI copy: [Post-Install]({{ '/docs/post-install.html' | relative_url }})
{% include step_nav.html %}
