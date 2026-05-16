---
description: >-
  Why UDP support is needed in proxies and how it helps bypass
  anti-fraud systems
icon: shield-exclamation
---

# About the UDP protocol

### **Contents**&#x20;

* [How WebRTC detection works](how-webrtc-leak-works.md)
* [How to check for WebRTC leaks or WebRTC functionality](webrtc-leak-check-tools.md)
* [Why a TCP proxy alone is not enough!](why-tcp-proxy-not-enough.md)
* [Software solutions for enabling WebRTC](webrtc-software-solutions.md)
* [Why blocking WebRTC does not protect you from detection](why-blocking-webrtc-doesnt-help.md)
* [Results of our field tests](field-test-results.md)
* [FAQ](../../faq-and-support/faq/)



### **Introductory theory**

Modern anti-fraud systems are becoming increasingly persistent in identifying your real address or detecting the use of tools that hide your address. Even if you use a proxy or <mark style="color:purple;">VPN</mark>, they can determine that you are not a “real” user by many parameters.&#x20;

One of the most common detection mechanisms is <mark style="color:purple;">WebRTC</mark>, a technology that can send requests around the proxy and therefore expose your real IP if <mark style="color:purple;">WebRTC</mark> is not blocked by the browser.<br>

The solution? Two-way <mark style="color:purple;">UDP</mark> protocol support in both proxies and software products.

{% hint style="info" %}
<sup>_This article was inspired by_</sup> [<sup>_Zl0yTeam_</sup>](https://t.me/Zl0yTeam)<sup>_ and their article_</sup> [<sup>_“Why UDP proxies are needed and what WebRTC has to do with it”_</sup>](https://telegra.ph/Zachem-nuzhny-proksi-s-UDP-i-pri-chyom-tut-protechka-WrbRTC-v-Antike-12-19)<sup>_._</sup>\ <sup>_It helped us significantly understand how_</sup><sup>_&#x20;_</sup><sup>_<mark style="color:purple;">WebRTC</mark>_</sup><sup>_&#x20;_</sup><sup>_works and write this article!_</sup>
{% endhint %}

&#x20;
