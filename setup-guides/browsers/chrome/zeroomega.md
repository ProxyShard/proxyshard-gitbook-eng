---
description: Proxy setup for Chrome
---

# ZeroOmega

## Installing ZeroOmega

{% hint style="warning" %}
ZeroOmega handles TCP traffic only. Use [Vision Browser](../../antidetect-browsers/vision-browser.md) when you need UDP support.
{% endhint %}

Install [ZeroOmega](https://chromewebstore.google.com/detail/pfnededegaaopdmhkdmcofjmoldfiped) from the Chrome Web Store.

{% embed url="https://chromewebstore.google.com/detail/pfnededegaaopdmhkdmcofjmoldfiped" %}

After installation, open the extensions menu and pin ZeroOmega to the browser toolbar.

<figure><img src="../../../.gitbook/assets/chrome-extensions-pin-zeroomega.png" alt="Pinning ZeroOmega to the Chrome toolbar"><figcaption></figcaption></figure>

Open ZeroOmega and select `Параметры`.

<figure>
  <picture>
    <source srcset="../../../.gitbook/assets/chrome-zeroomega-open-options_black.png" media="(prefers-color-scheme: dark)">
    <img src="../../../.gitbook/assets/chrome-zeroomega-open-options_white.png" alt="Opening ZeroOmega settings">
  </picture>
</figure>

## Configuring the proxy

In the profiles section, click `Новый профиль...`.

<div align="center"><figure>
  <picture>
    <source srcset="../../../.gitbook/assets/chrome-zeroomega-new-profile_black.png" media="(prefers-color-scheme: dark)">
    <img src="../../../.gitbook/assets/chrome-zeroomega-new-profile_white.png" alt="Creating a ZeroOmega profile">
  </picture>
</figure></div>

Enter a profile name, select `Профиль прокси`, and click `Создать`.

<figure>
  <picture>
    <source srcset="../../../.gitbook/assets/chrome-zeroomega-new-profile-dialog_black.png" media="(prefers-color-scheme: dark)">
    <img src="../../../.gitbook/assets/chrome-zeroomega-new-profile-dialog_white.png" alt="ZeroOmega profile name and type">
  </picture>
</figure>

In the profile settings, select the protocol and enter the server address and port from your order's `Proxy List`. Click the lock icon to add the username and password.

{% hint style="info" %}
The data format and an example order are described in [Getting Started](../../getting-started.md).
{% endhint %}

<figure>
  <picture>
    <source srcset="../../../.gitbook/assets/chrome-zeroomega-proxy-server_black.png" media="(prefers-color-scheme: dark)">
    <img src="../../../.gitbook/assets/chrome-zeroomega-proxy-server_white.png" alt="Proxy address and port in ZeroOmega">
  </picture>
</figure>

Enter the proxy username and password, then click `Сохранить изменения`.

<figure>
  <picture>
    <source srcset="../../../.gitbook/assets/chrome-zeroomega-proxy-auth_black.png" media="(prefers-color-scheme: dark)">
    <img src="../../../.gitbook/assets/chrome-zeroomega-proxy-auth_white.png" alt="Proxy authentication in ZeroOmega">
  </picture>
</figure>

Click `Применить изменения` to save the profile.

<figure>
  <picture>
    <source srcset="../../../.gitbook/assets/chrome-zeroomega-apply-changes_black.png" media="(prefers-color-scheme: dark)">
    <img src="../../../.gitbook/assets/chrome-zeroomega-apply-changes_white.png" alt="Saving the ZeroOmega profile">
  </picture>
</figure>

Open ZeroOmega from the browser toolbar and select the profile you created.

<figure><img src="../../../.gitbook/assets/chrome-zeroomega-select-profile.png" alt="Selecting a ZeroOmega profile"><figcaption></figcaption></figure>

The proxy is connected and ready to use in Chrome.
