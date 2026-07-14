---
icon: hand
---

# Restrictions

This page lists all current restrictions for our products.

***

## Blocking of specific websites

The following are unavailable through proxies:

* Banking websites (online banking, bank personal accounts)
* Government portals and websites
* Payment processors: <mark style="color:purple;">Stripe</mark>, <mark style="color:purple;">PayPal</mark> (including <mark style="color:purple;">Yahoo</mark>)

This is a regulatory requirement aimed at limiting fraudulent activity. The block **does not apply** to crypto services and payment systems such as exchanges.

{% hint style="warning" %}
Applies to all products **except** [Mobile proxy](mobile-proxies.md).

Stripe and PayPal are available on Datacenter and ISP proxies.
{% endhint %}

***

## UDP on Residential proxies (US)

{% hint style="danger" %}
UDP does not work on [Residential proxies](residential-proxies/) (**including Unlimited**) in the **US** location :flag\_us:
{% endhint %}

This is not our restriction. In early 2026, US providers prohibited incoming UDP connections without prior initiation from inside the network. Because of this, UDP Associate on proxies stopped working in this region.

UDP works without issues in all other locations.

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

## Closed ports

{% hint style="info" %}
Applies to all products. IMAP (993) is available on DC\ISP proxies.
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
