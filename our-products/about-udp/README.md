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
* [FAQ](../../faq-and-support/faq/)

### **Introductory theory**

Modern anti-fraud systems use increasingly sophisticated methods to identify a user's real IP address and detect tools that mask network traffic. Even when you use a proxy or <mark style="color:purple;">VPN</mark>, a website may detect that masking through other signals.

One such mechanism involves <mark style="color:purple;">WebRTC</mark>. This technology can send requests over UDP and expose the user's real IP address if the proxy or client application does not support UDP or routes this traffic incorrectly.
