---
icon: signal
---

# Mobile proxies

<mark style="color:purple;">Mobile proxies</mark> are hosted on routers with real SIM cards. The type and quality of the connection are identical to ordinary mobile internet through a cellular operator — exactly like on your smartphone. They support <mark style="color:purple;">UDP</mark> and offer a rich choice of locations and operators.

{% hint style="info" %}
**Mobile proxies work on any device.** The name "mobile" reflects only the connection method via a SIM card, not the type of end device. They work equally well on a PC, a laptop, or in an antidetect browser.
{% endhint %}

{% hint style="warning" %}
**A specific product — for those who understand why they need it.** Traffic goes through a real SIM card, so speed may vary — this is normal, not a malfunction. If you are not sure whether mobile proxies fit your task, ask in [live chat](../contact-us.md) or consider [ISP proxies](isp-proxies.md) (stable speed, home IPs) or [Residential proxies](residential-proxies/README.md) (a large pool, many sessions).
{% endhint %}

{% hint style="danger" %}
1\) Device fingerprint switching (p0f) is not available on all operators. See the full list of restrictions on the [Restrictions](restrictions.md) page.

2\) Not available to users in Russia without using a VPN.
{% endhint %}

{% embed url="https://dashboard.proxyshard.com/en/mobile-proxy" %}

## Characteristics

| Parameter      | Value                                 |
| -------------- | ------------------------------------- |
| IP type        | Mobile IPv4                           |
| Sharing        | No — one port per user                |
| Traffic        | Unlimited                             |
| UDP support    | ✓                                     |
| p0f support    | ✓ (not in all locations, see above)   |
| Price          | from **$4** / day · from **$55** / month |

## Available locations

| Country | Operators |
| ------- | --------- |
| 🇺🇸 USA | T-Mobile (5G), Verizon (5G, Colorado) |
| 🇬🇧 United Kingdom | O2, Vodafone |
| 🇩🇪 Germany | O2, Vodafone |
| 🇫🇷 France | SFR (5G), Bouygues Telecom (5G) |
| 🇮🇹 Italy | Vodafone (5G), WindTre (5G) |
| 🇪🇸 Spain | Digimobil, Movistar (5G), Vodafone (5G) |
| 🇵🇹 Portugal | NOS (5G) |
| 🇳🇱 Netherlands | Ziggo (5G), Odido (5G) |
| 🇮🇪 Ireland | Vodafone (5G), Three (5G) |
| 🇵🇱 Poland | T-Mobile (5G) |
| 🇺🇦 Ukraine | Lifecell, Vodafone, Kyivstar |
| 🇲🇩 Moldova | Moldcell, Moldtelecom |
| 🇨🇦 Canada | Rogers |
| 🇮🇩 Indonesia | Telkomsel |

{% hint style="info" %}
The list is regularly expanding. Up-to-date locations and pricing are on the purchase page [Mobile proxy](https://dashboard.proxyshard.com/en/mobile-proxy).
{% endhint %}

## **How do they work?**

To get started, you need to [**purchase**](https://dashboard.proxyshard.com/en/mobile-proxy) an order. Go to the page ![](<../.gitbook/assets/image (58).png>) and select a suitable country and operator.

<figure><img src="../.gitbook/assets/image (59).png" alt=""><figcaption></figcaption></figure>

## Order field description

Let's review the <mark style="color:purple;">order</mark> fields:

<figure><img src="../.gitbook/assets/image (20) (1).png" alt=""><figcaption></figcaption></figure>

<mark style="color:purple;">Proxy info</mark> - Product name

<mark style="color:purple;">Reset URL</mark> - Link for changing the IP address on the connection

<mark style="color:purple;">Login</mark> - Proxy login

<mark style="color:purple;">Password</mark> - Proxy password

<mark style="color:purple;">Order status</mark> - Order status. Possible statuses:

* <mark style="color:green;">**Active**</mark> - Active order
* <mark style="color:orange;">**On-Hold**</mark> - Waiting for payment after the rental period expires
* <mark style="color:red;">**Cancelled**</mark> - Cancelled order

<mark style="color:purple;">Proxy status</mark> - Proxy status. Possible statuses:

* <mark style="color:green;">**Active**</mark> - Active order
* <mark style="color:$danger;">Disconnected</mark> - Disconnected, inactive port

{% hint style="danger" %}
**After purchase or after there has been no activity on the port, it must be&#x20;**<mark style="color:$success;">**activated**</mark>**. If the proxy status is&#x20;**<mark style="color:$danger;">**Disconnected**</mark>**, the proxies will not work until you activate them!**

**You can activate the proxy through the&#x20;**<mark style="color:purple;">**Reset URL**</mark>**&#x20;or the&#x20;**<mark style="color:purple;">**Restart Proxy**</mark>**&#x20;button.**
{% endhint %}

<mark style="color:purple;">Next Due Date</mark> - Next charge date

<mark style="color:purple;">Copy proxy</mark> - Button for copying proxies to the clipboard

<mark style="color:purple;">Re-generate</mark> - Change the proxy password

<mark style="color:purple;">Restart</mark> - Start or change IP; equivalent to the <mark style="color:purple;">Reset URL</mark> address

## What tasks they fit

Social media and multi-accounting, mobile ad verification, mobile ad checks, most crypto exchanges, Polymarket, testing mobile sites and apps, web scraping of mobile site versions, SEO monitoring of mobile results, e-commerce monitoring of mobile prices, geo-targeted content testing, travel scraping of mobile fares, brand monitoring in the mobile environment.

## Pros and cons of Mobile proxies

#### <mark style="color:green;">Pros:</mark>

* **Choice of a specific operator** — connect through the exact cellular provider you need
* **IP change via Reset URL** — rotation no more than once a minute
* **p0f support** — available in most locations (see [Restrictions](restrictions.md))
* **UDP support**
* **Flexible rental period** — from one day to a month
* **One user per port** — one SIM card, one user

#### <mark style="color:red;">Cons:</mark>

* **Possible speed drops** when the operator's cell tower is overloaded — rare, but possible
* **A complex product for beginners** — we recommend checking with [Support](../contact-us.md) before purchase
* **p0f spoofing on macOS / iOS** reduces channel speed due to the complexity of the algorithm
* **Dynamic IP** — the address may change at the operator's initiative at any moment
* **One session at a time** — one port holds one IP. If you need to connect several devices _simultaneously_ (not one after another, but at the same moment), buy a separate port or consider [Residential proxies](residential-proxies/README.md)

{% hint style="info" %}
You can learn how to configure proxies in our [Setup guide](../setup-guides/getting-started.md) section.
{% endhint %}
