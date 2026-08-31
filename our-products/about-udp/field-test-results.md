---
icon: island-tropical
---

# Results of our field tests

We enabled <mark style="color:purple;">**UDP**</mark> in all [<mark style="color:purple;">**Datacenter**</mark>](../datacenter-proxies.md) proxy locations and tested the setup in the [Vision](../../setup-guides/antidetect-browsers/vision-browser.md) browser. We obtained the following results:

* Google: 15 accounts were created in a row without errors or phone number verification.
* Discord: registration and joining servers with enhanced bot checks succeeded, including servers that normally block ISP proxies.
* Twitter: the 10-image CAPTCHA was accepted, and repeat verification completed without problems.
* Facebook, Instagram, and Facebook Ads: registration completed without issues or a CAPTCHA.

For comparison, the same actions through ISP proxies without **UDP** resulted in errors or required SMS verification.

With WebRTC operating correctly, false bot-activity detections no longer occurred during these tests.
