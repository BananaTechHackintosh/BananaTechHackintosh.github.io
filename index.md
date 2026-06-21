---
title: Home
nav_order: 1
description: Beginner-friendly OpenCore Hackintosh documentation with EFI setup, USB mapping, installer preparation, troubleshooting, and support.
permalink: /
---

<div class="banana-hero" markdown="1">

<div class="banana-kicker">Banana Tech Hackintosh</div>

# Build a cleaner OpenCore Hackintosh

A terminal-styled, beginner-friendly OpenCore guide for compatible x86 PCs: check hardware, build an EFI, map USB ports, create a recovery installer, install macOS, and finish post-install safely.

<div class="banana-actions terminal-actions">
  <a class="btn btn-primary terminal-type" style="--type-chars: 15" href="{{ '/guide.html' | relative_url }}"><span class="terminal-text">Start the guide</span></a>
  <a class="btn terminal-type" style="--type-chars: 10" href="{{ '/docs/download-tools.html' | relative_url }}"><span class="terminal-text">Tool links</span></a>
  <a class="btn terminal-type" style="--type-chars: 16" href="{{ '/docs/create-installer.html' | relative_url }}"><span class="terminal-text">Create installer</span></a>
  <a class="btn terminal-type" style="--type-chars: 13" href="{{ '/docs/troubleshooting.html' | relative_url }}"><span class="terminal-text">Troubleshoot</span></a>
</div>

**Updated docs:** cleaner chapters, current tool notes, and a stronger troubleshooting flow.

</div>

## Choose Your Step

<div class="banana-grid">
  <div class="banana-card"><h3>1. Prep</h3><p>Collect hardware details, make a working folder, understand the risks, and get ready before touching disks.</p><p><a href="{{ '/docs/before-you-start.html' | relative_url }}">Before you start -></a></p></div>
  <div class="banana-card"><h3>2. Compatibility</h3><p>Install Python, download OpCore Simplify, run the hardware scan, and write down the supported macOS version.</p><p><a href="{{ '/docs/check-compatibility.html' | relative_url }}">Check compatibility -></a></p></div>
  <div class="banana-card"><h3>3. EFI</h3><p>Select the supported macOS version, build the starter EFI, and save the result screenshot.</p><p><a href="{{ '/docs/build-efi.html' | relative_url }}">Build the EFI -></a></p></div>
  <div class="banana-card"><h3>4. USB Map</h3><p>Download USBToolBox, follow the menu flow, build the USB map kext, and add it to your EFI.</p><p><a href="{{ '/docs/usb-mapping.html' | relative_url }}">Map USB ports -></a></p></div>
  <div class="banana-card"><h3>5. Config</h3><p>Download ProperTree, run OC Clean Snapshot, and save the updated `config.plist`.</p><p><a href="{{ '/docs/config-plist.html' | relative_url }}">Clean config.plist -></a></p></div>
  <div class="banana-card"><h3>6. Installer</h3><p>Download OpenCorePkg recovery files, format the USB with Rufus, and copy both required folders.</p><p><a href="{{ '/docs/create-installer.html' | relative_url }}">Create installer -></a></p></div>
  <div class="banana-card"><h3>7. Install</h3><p>Boot from USB, choose the macOS installer in OpenCore, format the target disk, and complete setup.</p><p><a href="{{ '/docs/boot-install.html' | relative_url }}">Boot and install -></a></p></div>
  <div class="banana-card"><h3>8. Finish</h3><p>Mount the internal EFI, copy your working EFI folder, reboot without USB, and save backups.</p><p><a href="{{ '/docs/post-install.html' | relative_url }}">Post-install -></a></p></div>
</div>

## Quick Notes

{: .warning }
This guide is for education and compatible x86 PCs. It is not a promise that every computer can run macOS.

{: .important }
For modern installs, USB mapping matters. Do not rely on `XhciPortLimit` for macOS 11.3 or newer.

## Ask Banana Tech a Question

Use the form below and include your CPU, GPU, motherboard or laptop model, BIOS version, target macOS version, and what you already tried.

<form class="contact-form" action="https://formspree.io/f/xkgzeaag" method="POST">
  <label for="name">Name</label>
  <input id="name" name="name" type="text" autocomplete="name" required>

  <label for="email">Email</label>
  <input id="email" name="email" type="email" autocomplete="email" required>

  <label for="question">Your question</label>
  <textarea id="question" name="question" rows="7" maxlength="2000" required></textarea>

  <input type="hidden" name="_subject" value="Banana Tech ? New Question">
  <input type="hidden" name="page" value="bananatechhackintosh.github.io">
  <input type="text" name="_gotcha" style="display:none">

  <button class="btn btn-primary" type="submit">Submit</button>
</form>
