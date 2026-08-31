---
description: How WebRTC works
icon: wave-square
---

# How a WebRTC leak works

An anti-fraud system does not learn your real IP address through a separate request. It **compares two addresses**: the address used for the TCP session and the address reported by the browser through WebRTC over UDP. A mismatch between them is the signal.

### How the check works

The sequence is the same in all three scenarios:

1. The browser opens a page through a SOCKS5 proxy. All HTTP/HTTPS traffic uses TCP, so the website sees the proxy IP address.
2. The anti-fraud system provides a script that creates an `RTCPeerConnection` and specifies its STUN or TURN server in `iceServers`.
3. The browser starts gathering ICE candidates and sends a **STUN Binding Request over UDP** to that server.
4. The STUN server returns a `Binding Response` with an `XOR-MAPPED-ADDRESS` attribute. This attribute contains the public address of the packet source. The browser converts it into a **srflx candidate**.
5. The script receives the candidate through `onicecandidate`, extracts its IP address, and compares it with the address of the TCP session.

Key point: **step 3**. Whether the UDP packet travels through the proxy or bypasses it depends on two things: whether the proxy supports UDP and whether the browser routes UDP through that proxy. This produces three possible outcomes.

<br>

<figure><img src="../../.gitbook/assets/webrtc-leak (1).svg" alt=""><figcaption></figcaption></figure>

### Scenario 1: The proxy carries UDP and the addresses match

1. The TCP session goes through the SOCKS5 proxy, so the website sees `198.51.100.7`.
2. The anti-fraud system provides a script configured with its STUN server.
3. The browser opens a UDP association through the same proxy (`UDP ASSOCIATE`, RFC 1928) and sends the Binding Request through it.
4. STUN sees the proxy address and returns that same value in `XOR-MAPPED-ADDRESS`: `198.51.100.7`.
5. The script compares the values. The TCP session IP and the srflx candidate match.

**Result:** WebRTC works normally, candidates are available, and the addresses match. At the network level, the profile behaves like a regular user.

This requires two things at the same time: a proxy that supports `UDP ASSOCIATE` and a client, such as a browser or antidetect browser, that actually routes WebRTC traffic through the proxy.

***

### Scenario 2: UDP bypasses the proxy and exposes the real address

1. The TCP session goes through the proxy, so the website sees `198.51.100.7`.
2. The anti-fraud system provides a script configured with its STUN server.
3. The browser sends the Binding Request **directly from the network interface**, bypassing the proxy.
4. STUN sees the real address `113.22.13.2` and returns it as a srflx candidate.
5. The script compares the values: `113.22.13.2` ≠ `198.51.100.7`. The proxy is detected and the real IP address is exposed.

**Result:** an IP leak. The anti-fraud system receives a specific address, not merely a suspicious signal.

UDP may bypass the proxy for several reasons:

* the proxy supports **TCP only**: an HTTP proxy using `CONNECT` carries only TCP, as does SOCKS5 without `UDP ASSOCIATE`;
* the proxy supports UDP, but **the browser does not route UDP through it**: by default, Chrome does not send WebRTC traffic through the configured proxy and sends it directly instead;
* the proxy is configured only for a specific profile or extension, while WebRTC operates at the process level.

If the anti-fraud system controls the STUN/TURN server listed in `iceServers`, it does not even need step 5. It can see the real address directly in the source address of the incoming UDP packet.

Local addresses such as `192.168.*` and `10.*` are less relevant here. Starting with Chrome 80, host candidates are represented as mDNS names such as `<uuid>.local`, making local network details harder to obtain through WebRTC. In this scenario, the public srflx address is what gets exposed.

***

### Scenario 3: The browser blocks WebRTC, preventing a leak but creating a signal

1. The TCP session goes through the proxy, so the website sees `198.51.100.7`.
2. The anti-fraud system provides a script configured with its STUN server.
3. `RTCPeerConnection` is blocked by an extension, a browser setting, or a modified API in an antidetect browser. No STUN request is sent through the proxy or directly.
4. There is no response. `onicecandidate` does not fire, and candidate gathering ends with an empty list.
5. The script has no addresses to compare.

**Result:** the real IP address is not exposed. However, the anti-fraud system sees a different anomaly: a current desktop version of Chrome in which **WebRTC is entirely unavailable**. WebRTC is enabled for most regular users, so an empty candidate list can raise the risk score, just like any other mismatch between the claimed user-agent and actual API behavior.

Turning WebRTC off therefore trades an IP leak for a fingerprint anomaly. This may be acceptable in some cases, but it is a tradeoff rather than a complete solution.
