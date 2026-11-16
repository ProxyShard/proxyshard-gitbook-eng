---
description: Installation, setup, and features of the ShardBrowser anti-detect browser
icon: browser
---

# ShardBrowser

<figure>
  <picture>
    <source srcset="../.gitbook/assets/shardbrowser-cover_black.svg" media="(prefers-color-scheme: dark)">
    <img src="../.gitbook/assets/shardbrowser-cover_white.svg" alt="ShardBrowser logo">
  </picture>
</figure>

{% hint style="info" %}
ShardBrowser is a Chromium-based anti-detect browser by the ShardX team. Every profile gets its own fingerprint of a real device and its own proxy, so websites see your profiles as different computers. The program is free and provided "as is". If you run into a serious issue, please file a bug report on [GitHub](https://github.com/ProxyShard/ShardBrowser/issues).
{% endhint %}

Official ShardBrowser website: [shardbrowser.com](https://shardbrowser.com/).

<figure><img src="../.gitbook/assets/shardbrowser-website.png" alt="Official ShardBrowser website"><figcaption>Official ShardBrowser website</figcaption></figure>

## Installation and setup

### Windows system requirements

| Component      | Minimum                                | Recommended                                  |
| -------------- | -------------------------------------- | -------------------------------------------- |
| OS             | Windows 10 22H2 or Windows 11, 64-bit  | Windows 11 64-bit                            |
| Architecture   | x64 / x86\_64                          | x64                                          |
| CPU            | Dual-core 64-bit with SSE3 support     | Quad-core or better                          |
| RAM            | 4 GB                                   | 8 GB (16 GB when running many profiles)      |
| Disk space     | 1 GB                                   | 5 GB or more                                 |
| Runtime        | Microsoft Edge WebView2                | Latest version                               |

---

### Installing on Windows

Download the latest version:

{% embed url="https://github.com/ProxyShard/ShardBrowser/releases/latest" %}

Under <mark style="color:purple;">**Assets**</mark>, pick the installer <mark style="color:purple;">`ShardBrowser.Launcher_<version>_x64-setup.exe`</mark>. If you need a version that runs without installation, download <mark style="color:purple;">`ShardBrowser-Launcher-portable-win-x64.exe`</mark>.

<figure>
  <picture>
    <source srcset="../.gitbook/assets/shardbrowser-github-release-assets_black.png" media="(prefers-color-scheme: dark)">
    <img src="../.gitbook/assets/shardbrowser-github-release-assets_white.png" alt="Pick x64-setup.exe under Assets">
  </picture>
  <figcaption>Pick x64-setup.exe under Assets</figcaption>
</figure>

Run the downloaded file. <mark style="color:purple;">Windows SmartScreen</mark> may show a warning. Click <mark style="color:purple;">**More info**</mark>, then <mark style="color:purple;">**Run anyway**</mark>.

<figure>
  <picture>
    <source srcset="../.gitbook/assets/shardbrowser-windows-smartscreen_black.png" media="(prefers-color-scheme: dark)">
    <img src="../.gitbook/assets/shardbrowser-windows-smartscreen_white.png" alt="SmartScreen: click Run anyway">
  </picture>
  <figcaption>SmartScreen: click Run anyway</figcaption>
</figure>

### Installing on macOS

Under <mark style="color:purple;">**Assets**</mark>, download <mark style="color:purple;">`ShardBrowser.Launcher_<version>_aarch64.dmg`</mark>. This build supports Macs with Apple Silicon processors.

Open the `.dmg` file and drag <mark style="color:purple;">**ShardBrowser Launcher**</mark> to <mark style="color:purple;">**Applications**</mark>. The app is signed with an Apple Developer ID and notarized, so it opens like any other macOS app.

### Installing on Linux

The <mark style="color:purple;">**Assets**</mark> section provides `.AppImage`, `.deb` and `.rpm` builds. To run the AppImage, make it executable:

```bash
chmod +x ShardBrowser.Launcher_<version>_amd64.AppImage
./ShardBrowser.Launcher_<version>_amd64.AppImage
```

Install the `.deb` package with:

```bash
sudo apt install ./ShardBrowser.Launcher_<version>_amd64.deb
```

### First launch

After installation and launch, the <mark style="color:purple;">**All profiles**</mark> home screen opens. The section menu is on the left: profiles, proxies, fingerprints, extensions, bookmarks, automation and your ShardX account.

<figure>
  <picture>
    <source srcset="../.gitbook/assets/shardbrowser-profiles-empty_black.png" media="(prefers-color-scheme: dark)">
    <img src="../.gitbook/assets/shardbrowser-profiles-empty_white.png" alt="ShardBrowser home screen">
  </picture>
  <figcaption>ShardBrowser home screen</figcaption>
</figure>

---

### Adding a proxy

Go to <mark style="color:purple;">**Proxies**</mark> and click <mark style="color:purple;">**+ Add proxies**</mark>.

<figure>
  <picture>
    <source srcset="../.gitbook/assets/shardbrowser-proxies-empty_black.png" media="(prefers-color-scheme: dark)">
    <img src="../.gitbook/assets/shardbrowser-proxies-empty_white.png" alt="Proxies section">
  </picture>
  <figcaption>Proxies section</figcaption>
</figure>

In the <mark style="color:purple;">**Add proxies**</mark> window, choose the type in <mark style="color:purple;">**Type for lines without one**</mark> (<mark style="color:purple;">SOCKS5</mark> by default) and paste your proxies, one per line. Supported formats:

```
host:port
host:port:user:pass
user:pass@host:port
socks5://user:pass@host:port
```

Lines starting with `#` are ignored. Proxies you already have (same type, host, port, username and password) are skipped.

<figure>
  <picture>
    <source srcset="../.gitbook/assets/shardbrowser-add-proxies-paste_black.png" media="(prefers-color-scheme: dark)">
    <img src="../.gitbook/assets/shardbrowser-add-proxies-paste_white.png" alt="Paste one proxy per line and click Preview">
  </picture>
  <figcaption>Paste one proxy per line and click Preview</figcaption>
</figure>

Click <mark style="color:purple;">**Preview**</mark>. In the preview window, click <mark style="color:purple;">**Test all**</mark> to check the proxies before adding them. After the test every proxy gets a status and a country.

<figure>
  <picture>
    <source srcset="../.gitbook/assets/shardbrowser-add-proxies-preview_black.png" media="(prefers-color-scheme: dark)">
    <img src="../.gitbook/assets/shardbrowser-add-proxies-preview_white.png" alt="Click Test all, then Add 1 proxy">
  </picture>
  <figcaption>Click Test all, then Add 1 proxy</figcaption>
</figure>

Proxies marked <mark style="color:purple;">**UDP**</mark> support <mark style="color:purple;">SOCKS5 UDP</mark> and therefore <mark style="color:purple;">WebRTC</mark>, which matters a lot against serious anti-fraud systems. Without the <mark style="color:purple;">**UDP**</mark> mark the profile switches to <mark style="color:purple;">**TCP-only**</mark> mode: your IP won't leak, but the traffic may look suspicious to advanced anti-fraud systems. We strongly recommend [proxies with UDP support](about-udp/).

<mark style="color:purple;">**Select working only**</mark> keeps only the working proxies selected. Click <mark style="color:purple;">**Add 1 proxy**</mark> - the proxy appears in the list.

---

### Creating your first profile

Go to <mark style="color:purple;">**All profiles**</mark> and click <mark style="color:purple;">**+ New profile**</mark>. You can also import a profile from the clipboard with <mark style="color:purple;">**Import from clipboard**</mark>.

<figure>
  <picture>
    <source srcset="../.gitbook/assets/shardbrowser-new-profile-button_black.png" media="(prefers-color-scheme: dark)">
    <img src="../.gitbook/assets/shardbrowser-new-profile-button_white.png" alt="All profiles section">
  </picture>
  <figcaption>All profiles section</figcaption>
</figure>

The <mark style="color:purple;">**New profile**</mark> window opens with the <mark style="color:purple;">**Basics**</mark>, <mark style="color:purple;">**Proxy**</mark>, <mark style="color:purple;">**Fingerprint**</mark> and <mark style="color:purple;">**Extensions**</mark> tabs. On <mark style="color:purple;">**Basics**</mark>, enter a profile name. Here you can also pick a folder, tags and a color, add a note and load a cookies file.

<figure>
  <picture>
    <source srcset="../.gitbook/assets/shardbrowser-new-profile-basics_black.png" media="(prefers-color-scheme: dark)">
    <img src="../.gitbook/assets/shardbrowser-new-profile-basics_white.png" alt="Enter the profile name">
  </picture>
  <figcaption>Enter the profile name</figcaption>
</figure>

On the <mark style="color:purple;">**Proxy**</mark> tab, pick a saved proxy from the list. <mark style="color:purple;">**+ Add a new proxy**</mark> lets you add a new one right away.

<figure>
  <picture>
    <source srcset="../.gitbook/assets/shardbrowser-new-profile-proxy_black.png" media="(prefers-color-scheme: dark)">
    <img src="../.gitbook/assets/shardbrowser-new-profile-proxy_white.png" alt="Pick a proxy for the profile">
  </picture>
  <figcaption>Pick a proxy for the profile</figcaption>
</figure>

You don't have to change anything on the <mark style="color:purple;">**Fingerprint**</mark> tab - ShardBrowser picks a fingerprint for the chosen OS by itself. If you want, choose the <mark style="color:purple;">operating system</mark> (macOS, Windows, Linux, Android), a specific fingerprint, the graphics card, CPU cores, memory, refresh rate and screen resolution.

<figure>
  <picture>
    <source srcset="../.gitbook/assets/shardbrowser-new-profile-fingerprint_black.png" media="(prefers-color-scheme: dark)">
    <img src="../.gitbook/assets/shardbrowser-new-profile-fingerprint_white.png" alt="Profile fingerprint settings">
  </picture>
  <figcaption>Profile fingerprint settings</figcaption>
</figure>

Click <mark style="color:purple;">**Create profile**</mark>.

---

### Launching a profile

The profile appears in the list. The profile card opens on the right: proxy, extensions, notes, fingerprint settings, timezone and language (taken from the proxy by default). Click <mark style="color:purple;">**Start**</mark>.

<figure>
  <picture>
    <source srcset="../.gitbook/assets/shardbrowser-profile-start_black.png" media="(prefers-color-scheme: dark)">
    <img src="../.gitbook/assets/shardbrowser-profile-start_white.png" alt="Click Start to launch the profile">
  </picture>
  <figcaption>Click Start to launch the profile</figcaption>
</figure>

The browser starts with an isolated fingerprint and proxy. The `chrome://shardx` start page lists the profile's protections.

<figure>
  <picture>
    <source srcset="../.gitbook/assets/shardbrowser-profile-browser-started_black.png" media="(prefers-color-scheme: dark)">
    <img src="../.gitbook/assets/shardbrowser-profile-browser-started_white.png" alt="Profile launched">
  </picture>
  <figcaption>Profile launched</figcaption>
</figure>

---

### Troubleshooting

#### The app doesn't start

Most likely <mark style="color:purple;">Microsoft Edge WebView2 Runtime</mark> is not installed. Download and install it:

{% embed url="https://developer.microsoft.com/en-us/microsoft-edge/webview2/consumer" %}

Original Windows 10/11 images already include WebView2. Stripped-down builds may have it removed.

## Features

* Generates unique fingerprints for <mark style="color:purple;">Windows</mark>, <mark style="color:purple;">macOS</mark>, and <mark style="color:purple;">Linux</mark> (navigator, screen, client hints, WebGL / WebGPU, etc.)
* Per-vector noise for <mark style="color:purple;">canvas, WebGL, audio, client rects, fonts, and sensors</mark>
* Unlimited profiles organized into folders
* Proxy binding per profile (<mark style="color:purple;">SOCKS5 / HTTP / HTTPS</mark>) with automatic testing when added
* Local **HTTP API** for full automation
* Control through **CDP** (Chrome DevTools Protocol) with Puppeteer, Playwright, and similar tools
* Cookie export and import between profiles
* A separate **MCP server** that lets an AI agent control a profile

### Fingerprints and anti-detect

For every profile, ShardBrowser provides a consistent set of parameters: User-Agent, platform, CPU cores, device memory (never exceeding the real machine), screen resolution, Sec-CH-UA, and more. Per-vector **noise** is applied to canvas, WebGL, audio, client rects, fonts, and sensors. Each noise option is controlled independently, so a profile's fingerprint remains stable across sessions while differing from other profiles and from your real device.

{% hint style="info" %}
The fingerprint is unique and not tied to the hardware: CPU cores and RAM are capped to the host, and screen parameters are limited to the real display. This reduces the risk of detection caused by inconsistent values.
{% endhint %}

### Proxies, QUIC, and WebRTC

Whenever a profile starts, ShardBrowser tests its proxy for UDP relay support (SOCKS5 UDP\_ASSOCIATE) before launching the browser:

* if UDP works, <mark style="color:purple;">QUIC</mark> is enabled and WebRTC uses the proxied UDP relay;
* if UDP is unavailable, QUIC is disabled and WebRTC switches to **TCP-only** mode so the real IP cannot leak.

Timezone, locale, and geolocation fields set to `auto` are also resolved through the proxy at launch.

{% hint style="success" %}
ShardBrowser combined with our [**UDP-supporting proxies**](about-udp/) prevents WebRTC leaks at the browser level: UDP traffic goes through the proxy rather than directly from your IP. Learn more in [**About UDP**](about-udp/).
{% endhint %}

### Automation: local API

The application starts a local HTTP server on <mark style="color:purple;">**127.0.0.1**</mark> (default port **40325**, configurable under _Settings → Automation API_). It is accessible only from your computer.

All requests except `GET /health` require a **Bearer token** (a persistent JWT from the settings):

```
Authorization: Bearer <token>
```

The **Regenerate token** button rotates the secret immediately: the new token becomes active at once and all previous tokens stop working.

Typical automation flow:

1. `GET /fingerprint/new/{platform}` — get a ready-to-use unique fingerprint without saving it.
2. Optionally adjust the fingerprint, for example by enabling font noise or changing the WebRTC mode.
3. `POST /profiles` — create a profile with that fingerprint and bind a proxy.
4. `POST /profiles/{id}/start` — start the profile and receive its **CDP endpoint**.
5. Connect to it as `browserWSEndpoint = cdp.web_socket_debugger_url` in Puppeteer / Playwright.
6. `POST /profiles/{id}/stop` — close the profile.

{% hint style="info" %}
**Temporary profiles.** `POST /profiles/temporary` creates a hidden profile with the `temporary` flag. When the browser closes, the profile and its data directory are deleted automatically.
{% endhint %}

See the [ShardX Launcher API specification](https://docs.shardx.com/eng/shardx-launcher-api/binding-and-lifecycle) for the complete method reference, data models, and examples.

### MCP server for AI agents

ShardBrowser includes a separate **MCP server** (Model Context Protocol). It lets an AI client control the launcher through the API and the profile browser through CDP. It runs as a separate Node process and is not part of the HTTP API.

Download it directly from the launcher under _Settings → MCP server → Download MCP server_. Configure it with `SHARDX_API` (the API base URL) and `SHARDX_TOKEN` (the Bearer token). The MCP server provides:

* **API tools** for profiles, fingerprints, proxies, folders, cookies, start, and stop operations;
* **browser tools** over CDP for navigation, JavaScript execution, screenshots, clicks, text input, tabs, and waits.

{% hint style="warning" %}
CDP (remote debugging) is enabled **only** when a profile is started through the API. Profiles started from the interface do not use a debugging port.
{% endhint %}
