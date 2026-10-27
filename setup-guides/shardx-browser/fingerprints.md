---
description: The device fingerprint library in ShardBrowser
icon: fingerprint
---

# Fingerprints

<mark style="color:purple;">**Fingerprints**</mark> is the library of real-device fingerprints that ShardBrowser builds profiles from. Each fingerprint describes a specific machine: operating system, Chrome version, graphics card, screen, CPU cores and memory.

At the top are the system filters: <mark style="color:purple;">**All**</mark>, <mark style="color:purple;">**macOS**</mark>, <mark style="color:purple;">**Windows**</mark>, <mark style="color:purple;">**Linux**</mark> and <mark style="color:purple;">**Android**</mark>, plus extra <mark style="color:purple;">**Filters**</mark> and search. Each fingerprint card shows the screen resolution, the number of cores and the Chrome version.

<figure>
  <picture>
    <source srcset="../../.gitbook/assets/shardbrowser-fingerprints-list_black.png" media="(prefers-color-scheme: dark)">
    <img src="../../.gitbook/assets/shardbrowser-fingerprints-list_white.png" alt="Fingerprints section">
  </picture>
  <figcaption>Fingerprints section</figcaption>
</figure>

The <mark style="color:purple;">**GPU mismatch**</mark> tag means the fingerprint claims a graphics card your computer doesn't have. Such a profile works, but the browser can't deliver some of the WebGL and WebGPU features the fingerprint claims. The fingerprint card explains this in detail in the <mark style="color:purple;">**This computer**</mark> block.

Click a fingerprint to open its card. The <mark style="color:purple;">**Details**</mark> block lists the OS, Chrome version, graphics card, screen, cores, memory and <mark style="color:purple;">User agent</mark>. <mark style="color:purple;">**New profile**</mark> creates a profile straight from this fingerprint.

<figure>
  <picture>
    <source srcset="../../.gitbook/assets/shardbrowser-fingerprint-details_black.png" media="(prefers-color-scheme: dark)">
    <img src="../../.gitbook/assets/shardbrowser-fingerprint-details_white.png" alt="Fingerprint card and New profile button">
  </picture>
  <figcaption>Fingerprint card and New profile button</figcaption>
</figure>
