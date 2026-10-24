# Getting started

The ProxyShard API lets you retrieve profile and order information, manage proxies, and perform other operations from your applications and scripts.

## Where to get an API key

You can open the API key tab using this [direct link](https://dashboard.proxyshard.com/en/profile?tab=api-key). To reach it through the dashboard menu:

1. In the bottom-left corner, click the three-dot button next to your profile.
2. Select `Settings`.
3. Open the `API` tab.
4. Click `Copy` to copy the key.

<figure>
  <picture>
    <source srcset="../.gitbook/assets/proxyshard-api-key_black.png" media="(prefers-color-scheme: dark)">
    <img src="../.gitbook/assets/proxyshard-api-key_white.png" alt="Getting an API key from the ProxyShard dashboard">
  </picture>
</figure>

{% hint style="warning" %}
Do not publish your API key or share it with anyone. `Change API Key` creates a new key. After changing it, update the key in all scripts and integrations.
{% endhint %}

## Authentication

API base URL: `https://user-api.proxyshard.com`.

For methods that require authentication, send the API key in the request header:

```http
Authorization: Bearer <API_KEY>
```
