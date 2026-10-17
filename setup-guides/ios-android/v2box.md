# V2Box

{% hint style="success" %}
V2Box supports UDP traffic.
{% endhint %}

## Installing V2Box

Install V2Box from the app store for your device.

#### <mark style="color:green;">Android</mark>

{% embed url="https://play.google.com/store/apps/details?id=dev.hexasoftware.v2box" %}

#### <mark style="color:blue;">**iOS**</mark>

{% embed url="https://apps.apple.com/app/v2box-v2ray-client/id6446814690" %}

## Configuring V2Box

1. Open `Configs`.
2. Tap `+` to create a configuration.

<figure>
  <picture>
    <source srcset="../../.gitbook/assets/v2box-ios-configs-add_black.png" media="(prefers-color-scheme: dark)">
    <img src="../../.gitbook/assets/v2box-ios-configs-add_white.png" alt="Adding a configuration in V2Box">
  </picture>
</figure>

<figure>
  <picture>
    <source srcset="../../.gitbook/assets/v2box-ios-add-manual-config_black.png" media="(prefers-color-scheme: dark)">
    <img src="../../.gitbook/assets/v2box-ios-add-manual-config_white.png" alt="Manual configuration in V2Box">
  </picture>
</figure>

In `Protocol`, select `SOCKS`.

<figure>
  <picture>
    <source srcset="../../.gitbook/assets/v2box-ios-protocol-socks_black.png" media="(prefers-color-scheme: dark)">
    <img src="../../.gitbook/assets/v2box-ios-protocol-socks_white.png" alt="Selecting the SOCKS protocol in V2Box">
  </picture>
</figure>

Enter a configuration name in `Remarks`. Fill in `Address`, `Port`, `Username`, and `ID/Password/Key` using the details from your order's `Proxy List`, then tap `Save`.

<figure>
  <picture>
    <source srcset="../../.gitbook/assets/v2box-ios-server-form_black.png" media="(prefers-color-scheme: dark)">
    <img src="../../.gitbook/assets/v2box-ios-server-form_white.png" alt="Proxy configuration in V2Box">
  </picture>
</figure>

{% hint style="info" %}
The data format and an example order are described in [Getting Started](../getting-started.md).
{% endhint %}

Return to `Configs`, select the configuration you created, and use `Slide to Connect` to connect.

<figure>
  <picture>
    <source srcset="../../.gitbook/assets/v2box-ios-connected_black.png" media="(prefers-color-scheme: dark)">
    <img src="../../.gitbook/assets/v2box-ios-connected_white.png" alt="Connecting through a proxy in V2Box">
  </picture>
</figure>

Test the connection with [Proxy Tester](../../our-products/proxy-tester.md).
