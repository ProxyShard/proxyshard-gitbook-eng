---
description: How WebRTC works
icon: wave-square
---

# How a WebRTC leak works

1. The website sends a regular TCP request from the browser or antidetect browser.
2. The anti-fraud system responds and injects a script for a STUN request.
3. The browser makes a STUN request over UDP, bypassing the proxy from the real address, because the proxy or antidetect browser may not support UDP.
4.  If the IP in the TCP connection and the UDP connection differs, the user is exposed as using a proxy.<br>

