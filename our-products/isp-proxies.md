---
icon: fire
---

# ISP proxies

<mark style="color:purple;">ISP proxies</mark>, like <mark style="color:purple;">Datacenter</mark> proxies, are issued to one user only: no sharing, meaning no more than one user per address and no hidden sharing. The addresses are <mark style="color:purple;">IPv4</mark> and support <mark style="color:purple;">UDP</mark>.

<mark style="color:purple;">ISP proxies</mark> combine the benefits of both <mark style="color:purple;">Residential</mark> proxies and <mark style="color:purple;">Datacenter</mark> proxies. They are as stable and static as <mark style="color:purple;">Datacenter</mark> proxies, but they use IP addresses registered to home internet providers, like <mark style="color:purple;">Residential</mark> proxies.

This makes them a good option for Tier-1 sites and services that are sensitive to the <mark style="color:purple;">IP</mark> type. <mark style="color:purple;">UDP</mark> support also makes them suitable for WebRTC and other UDP-based workflows.

ISP proxies support <mark style="color:purple;">p0f</mark> network fingerprint spoofing.

{% embed url="https://dashboard.proxyshard.com/en/isp-proxy" %}

Step-by-step purchase and payment guide: [Purchasing ISP / Datacentre proxies](../site-navigation/buying-and-renewing/buying-datacenter-proxies.md).

Current product restrictions are listed on the [Restrictions](restrictions.md) page.

## Characteristics

| Parameter      | Value                              |
| -------------- | ---------------------------------- |
| IP type        | IPv4 (home ISP)                    |
| Sharing        | No - one IP per user               |
| Connection limit | 2,500 per IP                     |
| [UDP support](about-udp/) | ✓                          |
| [p0f support](p0f-spoofing.md) | ✓ (+$0.6 / IP per month) |
| Price          | **$2** / IP per month              |

## Available locations

| Country |
| ------- |
| 🇹🇷 Turkey |
| 🇺🇸 USA |
| 🇨🇿 Czechia |
| 🇺🇦 Ukraine |

{% hint style="info" %}
The list of locations is constantly expanding.
{% endhint %}

## How to purchase

1. Open `ISP Proxy`.
2. Select a country in `Proxy region`.
3. Enter the quantity in `Number of proxies`.
4. Enable `Auto renew` if you want the order to renew automatically.
5. Enable `Enable p0f settings` if required.
6. In `Total slots`, enter how many proxies should use p0f spoofing.
7. If you have a promo code, enter it in `Promocode` and click `Apply`.
8. Review the total and click `Buy now`.

<figure>
  <picture>
    <source srcset="../.gitbook/assets/isp-purchase-form_black.png" media="(prefers-color-scheme: dark)">
    <img src="../.gitbook/assets/isp-purchase-form_white.png" alt="Purchasing ISP proxies">
  </picture>
</figure>

Payment and renewal are covered in [Purchasing ISP / Datacentre proxies](../site-navigation/buying-and-renewing/buying-datacenter-proxies.md).

{% hint style="info" %}
After payment, allow 1-2 minutes for the order to synchronize and the proxies to start working.
{% endhint %}

## Order fields

<figure>
  <picture>
    <source srcset="../.gitbook/assets/isp-order-details_black.png" media="(prefers-color-scheme: dark)">
    <img src="../.gitbook/assets/isp-order-details_white.png" alt="ISP proxy order fields">
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

Any crypto exchanges, Polymarket, stable web scraping sessions, SEO monitoring, e-commerce price monitoring, marketplace checks, ad verification, brand monitoring, testing sites from a home-ISP ASN, QA of authorization and user scenarios, website availability monitoring, account management.

## Pros and cons of ISP proxies

#### <mark style="color:green;">Pros:</mark>

* **Real ISP addresses** - IPs are listed under real home internet providers (in geolocation databases the ASN type is provider, not hosting)
* **Reliable home-ISP carriers**
* **Wide channel with minimal latency**
* **Static addresses, one user only** - the IP does not change during the rental
* **p0f and UDP support**

#### <mark style="color:red;">Cons:</mark>

* **Price** - higher than Datacenter proxies
* **Number of available locations** - integration with real providers is extremely complex, but we keep expanding the list

{% hint style="info" %}
See the [setup guides](../setup-guides/getting-started.md) for proxy configuration instructions.
{% endhint %}
