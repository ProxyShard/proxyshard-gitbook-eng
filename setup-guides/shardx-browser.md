---
description: Installing ShardX Launcher, setting up proxies, and launching your first profile
icon: browser
---

# ShardX Launcher

{% hint style="info" %}
ShardX Launcher is distributed under the MIT license as a free tool for personal use. The software is provided "as is". We regularly release updates, but we don't offer live chat support - for serious issues, please file a bug report on [GitHub](https://github.com/ProxyShard/ShardBrowser/issues).
{% endhint %}

## System Requirements

### Windows

| Component    | Minimum                                       | Recommended                                   |
| ------------ | --------------------------------------------- | --------------------------------------------- |
| OS           | Windows 10 22H2 or Windows 11, 64-bit         | Windows 11 64-bit                             |
| Architecture | x64 / x86\_64                                 | x64                                           |
| CPU          | Dual-core 64-bit with SSE3 support            | Quad-core or better                           |
| RAM          | 4 GB                                          | 8 GB (16 GB for heavy multi-profile use)      |
| Disk space   | 1 GB                                          | 5 GB+                                         |
| Runtime      | Microsoft Edge WebView2                       | -                                             |

### macOS

| Component  | Minimum                          | Recommended            |
| ---------- | -------------------------------- | ---------------------- |
| OS         | macOS 11 Big Sur or newer        | Latest stable release  |
| CPU        | Apple Silicon M1 or newer        | Apple M2 or newer      |
| RAM        | 4 GB                             | 8 GB or more           |
| Disk space | 1 GB                             | 5 GB+                  |

{% hint style="warning" %}
The current build targets `aarch64-apple-darwin`. Intel Macs are not supported.
{% endhint %}

---

## Installing on Windows

Download the latest release:

{% embed url="https://github.com/ProxyShard/ShardBrowser/releases/latest" %}

Under <mark style="color:purple;">**Assets**</mark>, pick the <mark style="color:purple;">`.exe`</mark> or <mark style="color:purple;">`.msi`</mark> file.

<figure><img src="../.gitbook/assets/shardx-win-download.png" alt=""><figcaption>Choose .exe or .msi under Assets</figcaption></figure>

Run the downloaded file. <mark style="color:purple;">Windows SmartScreen</mark> may show a warning - click <mark style="color:purple;">**More info**</mark>, then <mark style="color:purple;">**Run anyway**</mark>.

<figure><img src="../.gitbook/assets/shardx-win-smartscreen.png" alt=""><figcaption>SmartScreen - click «Run anyway»</figcaption></figure>

The installer will finish in a few seconds.

<figure><img src="../.gitbook/assets/shardx-win-install-done.png" alt=""><figcaption>Installation complete</figcaption></figure>

---

## Installing on macOS

Download the latest release:

{% embed url="https://github.com/ProxyShard/ShardBrowser/releases/latest" %}

Under <mark style="color:purple;">**Assets**</mark>, pick the <mark style="color:purple;">`aarch64.dmg`</mark> file.

<figure><img src="../.gitbook/assets/shardx-mac-download.png" alt=""><figcaption>Choose aarch64.dmg under Assets</figcaption></figure>

Open the downloaded `.dmg` and drag <mark style="color:purple;">**ShardX Launcher**</mark> into the <mark style="color:purple;">**Applications**</mark> folder.

<figure><img src="../.gitbook/assets/shardx-mac-install-dmg.png" alt=""><figcaption>Drag the icon into Applications</figcaption></figure>

### Bypassing Gatekeeper

{% hint style="warning" %}
This step is mandatory. macOS blocks all unsigned apps - without it the application will not open.
{% endhint %}

Open <mark style="color:purple;">**Terminal**</mark> using one of two methods:

- <mark style="color:purple;">**Spotlight:**</mark> press `⌘ + Space`, type `terminal`, select the app

<figure><img src="../.gitbook/assets/shardx-mac-find-terminal.png" alt=""><figcaption>Finding Terminal via Spotlight</figcaption></figure>

- <mark style="color:purple;">**Finder:**</mark> Applications -> Utilities -> Terminal

Paste the command and press <mark style="color:purple;">**Enter:**</mark>

```bash
xattr -dr com.apple.quarantine "/Applications/ShardX Launcher.app"
```

<figure><img src="../.gitbook/assets/shardx-mac-xattr-command.png" alt=""><figcaption>The command runs silently - that's normal</figcaption></figure>

After that, open the app via <mark style="color:purple;">Spotlight</mark> (`⌘ + Space` → `shardx`) or from the <mark style="color:purple;">Applications</mark> folder.

<figure><img src="../.gitbook/assets/shardx-mac-open-spotlight.png" alt=""><figcaption>Launching ShardX via Spotlight</figcaption></figure>

---

## First Launch

On first launch ShardX downloads the browser engine from CDN (about 198 MB, one time only). Wait for the download to finish.

<figure><img src="../.gitbook/assets/shardx-win-first-run.png" alt=""><figcaption>Downloading the engine on first launch</figcaption></figure>

Once done, the main <mark style="color:purple;">**Browsers**</mark> screen will open.

<figure><img src="../.gitbook/assets/shardx-win-ready.png" alt=""><figcaption>ShardX Launcher main screen</figcaption></figure>

---

## Adding a Proxy

Go to the <mark style="color:purple;">**Proxies**</mark> section and click <mark style="color:purple;">**+ New proxy**</mark>.

<figure><img src="../.gitbook/assets/shardx-setup-proxy-empty.png" alt=""><figcaption>Proxies section</figcaption></figure>

In the <mark style="color:purple;">**Bulk import proxies**</mark> window, paste your proxies one per line. Supported formats:

```
host:port
host:port:user:pass
scheme://host:port
scheme://user:pass@host:port
```

<figure><img src="../.gitbook/assets/shardx-setup-add-proxy.png" alt=""><figcaption>Paste proxies one per line</figcaption></figure>

Click <mark style="color:purple;">**Test all**</mark> to check the proxies before importing.

<figure><img src="../.gitbook/assets/shardx-setup-check-proxy.png" alt=""><figcaption>Click «Test all» to verify, then «Import»</figcaption></figure>

After testing, each proxy gets a status. Proxies with the <mark style="color:purple;">**UDP**</mark> label support <mark style="color:purple;">SOCKS5 UDP</mark>, which means <mark style="color:purple;">WebRTC</mark> too - very useful when working with serious antifraud systems. If there is no <mark style="color:purple;">**UDP**</mark> label, the browser profile automatically switches to <mark style="color:purple;">**TCP-only**</mark> mode: your IP won't leak, but traffic may look suspicious to advanced antifraud systems. We strongly recommend using [proxies with UDP support](../our-products/about-udp/).

Click <mark style="color:purple;">**Import**</mark> - the proxy will appear in the list with status <mark style="color:purple;">**Active**</mark>.

<figure><img src="../.gitbook/assets/shardx-setup-proxy-done.png" alt=""><figcaption>Proxy added</figcaption></figure>

---

## Creating Your First Profile

Go to the <mark style="color:purple;">**Browsers**</mark> section and click <mark style="color:purple;">**+ New profile**</mark>.

<figure><img src="../.gitbook/assets/shardx-setup-profiles-empty.png" alt=""><figcaption>Browsers section</figcaption></figure>

No need to change the default settings - ShardX will generate a unique <mark style="color:purple;">fingerprint</mark> automatically. Make sure to select a proxy in the <mark style="color:purple;">**Proxy**</mark> field at the bottom of the form.

<figure><img src="../.gitbook/assets/shardx-setup-new-profile.png" alt=""><figcaption>Select a proxy and click «Create profile»</figcaption></figure>

Click <mark style="color:purple;">**Create profile**</mark>.

<figure><img src="../.gitbook/assets/shardx-setup-profile-proxy-check.png" alt=""><figcaption>Profile created</figcaption></figure>

---

## Launching a Profile

Click <mark style="color:purple;">**Start**</mark> - the browser will open with an isolated fingerprint and proxy.

<figure><img src="../.gitbook/assets/shardx-setup-done.png" alt=""><figcaption>Profile launched</figcaption></figure>

---

## Troubleshooting

### Windows: the app won't start

Most likely <mark style="color:purple;">Microsoft Edge WebView2 Runtime</mark> is not installed. Download and install it:

{% embed url="https://developer.microsoft.com/en-us/microsoft-edge/webview2/consumer" %}

Original Windows 10/11 images already include WebView2. On stripped-down builds it may have been removed.

### macOS: "ShardX Launcher is damaged and can't be opened"

This is a standard <mark style="color:purple;">Gatekeeper</mark> block. Follow the steps in [Bypassing Gatekeeper](#bypassing-gatekeeper) - both ways to open Terminal and the command to remove the quarantine flag are described there.

---

## What's Next?

- **Automation:** manage profiles via the [local HTTP API](../our-products/shardx-launcher.md) on `127.0.0.1:40325`
- **MCP server:** download it from settings (<mark style="color:purple;">Settings -> MCP server</mark>) to control profiles via an AI agent
