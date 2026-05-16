---
icon: lock-keyhole-open
---

# Why a TCP proxy alone is not enough!

Even if your SOCKS5 proxy supports <mark style="color:purple;">UDP</mark>, most antidetect browsers, especially Chromium-based ones, cannot pass <mark style="color:purple;">WebRTC</mark> traffic through a proxy. The reason is technical limitations in the browser engine.

Today, captcha systems are already introducing enhanced checks for the presence of <mark style="color:purple;">WebRTC</mark>. One example is <mark style="color:purple;">Discord</mark>: they connected "<mark style="color:purple;">Hcaptcha-enterprise</mark>", where checks for enabled <mark style="color:purple;">WebRTC</mark> on the user side are already included.
