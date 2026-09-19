---
icon: arrow-down-right
---

# Why blocking WebRTC does not protect against detection

Many antidetect browsers block <mark style="color:purple;">WebRTC</mark> to prevent the real IP address from leaking. However, blocking it can itself become a signal for an anti-fraud system. WebRTC works for most regular users, so its complete absence is unusual.

If a profile has no native UDP support, a website running a WebRTC check may receive an empty list of ICE candidates. The real address is not exposed, but the website can see that the browser behaves differently from a standard configuration and may raise its risk score.

The correct approach is to keep WebRTC enabled and route its UDP traffic through the proxy. Both the client application and the proxy must support `UDP ASSOCIATE`.

UDP is available across all ProxyShard product lines, with restrictions for certain products, locations and devices. See the current summary on the [About the UDP protocol](README.md#products-with-udp-support) page and compatible applications under [Software solutions for enabling WebRTC](webrtc-software-solutions.md).
