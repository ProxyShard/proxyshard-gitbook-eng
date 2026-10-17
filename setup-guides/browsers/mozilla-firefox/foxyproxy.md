---
description: Proxy setup for Mozilla Firefox
---

# FoxyProxy

## Installing FoxyProxy

{% hint style="warning" %}
FoxyProxy handles TCP traffic only.
{% endhint %}

Install [FoxyProxy Standard](https://addons.mozilla.org/firefox/addon/foxyproxy-standard/) from Firefox Add-ons.

{% embed url="https://addons.mozilla.org/firefox/addon/foxyproxy-standard/" %}

<figure>
  <picture>
    <source srcset="../../../.gitbook/assets/foxyproxy-addon-page_black.png" media="(prefers-color-scheme: dark)">
    <img src="../../../.gitbook/assets/foxyproxy-addon-page_white.png" alt="FoxyProxy Standard in Firefox Add-ons">
  </picture>
</figure>

After installation, open FoxyProxy and go to the extension settings.

<figure>
  <picture>
    <source srcset="../../../.gitbook/assets/foxyproxy-options-popup-disable_black.png" media="(prefers-color-scheme: dark)">
    <img src="../../../.gitbook/assets/foxyproxy-options-popup-disable_white.png" alt="Opening FoxyProxy settings">
  </picture>
</figure>

## Configuring the proxy

Open `Proxies` and click `Add`.

<figure>
  <picture>
    <source srcset="../../../.gitbook/assets/foxyproxy-add-proxy-form_black.png" media="(prefers-color-scheme: dark)">
    <img src="../../../.gitbook/assets/foxyproxy-add-proxy-form_white.png" alt="Adding a proxy in FoxyProxy">
  </picture>
</figure>

{% hint style="info" %}
The data format and an example order are described in [Getting Started](../../getting-started.md).
{% endhint %}

Enter a profile name in `Title`. Select the proxy type, then fill in `Hostname`, `Port`, `Username`, and `Password` using the details from your order's `Proxy List`. Click `Save`.

<figure>
  <picture>
    <source srcset="../../../.gitbook/assets/foxyproxy-proxy-config-filled_black.png" media="(prefers-color-scheme: dark)">
    <img src="../../../.gitbook/assets/foxyproxy-proxy-config-filled_white.png" alt="Completed proxy profile in FoxyProxy">
  </picture>
</figure>

## Connecting

Open FoxyProxy and select the profile you created.

<figure>
  <picture>
    <source srcset="../../../.gitbook/assets/foxyproxy-options-popup-proxyshard_black.png" media="(prefers-color-scheme: dark)">
    <img src="../../../.gitbook/assets/foxyproxy-options-popup-proxyshard_white.png" alt="Selecting a proxy profile in FoxyProxy">
  </picture>
</figure>

The proxy is connected and ready to use in Mozilla Firefox.
