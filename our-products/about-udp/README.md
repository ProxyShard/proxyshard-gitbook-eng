---
description: >-
  Why proxies need UDP support and how it helps prevent detection by
  anti-fraud systems
icon: shield-exclamation
---

# About the UDP protocol

### **Contents**

* [How WebRTC detection works](how-webrtc-leak-works.md)
* [How to check for WebRTC leaks or WebRTC functionality](webrtc-leak-check-tools.md)
* [Why blocking WebRTC does not protect against detection](why-blocking-webrtc-doesnt-help.md)
* [How to install Tampermonkey and the WebRTC debug script](tampermonkey-webrtc-debug.md)
* [Results of our field tests](field-test-results.md)
* [Software solutions for enabling WebRTC](webrtc-software-solutions.md)
* [Products with UDP support](#products-with-udp-support)
* [FAQ](../../faq-and-support/faq/)

### **Introductory theory**

Modern anti-fraud systems use increasingly sophisticated methods to identify a user's real IP address and detect tools that mask network traffic. Even when you use a proxy or <mark style="color:purple;">VPN</mark>, a website may detect that masking through other signals.

One such mechanism involves <mark style="color:purple;">WebRTC</mark>. This technology can send requests over UDP and expose the user's real IP address if the proxy or client application does not support UDP or routes this traffic incorrectly.

## Products with UDP support

| Product | UDP support |
| --- | --- |
| [Datacenter](../datacenter-proxies.md) | ✓ All locations |
| [ISP](../isp-proxies.md) | ✓ All locations |
| [Mobile](../mobile-proxies.md) | ✓ |
| [Standard Residential](../residential-proxies/standard-residential.md) | ✓ Except USA; [port restrictions apply](../restrictions.md) |
| [Unlimited Residential](../residential-proxies/unlimited-residential-proxy.md) | ✓ Except USA; [port restrictions apply](../restrictions.md) |
| [Premium Residential](../residential-proxies/premium-residential.md) | ✓ All locations [except certain cities and macOS/iOS devices](../restrictions.md) |

To carry UDP traffic, use SOCKS5 and an application that supports `UDP ASSOCIATE`. Compatible options are listed under [Software solutions for enabling WebRTC](webrtc-software-solutions.md).

See [Limitations](../restrictions.md) for the complete list of exceptions and blocked ports.
