---
description: >-
  ShardX anti-detect browser with unique fingerprints and a local API for
  automating profiles via Puppeteer / Playwright
icon: fingerprint
---

# ShardX Launcher

<mark style="color:purple;">**ShardX Browser**</mark> is our anti-detect browser:

## Download and install

Step-by-step guide covering installation, proxy setup, and your first profile:

{% content-ref url="../setup-guides/shardx-browser.md" %}
[ShardX Launcher — setup guide](../setup-guides/shardx-browser.md)
{% endcontent-ref %} create separate profiles with unique fingerprints, bind a dedicated proxy to each one, and work across dozens of accounts as if they were different people on different devices. On top of the manual UI there is a local **Automation API** through which profiles can be created, launched, and driven by Puppeteer / Playwright bots.

#### What ShardX can do:

* Generates unique fingerprints for <mark style="color:purple;">Windows</mark>, <mark style="color:purple;">macOS</mark>, and <mark style="color:purple;">Linux</mark> (navigator, screen, client hints, WebGL / WebGPU, etc.)
* Per-vector noise: <mark style="color:purple;">canvas, WebGL, audio, client rects, fonts, sensors</mark>
* Unlimited profiles organised into folders
* Proxy binding per profile (<mark style="color:purple;">SOCKS5 / HTTP / HTTPS</mark>) with an automatic test on add
* Local **HTTP API** for full automation
* Control via **CDP** (Chrome DevTools Protocol) — Puppeteer, Playwright and equivalents
* Cookie export and import between profiles
* Separate **MCP server** so an AI agent can control a profile

## Fingerprints and anti-detect

For every profile ShardX injects a consistent set of parameters: User-Agent, platform, CPU cores, and device memory (never exceeding the real machine), screen resolution, Sec-CH-UA, and more. On top of that, **noise** is applied per vector — canvas, WebGL, audio, client rects, fonts, sensors. Each noise block is toggled independently, so a profile's fingerprint is stable across sessions yet different from other profiles and from your real device.

{% hint style="info" %}
The fingerprint is uniquified and not tied to hardware: CPU core count and RAM are capped to the host and never inflated, and the screen is clamped to the real display. This reduces the risk of being caught on inconsistencies.
{% endhint %}

## Proxies, QUIC, and WebRTC

ShardX pairs especially well with our proxies. On **every** profile launch, before the browser starts, the bound proxy is tested live for UDP-relay support (SOCKS5 UDP\_ASSOCIATE):

* if UDP works — <mark style="color:purple;">QUIC</mark> is enabled and WebRTC uses the proxied UDP relay;
* if UDP is unavailable — QUIC is disabled and WebRTC is forced into **TCP-only** mode so the real IP cannot leak.

Timezone, locale, and geolocation fields set to `auto` are also resolved live through the proxy at launch time.

{% hint style="success" %}
The ShardX + [**UDP proxies**](udp-proxies.md) combination closes the WebRTC leak at the browser level: UDP traffic goes through the proxy, not directly from your IP. More about the underlying issue in the [**About UDP**](about-udp/) section.
{% endhint %}

## Automation: local API

Inside the application a local HTTP server is started on <mark style="color:purple;">**127.0.0.1**</mark> (default port **40325**, changed in _Settings → Automation API_). It is not reachable from outside — only from your machine.

All requests except `GET /health` require a **Bearer token** (permanent JWT from settings):

```
Authorization: Bearer <token>
```

The **Regenerate token** button in settings instantly rotates the secret: the new token becomes active immediately and all old tokens are invalidated.

Typical automation flow:

1. `GET /fingerprint/new/{platform}` — get a uniquified fingerprint (unsaved).
2. Optionally tweak the fingerprint (e.g. enable font noise or change the WebRTC mode).
3. `POST /profiles` — create a profile with that fingerprint (stored verbatim, no re-randomization) and bind a proxy.
4. `POST /profiles/{id}/start` — launch the profile and receive the **CDP endpoint**.
5. Connect as `browserWSEndpoint = cdp.web_socket_debugger_url` in Puppeteer / Playwright.
6. `POST /profiles/{id}/stop` — close the profile.

{% hint style="info" %}
**Temporary profiles.** `POST /profiles/temporary` creates a profile flagged `temporary`: hidden from the general list and the UI, and auto-deleted when its browser closes (together with its data folder). Convenient for one-off tasks.
{% endhint %}

The full reference for all methods (profiles, fingerprints, proxies, folders, cookies, start/stop) with data models and examples is in the **ShardX Launcher API** section (left-hand menu).

## MCP server for AI agents

A separate **MCP server** (Model Context Protocol) is included: it lets an AI client control the launcher through this same API, and the profile's browser over CDP. It is a separate Node process, not part of the HTTP API.

Download it directly from the launcher (_Settings → MCP server → Download MCP server_). Configure it with two variables: `SHARDX_API` (API base URL) and `SHARDX_TOKEN` (the Bearer token). The MCP server exposes:

* **API tools** — thin wrappers over the launcher methods (profiles, fingerprints, proxies, folders, cookies, start/stop);
* **Browser tools** over CDP — navigation, JS evaluation, screenshots, clicks, text input, tab management, and waits.

{% hint style="warning" %}
CDP (remote-debugging) is enabled **only** when a profile is launched via the API. UI launches have no debug port — anti-detect is not compromised.
{% endhint %}
