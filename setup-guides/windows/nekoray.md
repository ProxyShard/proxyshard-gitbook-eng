# NekoRay

{% hint style="success" %}
NekoRay can proxy both TCP and UDP traffic in TUN mode.
{% endhint %}

## Download and launch

Download the Windows archive from the [NekoRay releases page](https://github.com/MatsuriDayo/nekoray/releases), extract it, and run `nekoray.exe` or `nekobox.exe`. Select the `sing-box` core on first launch.

<figure>
  <picture>
    <source srcset="../../.gitbook/assets/nekoray-github-download_black.png" media="(prefers-color-scheme: dark)">
    <img src="../../.gitbook/assets/nekoray-github-download_white.png" alt="Downloading NekoRay from GitHub">
  </picture>
</figure>

## Create a profile

Right-click an empty area in the server list and select `New profile`.

<figure>
  <picture>
    <source srcset="../../.gitbook/assets/nekoray-main-new-profile_black.png" media="(prefers-color-scheme: dark)">
    <img src="../../.gitbook/assets/nekoray-main-new-profile_white.png" alt="Creating a new NekoRay profile">
  </picture>
</figure>

Select `Socks` from the `Type` list.

<figure>
  <picture>
    <source srcset="../../.gitbook/assets/nekoray-profile-type-socks_black.png" media="(prefers-color-scheme: dark)">
    <img src="../../.gitbook/assets/nekoray-profile-type-socks_white.png" alt="Selecting the Socks profile type in NekoRay">
  </picture>
</figure>

Enter the connection details:

1. Enter any recognizable name in `Name`.
2. Enter the proxy address and port in `Address` and `Port`.
3. Under `Socks`, select `Version: 5`.
4. Enter the `Username` and `Password`.
5. Click `OK`.

<figure>
  <picture>
    <source srcset="../../.gitbook/assets/nekoray-profile-config_black.png" media="(prefers-color-scheme: dark)">
    <img src="../../.gitbook/assets/nekoray-profile-config_white.png" alt="SOCKS5 proxy settings in NekoRay">
  </picture>
</figure>

{% hint style="info" %}
See the [general setup guide](../getting-started.md) for help finding the connection details.
{% endhint %}

## Connect

Select the created profile and enable `Tun Mode` in the top bar. Once connected, system traffic will be routed through the configured proxy.

<figure>
  <picture>
    <source srcset="../../.gitbook/assets/nekoray-tun-mode-enable_black.png" media="(prefers-color-scheme: dark)">
    <img src="../../.gitbook/assets/nekoray-tun-mode-enable_white.png" alt="Enabling Tun Mode in NekoRay">
  </picture>
</figure>
