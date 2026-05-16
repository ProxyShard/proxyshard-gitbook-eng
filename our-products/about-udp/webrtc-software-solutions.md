---
icon: git-alt
---

# Software solutions for enabling WebRTC

#### Full WebRTC operation requires software that supports UDP ASSOCIATE.

Examples of supported software for different operating systems:

<mark style="color:purple;">**Antidetect browser:**</mark>

* [<mark style="color:$success;">Vision</mark>](../../setup-guides/antidetect-browsers/#vision) - supports full UDP operation and working QUIC.

{% embed url="https://docs.proxyshard.com/instrukciya-po-ispolzovaniyu/antidetect-browsers/vision-browser" %}

{% hint style="success" %}
At the moment, the combination of our [ISP Proxy](https://dashboard.proxyshard.com/en/isp-proxy) and the [Vision](../../setup-guides/antidetect-browsers/vision-browser.md) browser is the most relevant and correct setup for using UDP with proxies. ISP Proxy also supports p0f switching, which makes proxy detection by any parameters impossible!
{% endhint %}

<mark style="color:purple;">**Windows:**</mark>

* ProxiFyre + Windows Packet Filter
* Win2Socks
* Netch
* [ClashX](../../setup-guides/windows/clashx.md)
* [V2rayN](../../setup-guides/windows/v2rayn.md)

<mark style="color:purple;">**macOS:**</mark>

* [V2Box](../../setup-guides/ios-android/v2box.md)
* Proximac (outdated)

<mark style="color:purple;">**Linux:**</mark>

* proxychains-NG + go-tun2socks
* redsocks-ng

<mark style="color:purple;">**Android:**</mark>

* Clash for Android
* SocksDroid
* [Super Proxy](../../setup-guides/ios-android/super-proxy.md)

<mark style="color:purple;">**Android:**</mark>

* [V2Box](../../setup-guides/ios-android/v2box.md)
* [Potatso](../../setup-guides/ios-android/potatso.md)

{% hint style="info" %}
You can view the current list, which is constantly updated, in the [Setup guide](../../setup-guides/getting-started.md).
{% endhint %}

