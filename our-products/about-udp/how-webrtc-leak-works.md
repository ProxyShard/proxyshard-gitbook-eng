---
description: How WebRTC works
icon: wave-square
---

# How a WebRTC leak works

1. The website sends a regular TCP request from the browser or antidetect browser.
2. The anti-fraud system responds and injects a script for a STUN request.
3. The browser makes a STUN request over UDP, bypassing the proxy from the real address, because the proxy or antidetect browser may not support UDP.
4.  If the IP in the TCP connection and the UDP connection differs, the user is exposed as using a proxy.<br>

    <figure><img src="../../.gitbook/assets/image (181).png" alt=""><figcaption><p>The image and information were taken and translated from the <a href="https://telegra.ph/Zachem-nuzhny-proksi-s-UDP-i-pri-chyom-tut-protechka-WrbRTC-v-Antike-12-19">ZloyTeam</a> article</p></figcaption></figure>
