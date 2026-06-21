---
title: Home
nav_order: 1
description: Beginner-friendly OpenCore Hackintosh documentation with EFI setup, USB mapping, installer preparation, troubleshooting, and support.
permalink: /
---

<div class="banana-hero" markdown="1">

<div class="banana-kicker">Banana Tech Hackintosh</div>

# How to Get macOS on a Compatible PC

A beginner-friendly OpenCore guide for compatible x86 PCs. Start with patience, check your hardware, build an EFI, map USB ports, create a recovery installer, install macOS, and finish post-install safely.

<div class="banana-actions">
  <a class="btn btn-primary" href="{{ '/guide.html' | relative_url }}">Start the guide</a>
  <a class="btn" href="{{ '/docs/create-installer.html' | relative_url }}">Create installer</a>
  <a class="btn" href="{{ '/docs/troubleshooting.html' | relative_url }}">Troubleshoot</a>
</div>

This web version keeps the PDF's simple step-by-step structure while adding search, links, and current OpenCore notes.

[Download the original PDF guide]({{ '/BananaTech-Hackintosh-Guide.pdf' | relative_url }})

</div>

## Choose Your Step

<div class="banana-grid">
  <div class="banana-card"><h3>1. Prep</h3><p>Collect hardware details, install Python, and understand the risks before touching disks.</p><p><a href="{{ '/docs/before-you-start.html' | relative_url }}">Before you start</a></p></div>
  <div class="banana-card"><h3>2. Compatibility</h3><p>Use OpCore Simplify and Dortania references to choose a sensible target macOS version.</p><p><a href="{{ '/docs/check-compatibility.html' | relative_url }}">Check compatibility</a></p></div>
  <div class="banana-card"><h3>3. EFI</h3><p>Generate the starter EFI, add your USB map, and clean the OpenCore config.</p><p><a href="{{ '/docs/build-efi.html' | relative_url }}">Build the EFI</a></p></div>
  <div class="banana-card"><h3>4. Installer</h3><p>Download macOS recovery files with OpenCorePkg and prepare the USB from Windows.</p><p><a href="{{ '/docs/create-installer.html' | relative_url }}">Create installer</a></p></div>
  <div class="banana-card"><h3>5. Install</h3><p>Boot OpenCore, enter recovery, format the target disk, and complete macOS setup.</p><p><a href="{{ '/docs/boot-install.html' | relative_url }}">Boot and install</a></p></div>
  <div class="banana-card"><h3>6. Finish</h3><p>Copy EFI to the internal disk, test hardware, and save a known-good backup.</p><p><a href="{{ '/docs/post-install.html' | relative_url }}">Post-install</a></p></div>
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

  <input type="hidden" name="_subject" value="Banana Tech - New Question">
  <input type="hidden" name="page" value="bananatechhackintosh.github.io">
  <input type="text" name="_gotcha" style="display:none">

  <button class="btn btn-primary" type="submit">Submit</button>
</form>
