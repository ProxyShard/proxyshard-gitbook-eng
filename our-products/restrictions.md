---
icon: hand
---

# Restrictions

This page lists all current restrictions for our products.

***

## Blocking of specific websites

The following are unavailable through proxies:

* Banking websites (online banking, bank personal accounts)
* Government portals and websites, as well as websites in the `.gov` and `.edu` domains
* Payment processors: <mark style="color:purple;">Stripe</mark>, <mark style="color:purple;">PayPal</mark> (including <mark style="color:purple;">Yahoo</mark>)

This is a regulatory requirement aimed at limiting fraudulent activity. This restriction **does not apply** to crypto services and payment systems such as exchanges.

{% hint style="warning" %}
Applies to all products **except** [Mobile proxy](mobile-proxies.md).

Stripe and PayPal are available on Datacenter and ISP proxies.
{% endhint %}

Additional restrictions on Residential proxies:

* Microsoft and Apple services are unavailable on [Standard Residential](residential-proxies/standard-residential.md) / [Unlimited Residential](residential-proxies/unlimited-residential-proxy.md) / [Premium Residential](residential-proxies/premium-residential.md).

***

## UDP on Residential proxies

{% hint style="danger" %}
UDP does not work on [Standard Residential](residential-proxies/standard-residential.md) and [Unlimited Residential](residential-proxies/unlimited-residential-proxy.md) in the **US** location :flag\_us:
{% endhint %}

This is not our restriction. In early 2026, US providers prohibited incoming UDP connections without prior initiation from inside the network. Because of this, UDP Associate on proxies stopped working in this region.

Standard and Unlimited support UDP in other locations, subject to the general port restrictions.

[Premium Residential](residential-proxies/premium-residential.md) supports UDP in all locations except certain cities and devices running macOS or iOS.

### UDP port restriction for Standard and Unlimited

Standard and Unlimited currently allow UDP traffic only to destination ports `8443`, `8080`, `3478`, and `19302`. Other UDP port ranges are blocked. UDP remains completely unavailable in the US location.

Premium Residential is not affected by this port restriction. Only the existing exceptions for certain cities and macOS/iOS devices apply.

### `static_mode2` and macOS/iOS devices

`static_mode2` corresponds to `Static` in the `Session mode` field for Premium Residential. In this mode, the proxy keeps the selected device and does not switch the session to another device if the current one temporarily goes offline.

If the selected device is unavailable, the generated proxy may stop responding until the device returns or the `TTL` expires. To get another device immediately, generate a new proxy with `Generate proxy`.

Filtering by `Device OS: macOS` or `iOS` significantly reduces the available pool. Combining the OS filter with a city and provider may leave no matching devices, especially in Tier 2 and Tier 3 countries. UDP is also unavailable on some macOS/iOS devices and in certain cities.

***

## p0f switching on Mobile proxies

Device fingerprint spoofing (p0f) is unavailable in some countries and operators:

| Country                   | Operator        |
| ------------------------- | --------------- |
| United Kingdom :flag\_gb: | All operators   |
| Ireland :flag\_ie:        | Vodafone        |
| Germany :flag\_de:        | All operators   |
| Netherlands :flag\_nl:    | Vodafone        |
| France :flag\_fr:         | All operators   |
| Italy :flag\_it:          | Vodafone, WIND  |
| Poland :flag\_pl:         | Orange          |
| Indonesia :flag\_id:      | All operators   |
| New Zealand :flag\_nz:    | OneNZ           |
| Ukraine :flag\_ua:        | Life (Lifecell) |

In all other locations and operators, p0f switching works normally.

***

## Connection limit for Datacenter and ISP proxies

[Datacenter proxies](datacenter-proxies.md) and [ISP proxies](isp-proxies.md) have a limit of **2,500 connections per IP**.

***

## Closed ports

{% hint style="info" %}
Applies to all products. IMAP (993) is available on Datacenter and ISP proxies.
{% endhint %}

Connections through proxies to service ports that are often used for attacks on third-party services are blocked:

| Port | Protocol |
| ---- | -------- |
| 21   | FTP      |
| 22   | SSH      |
| 23   | Telnet   |
| 25   | SMTP     |

***

## Restrictions on Unlimited Residential proxies

* Basic connection limit = 5000. It can be increased; more details are available from [Support](../contact-us.md).
* Maximum speed per order = 75 **Mbps**
