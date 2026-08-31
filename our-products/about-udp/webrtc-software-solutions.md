---
icon: git-alt
---

# Software solutions for enabling WebRTC

#### Full WebRTC operation requires software that supports UDP ASSOCIATE.

Examples of supported software for different operating systems:

<mark style="color:purple;">**Antidetect browsers:**</mark>

* [<mark style="color:$success;">Vision</mark>](../../setup-guides/antidetect-browsers/vision-browser.md): an accessible and reliable paid browser with support for UDP, QUIC, Smart Fingerprint, and other useful features. More than 60% of teams on our website choose it.

{% hint style="success" %}
Our [ISP Proxy](https://dashboard.proxyshard.com/en/isp-proxy) combined with the [Vision](../../setup-guides/antidetect-browsers/vision-browser.md) browser is one of the recommended setups for using UDP through a proxy. ISP Proxy also supports changing the [p0f](../p0f-spoofing.md) network fingerprint.
{% endhint %}

* [<mark style="color:$tint;">ShardX</mark>](../shardx-launcher.md): our open-source solution with a wide selection of profiles and proper UDP and QUIC support.

<mark style="color:purple;">**Windows:**</mark>

* ProxiFyre + Windows Packet Filter
* Win2Socks
* Netch
* [ClashX](../../setup-guides/windows/clashx.md)
* [V2rayN](../../setup-guides/windows/v2rayn.md)

<mark style="color:purple;">**macOS:**</mark>

* [V2Box](../../setup-guides/ios-android/v2box.md)

<mark style="color:purple;">**Linux:**</mark>

* proxychains-NG + go-tun2socks
* redsocks-ng

<mark style="color:purple;">**Android:**</mark>

* Clash for Android
* SocksDroid
* [Super Proxy](../../setup-guides/ios-android/super-proxy.md)
* [V2Box](../../setup-guides/ios-android/v2box.md)
* [Potatso](../../setup-guides/ios-android/potatso.md)

{% hint style="info" %}
The current list of applications is available in the [Setup guide](../../setup-guides/getting-started.md).
{% endhint %}
