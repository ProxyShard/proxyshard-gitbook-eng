---
description: Proxy setup for Microsoft Edge
---

# ZeroOmega

## Installing ZeroOmega

{% hint style="warning" %}
ZeroOmega handles TCP traffic only. Use [Vision Browser](../../antidetect-browsers/vision-browser.md) when you need UDP support.
{% endhint %}

Install [ZeroOmega](https://microsoftedge.microsoft.com/addons/detail/proxy-switchyomega-3-zer/dmaldhchmoafliphkijbfhaomcgglmgd) from Microsoft Edge Add-ons.

{% embed url="https://microsoftedge.microsoft.com/addons/detail/proxy-switchyomega-3-zer/dmaldhchmoafliphkijbfhaomcgglmgd" %}

<figure>
  <picture>
    <source srcset="../../../.gitbook/assets/edge-zeroomega-addons-get_black.png" media="(prefers-color-scheme: dark)">
    <img src="../../../.gitbook/assets/edge-zeroomega-addons-get_white.png" alt="Installing ZeroOmega in Microsoft Edge">
  </picture>
</figure>

After installation, open the extensions menu and pin ZeroOmega to the browser toolbar.

<figure><img src="../../../.gitbook/assets/edge-extensions-pin-zeroomega.png" alt="Pinning ZeroOmega to the Microsoft Edge toolbar"><figcaption></figcaption></figure>

## Configuring ZeroOmega

Open ZeroOmega and select `Options`.

<figure><img src="../../../.gitbook/assets/edge-zeroomega-popup-options.png" alt="Opening ZeroOmega settings"><figcaption></figcaption></figure>

Under `Profiles`, click `New profile...`.

<div align="center"><figure>
  <picture>
    <source srcset="../../../.gitbook/assets/edge-zeroomega-new-profile_black.png" media="(prefers-color-scheme: dark)">
    <img src="../../../.gitbook/assets/edge-zeroomega-new-profile_white.png" alt="Creating a ZeroOmega profile">
  </picture>
</figure></div>

Enter a profile name, select `Proxy Profile`, and click `Create`.

<figure>
  <picture>
    <source srcset="../../../.gitbook/assets/edge-zeroomega-new-profile-dialog_black.png" media="(prefers-color-scheme: dark)">
    <img src="../../../.gitbook/assets/edge-zeroomega-new-profile-dialog_white.png" alt="ZeroOmega profile name and type">
  </picture>
</figure>

In the profile settings, select the protocol and enter the server address and port from your order's `Proxy List`. Click the lock icon to add the username and password.

<figure>
  <picture>
    <source srcset="../../../.gitbook/assets/edge-zeroomega-proxy-server_black.png" media="(prefers-color-scheme: dark)">
    <img src="../../../.gitbook/assets/edge-zeroomega-proxy-server_white.png" alt="Proxy address and port in ZeroOmega">
  </picture>
</figure>

Enter the proxy username and password, then confirm the changes.

<figure>
  <picture>
    <source srcset="../../../.gitbook/assets/edge-zeroomega-proxy-auth_black.png" media="(prefers-color-scheme: dark)">
    <img src="../../../.gitbook/assets/edge-zeroomega-proxy-auth_white.png" alt="Proxy authentication in ZeroOmega">
  </picture>
</figure>

{% hint style="info" %}
The data format and an example order are described in [Getting Started](../../getting-started.md).
{% endhint %}

Click `Apply changes` to save the profile.

<figure>
  <picture>
    <source srcset="../../../.gitbook/assets/edge-zeroomega-apply-changes_black.png" media="(prefers-color-scheme: dark)">
    <img src="../../../.gitbook/assets/edge-zeroomega-apply-changes_white.png" alt="Saving the ZeroOmega profile">
  </picture>
</figure>

Open ZeroOmega from the browser toolbar and select the profile you created.

<figure>
  <picture>
    <source srcset="../../../.gitbook/assets/edge-zeroomega-select-profile_black.png" media="(prefers-color-scheme: dark)">
    <img src="../../../.gitbook/assets/edge-zeroomega-select-profile_white.png" alt="Selecting a ZeroOmega profile">
  </picture>
</figure>

The proxy is connected and ready to use in Microsoft Edge.
