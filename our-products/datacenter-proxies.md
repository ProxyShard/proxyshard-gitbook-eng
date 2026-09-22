---
icon: server
---

# Datacenter proxies

<mark style="color:purple;">Datacenter proxies</mark> are designed for high-load tasks. They are hosted in data centers and provide high speed and stable connections.

<mark style="color:purple;">Datacenter proxies</mark>, like <mark style="color:purple;">ISP</mark> proxies, are issued to one user only: no sharing, meaning no more than one user per address and no hidden sharing. The addresses are <mark style="color:purple;">IPv4</mark> and also support <mark style="color:purple;">UDP</mark>.

{% embed url="https://dashboard.proxyshard.com/en/datacenter-proxy" %}

Step-by-step purchase and payment guide: [Purchasing Datacenter proxies](../site-navigation/buying-and-renewing/buying-datacenter-proxies.md).

Current product restrictions are listed on the [Restrictions](restrictions.md) page.

## Characteristics

| Parameter      | Value                                                                     |
| -------------- | ------------------------------------------------------------------------- |
| IP type        | IPv4                                                                      |
| Sharing        | No - one IP per user                                                      |
| Connection limit | 2,500 per IP                                                            |
| [UDP support](about-udp/) | ✓                                                                 |
| [p0f support](p0f-spoofing.md) | ✓ (with monthly rental, +$0.3 / IP)                          |
| Price          | **$0.3** / 3 days · **$0.4** / week · **$0.7** / half-month · **$1.2** / month |

## Available locations

* 🇩🇪 Germany
* 🇫🇷 France
* 🇬🇧 United Kingdom
* 🇲🇩 Moldova
* 🇳🇱 Netherlands
* 🇵🇱 Poland
* 🇺🇦 Ukraine
* 🇪🇸 Spain

## How to purchase

1. Open `Datacenter Proxy`.
2. Select a country in `Proxy region`.
3. Select the rental period in `Billing cycle`.
4. Enter the quantity in `Number of proxies`.
5. Enable `Auto renew` if you want the order to renew automatically.
6. Enable `Enable p0f settings` if required.
7. In `Total slots`, enter how many proxies should use p0f spoofing.
8. If you have a promo code, enter it in `Promocode` and click `Apply`.
9. Review the total and click `Buy now`.

<figure>
  <picture>
    <source srcset="../.gitbook/assets/datacenter-purchase-form_black.png" media="(prefers-color-scheme: dark)">
    <img src="../.gitbook/assets/datacenter-purchase-form_white.png" alt="Purchasing Datacenter proxies">
  </picture>
</figure>

Payment and renewal are covered in [Purchasing Datacenter proxies](../site-navigation/buying-and-renewing/buying-datacenter-proxies.md).

{% hint style="info" %}
After payment, allow 1-2 minutes for the order to synchronize and the proxies to start working.
{% endhint %}

## Order fields

<figure>
  <picture>
    <source srcset="../.gitbook/assets/datacenter-order-details_black.png" media="(prefers-color-scheme: dark)">
    <img src="../.gitbook/assets/datacenter-order-details_white.png" alt="Datacenter proxy order fields">
  </picture>
</figure>

* `Status` shows the order state: `Active`, `On-hold`, or `Canceled`.
* `Product tag` adds a label that you can use to find the order in product lists.
* `User ID` identifies the order internally and may be requested by support.
* `Proxy Region` shows the selected country.
* `p0f slots` shows the active p0f slots and the change scheduled for the next billing period.
* `Username` and `Password` contain the credentials. `Regenerate` creates a new password, so existing proxy strings stop working.
* `Billing cycle`, `Next due date`, `Price`, and `Next charge` show the rental term and the next payment.
* `Auto-renew proxy` controls automatic renewal. The same settings are available through `Manage renewal`.
* `p0f` and `Buy p0f slots` open the fingerprint settings and the purchase of additional slots.
* In `Proxy List`, you can select `HTTP` or `SOCKS5`, change the proxy string format, copy the list with `Copy all`, or download it with `Export All`.

{% hint style="danger" %}
An order with the `Canceled` status cannot be restored. This status is assigned after three days without payment.
{% endhint %}

## What tasks they fit

Most crypto exchanges, Polymarket and platforms, mass web scraping of simple sites, fast collection of public data, availability and uptime checks, SEO scraping, price monitoring on weakly protected sites, load testing of your own systems, scraping catalogs and directories, API request automation.

## Pros and cons of Datacenter proxies

#### <mark style="color:green;">Pros:</mark>

* **Wide channel in a Tier 4 data center** with the lowest possible latency
* **Static addresses, one user only** - the IP does not change during the rental
* **p0f and UDP support**
* **Low price** - the most affordable option among all products
* **Flexible rental periods** - from 3 days to a month
* **High stability and availability**

#### <mark style="color:red;">Cons:</mark>

* **Easily detected** - major geolocation databases tag them DC / Hosting; this is normal and we don't hide it
* **Not suitable for some platforms** - certain resources block DC addresses outright (for example, the DePIN projects Grass and Gradient)

{% hint style="success" %}
These restrictions are bypassed with [ISP proxies](isp-proxies.md).
{% endhint %}

{% hint style="info" %}
See the [setup guides](../setup-guides/getting-started.md) for proxy configuration instructions.
{% endhint %}
