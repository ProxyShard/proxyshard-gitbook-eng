---
icon: triple-chevrons-up
---

# Unlimited Residential

<mark style="color:purple;">Unlimited Residential</mark> is based on the [Standard Residential](standard-residential.md) pool - the same devices, the same countries, the same IP range. The key difference: **no traffic limits**. This plan pays off where Standard with per-gigabyte billing becomes expensive.

{% embed url="https://dashboard.proxyshard.com/en/residential-unlimited" %}

Step-by-step purchase and payment guide: [Purchasing residential proxies](../../site-navigation/buying-and-renewing/buying-residential-proxies.md).

## Characteristics

| Parameter                | Value                                       |
| ------------------------ | ------------------------------------------- |
| Pool size                | 300,000 - 400,000 devices (= Standard)      |
| Max connections          | 5,000                                       |
| Max speed per order      | 75 Mbps                                     |
| [UDP support](../about-udp/) | Available (except in the USA; [port restrictions apply](../restrictions.md)) |
| [Device OS filtering](../p0f-spoofing.md) | Not available |
| Billing                  | Day / Half-month / Month                    |
| Price                    | **$30** / day · **$199** / week · **$399** / half-month · **$699** / month |

{% hint style="warning" %}
Unlimited plans support up to 5,000 concurrent connections. The limit includes every connection state, such as `ESTAB`, `FIN_WAIT`, and others. It cannot currently be increased. Dedicated plans are still in development and are not yet available.
{% endhint %}

## Suitable use cases

- Automation with high traffic consumption
- Long-running processes where counting gigabytes is impractical
- Tasks that require <mark style="color:purple;">UDP / WebRTC</mark> support

{% hint style="info" %}
Need to pay per gigabyte instead of a subscription? See [Standard Residential](standard-residential.md).\
Need a larger pool with fine targeting? See [Premium Residential](premium-residential.md).
{% endhint %}

You can review the product restrictions [here](../restrictions.md).
