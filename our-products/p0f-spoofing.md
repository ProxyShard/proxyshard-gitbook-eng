---
icon: fingerprint
---

# Network fingerprint spoofing (p0f)

## What p0f is and why it matters

Every device on a network has a digital fingerprint at the <mark style="color:$primary;">TCP/IP</mark> level, called <mark style="color:$primary;">**p0f**</mark>. It is formed from network stack parameters such as MSS, TSval, TTL, TCP options, Window size, and TOS. These parameters differ across Windows, macOS, Linux, iOS, and Android, and anti-fraud systems can use those differences to identify the device environment.

How websites perform these checks:

1. The website checks the <mark style="color:$primary;">**User-Agent**</mark>, <mark style="color:$primary;">**TLS fingerprint**</mark>, and other client parameters to determine which operating system the user is using.
2. In parallel, the <mark style="color:$primary;">**network layer**</mark> of the connection is analyzed, namely the <mark style="color:$primary;">TCP/IP fingerprint</mark> that the proxy server sends together with your traffic.
3. If the browser says “I am Windows 11”, but the TCP/IP fingerprint indicates <mark style="color:$primary;">Linux</mark>, the anti-fraud system records a mismatch.

**A common problem:** Datacenter and ISP proxies usually run on Linux servers. Without spoofing, the network fingerprint may indicate Linux even when the user is working on Windows or macOS. An anti-fraud system may treat this mismatch as a sign that a proxy is being used.

## How ProxyShard solves this

We added the ability to **spoof the p0f fingerprint** directly from the dashboard. You select the required OS, and the proxy server starts sending network packets with the corresponding TCP/IP fingerprint.

Available spoofing options:

| Value          | Description                 |
| -------------- | --------------------------- |
| **Unset**      | Default fingerprint (Linux) |
| **Windows 10** | Windows 10 fingerprint      |
| **Windows 11** | Windows 11 fingerprint      |
| **Mac OS**     | macOS fingerprint           |
| **Linux**      | Linux fingerprint           |
| **iOS**        | iOS fingerprint             |
| **Android**    | Android fingerprint         |

### ISP and Datacenter proxies

Open the order, click `p0f`, and select the required OS for each IP. The setting works the same way for ISP and Datacenter proxies.

<figure>
  <picture>
    <source srcset="../.gitbook/assets/p0f-datacenter-isp_black.png" media="(prefers-color-scheme: dark)">
    <img src="../.gitbook/assets/p0f-datacenter-isp_white.png" alt="p0f settings for ISP and Datacenter proxies">
  </picture>
</figure>

### Mobile proxies

In the `Signature` field, select the OS whose fingerprint the proxy should use. After changing the setting, restart the proxy with `Restart`.

<figure>
  <picture>
    <source srcset="../.gitbook/assets/p0f-mobile_black.png" media="(prefers-color-scheme: dark)">
    <img src="../.gitbook/assets/p0f-mobile_white.png" alt="Network fingerprint selection for a Mobile proxy">
  </picture>
</figure>

Some Mobile proxy locations do not support p0f spoofing. See [Limitations](restrictions.md) for the current list.

### Premium Residential

For Premium Residential, the `Device OS` parameter filters the proxy pool by the device operating system. It filters the pool rather than spoofing the network fingerprint.

<figure>
  <picture>
    <source srcset="../.gitbook/assets/p0f-premium-residential_black.png" media="(prefers-color-scheme: dark)">
    <img src="../.gitbook/assets/p0f-premium-residential_white.png" alt="Filtering Premium Residential proxies by Device OS">
  </picture>
</figure>

The availability of `Device OS` depends on the location. See [Limitations](restrictions.md) for details.

{% hint style="warning" %}
Before changing p0f, close all connections through the proxy. Existing connections will continue to use the previous fingerprint and may prevent the new setting from taking effect. After changing p0f, wait 2-3 minutes before reconnecting.
{% endhint %}

## Real results

Initial tests show that p0f spoofing helps with anti-fraud checks. One confirmed scenario:

{% hint style="success" %}
**Google accounts:** together with the developer of [Vision Browser](../setup-guides/antidetect-browsers/vision-browser.md), we tested Google registration without changing the browser fingerprint. On a clean profile without p0f spoofing, the system immediately requests verification through a QR code. After setting the fingerprint to Windows 10 or Windows 11, the QR check no longer appears and Google offers phone-number verification instead. This shows that the mismatch between the browser and network fingerprints has been removed.
{% endhint %}

When registering a Google account on a desktop device, a mismatch between the browser and network fingerprints usually triggers QR-code verification. p0f spoofing helps align the network fingerprint with the selected operating system.

## Recommended stack

For maximum results, we recommend using:

* [**Vision Browser**](../setup-guides/antidetect-browsers/vision-browser.md), an antidetect browser with UDP support
* **ProxyShard ISP proxies** with p0f spoofing enabled

In this configuration, Vision Browser handles the browser fingerprint, p0f handles the network fingerprint, and the ISP proxy provides an IP address from a residential internet provider.

## Where it is available

p0f spoofing and device filtering are available on the following products:

* [Datacenter proxies](datacenter-proxies.md)
* [ISP proxies](isp-proxies.md)
* [Mobile proxies](mobile-proxies.md)
* [Premium Residential](residential-proxies/premium-residential.md) - device filtering through the [Device OS](residential-proxies/#proxy-configuration) parameter, without p0f spoofing

{% hint style="warning" %}
p0f spoofing is not available on some [Mobile proxies](mobile-proxies.md). See the full list of restrictions on the [Limitations](restrictions.md) page.
{% endhint %}
