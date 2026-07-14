---
description: Installing Tampermonkey in Chrome and adding a custom script
icon: server
---

# How to install Tampermonkey and a WebRTC debug script

## Installing Tampermonkey

To run custom scripts in Chrome, it is convenient to use the **Tampermonkey** extension.

Go to the Chrome Web Store and install the extension:

{% embed url="https://chromewebstore.google.com/detail/tampermonkey/dhdgffkkebhmkfjojejmpbldmpobfkfo" %}

After installation, click the extensions icon in the upper-right corner and pin **Tampermonkey**.

{% hint style="info" %}
The extension is only needed to run the script in the browser. By itself, it does not fix WebRTC leaks.
{% endhint %}

## How to add the script manually

For this guide, use the script from Gist:

* [WebRTC debug script](https://gist.github.com/Kr1tos/26585898c08e5222d5edc3d6fad546be)

{% stepper %}
{% step %}
#### Open the Gist with the script

Open the Gist link.

Open the script file and copy its full contents.
{% endstep %}

{% step %}
#### Create a new script in Tampermonkey

Click the **Tampermonkey** icon and select **Create a new script**.

Delete the default template that opens in the editor.
{% endstep %}

{% step %}
#### Paste the script code

Paste the copied code from Gist into the Tampermonkey editor.

Save the changes with **Ctrl + S** or the **File → Save** button.
{% endstep %}

{% step %}
#### Check that the script is enabled

Make sure the new script appears in the Tampermonkey list and has the **Enabled** status.
{% endstep %}
{% endstepper %}

## How to check that the script works

1. Make sure the script toggle is enabled.
2. Refresh the target page.
3. Open DevTools with **F12**.
4. Go to the **Console** tab.
5. It is convenient to filter output by the `\[TM]`, `\[WebRTC]`, and `\[NET]` labels.

### What logs should appear

Immediately after the script starts, service messages usually appear:

```
[TM] Network hooks installed
[TM] WebRTC hook installed
```

If the page creates an `RTCPeerConnection`, WebRTC logs will appear in the console:

```
[WebRTC] created
config: { iceServers: [...] }
ICE servers: [...]
```

During candidate gathering, local and remote candidates will be visible:

```
[WebRTC] local candidate raw: candidate:...
[WebRTC] local candidate parsed: { ip: "192.168.1.10", port: "52344", type: "host" }

[WebRTC] remote candidate raw: candidate:...
[WebRTC] remote candidate parsed: { ip: "185.123.45.67", port: "3478", type: "srflx" }
```

If the connection reaches route selection, the script will show the final path:

```
[WebRTC] SELECTED PATH (connectionstatechange)
candidate-pair: { ... }
local-candidate: { ip: "10.0.0.2", port: 54012, protocol: "udp", candidateType: "host" }
remote-candidate: { ip: "185.123.45.67", port: 3478, protocol: "udp", candidateType: "srflx" }
[WebRTC] REAL REMOTE ENDPOINT: { ip: "185.123.45.67", port: 3478, protocol: "udp", candidateType: "srflx" }
```

If the website sends WebRTC data through `fetch`, `xhr`, `WebSocket`, or `sendBeacon`, the script will show that as well:

```
[NET][fetch] https://site.example/api
[NET] SDP detected
v=0
o=- 46117317 2 IN IP4 127.0.0.1
...

[NET][ws] wss://site.example/socket
[NET] ICE detected
{"candidate":"candidate:...","sdpMid":"0","sdpMLineIndex":0}
```

### What to look at first

* `\[TM] WebRTC hook installed` — the script loaded successfully.
* `\[WebRTC] created` — the page really created a WebRTC connection.
* `\[WebRTC] local candidate parsed` — a local candidate is visible.
* `\[WebRTC] remote candidate parsed` — a remote candidate is visible.
* `\[WebRTC] REAL REMOTE ENDPOINT` — the most useful log. It shows the final remote endpoint selected by WebRTC.

### If there are few logs

This script adds two manual console commands:

```javascript
__dumpAllWebRTCSelectedPaths()
__dumpAllWebRTCStats()
```

The first command prints the selected paths again.

The second shows a full snapshot of `candidate-pair`, `local-candidate`, `remote-candidate`, and `transport`.

## Useful checks after installation

After starting the script, you can check WebRTC behavior using the services from the article [How to check for WebRTC leaks](webrtc-leak-check-tools.md).

If you want to understand the leak mechanism itself, see [How a WebRTC leak works](how-webrtc-leak-works.md).
