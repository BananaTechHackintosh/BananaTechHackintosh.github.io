---
title: OpenCore Guide
nav_order: 2
has_children: true
description: Banana Tech's full Just-the-Docs OpenCore Hackintosh guide.
permalink: /guide.html
---

# Banana Tech OpenCore Guide

This guide is a searchable, step-by-step OpenCore workflow for compatible x86 PCs, rewritten for the web and updated with current OpenCore-era best practices.

{: .warning }
Hackintoshing is experimental. It only applies to compatible **x86 PCs**, can break after updates, and may conflict with Apple's macOS license terms. Back up everything before you begin.

## Start Here

Follow the guide in order:

1. [Before You Start]({{ '/docs/before-you-start.html' | relative_url }})
2. [Check Compatibility]({{ '/docs/check-compatibility.html' | relative_url }})
3. [Build the EFI]({{ '/docs/build-efi.html' | relative_url }})
4. [Map USB Ports]({{ '/docs/usb-mapping.html' | relative_url }})
5. [Clean `config.plist`]({{ '/docs/config-plist.html' | relative_url }})
6. [Create the Installer]({{ '/docs/create-installer.html' | relative_url }})
7. [Boot and Install macOS]({{ '/docs/boot-install.html' | relative_url }})
8. [Post-Install]({{ '/docs/post-install.html' | relative_url }})
9. [Troubleshooting]({{ '/docs/troubleshooting.html' | relative_url }})
10. [Tool Links]({{ '/docs/download-tools.html' | relative_url }})
11. [References and Updates]({{ '/docs/references.html' | relative_url }})

## What This Guide Covers

- A practical Windows-based path for building an OpenCore USB installer.
- Hardware compatibility checks before you erase or install anything.
- Starter EFI generation, USB mapping, and `config.plist` cleanup.
- Modern macOS recovery commands, including Sonoma, Sequoia, and Tahoe notes.
- Post-install EFI copy and first-pass hardware verification.

## Best Mindset

Treat tools as helpers, not magic buttons. If something does not match your hardware, pause and compare against Dortania before changing random settings.
