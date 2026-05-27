---
description: Popular questions about our products and pricing
icon: circle-question
---

# Popular product questions

{% hint style="warning" %}
**Information is current as of June 2026.** The list of products, locations, operators, and prices may change, please double-check the current pages in the [dashboard](https://dashboard.proxyshard.com/) before purchase.
{% endhint %}

***

## 1. Which products support p0f spoofing?

Network fingerprint spoofing (<mark style="color:purple;">p0f</mark>) is supported on:

* <mark style="color:purple;">**Datacenter**</mark> proxies
* <mark style="color:purple;">**ISP**</mark> proxies
* <mark style="color:purple;">**Mobile**</mark> proxies (not in every location / operator)

For Mobile proxies there are exceptions by country and operator, the full list is in the [p0f switching on Mobile proxies](../../our-products/restrictions.md#p0f-switching-on-mobile-proxies) section.

On <mark style="color:purple;">Residential</mark> and <mark style="color:purple;">Unlimited Residential</mark> proxies, p0f spoofing **is not supported**.

More about the technology: [Network fingerprint spoofing (p0f)](../../our-products/p0f-spoofing.md).

***

## 2. Which products support UDP?

UDP is supported on **all** products, except:

* **Residential** and **Unlimited Residential** proxies in the <mark style="color:purple;">**US**</mark> :flag\_us: location (a restriction from American providers since early 2026)
* **Premium Residential** proxies in **all locations**

On Datacenter, ISP, Mobile, and non-US Residential proxies, UDP works normally.

More info: [About the UDP protocol](../../our-products/about-udp/) and [Proxies with UDP](../../our-products/udp-proxies.md).

***

## 3. Is QUIC supported?

Yes, **QUIC is supported** on every proxy where UDP works (see question 2). However, your software also needs to support QUIC.

For example, in the [Vision browser](../../setup-guides/antidetect-browsers/vision-browser.md) you need to turn on the <mark style="color:purple;">**Enable QUIC**</mark> option in settings.

***

## 4. Which proxies are static (with a fixed IP)?

Fully **static** proxies (the same IP for the entire rental period) are only:

* <mark style="color:purple;">**Datacenter**</mark> proxies
* <mark style="color:purple;">**ISP**</mark> proxies

Residential and Mobile proxies are rotational by nature, their IP changes during use (see questions 11 and 14 below).

***

## 5. Which products are individual (one order = one user)?

Sold without sharing, on a one-per-user basis:

* <mark style="color:purple;">**Datacenter**</mark> proxies - one IP per user
* <mark style="color:purple;">**ISP**</mark> proxies - one IP per user
* <mark style="color:purple;">**Mobile**</mark> proxies - one port (one SIM card) per user

Residential proxies work through a shared address pool and are not individual.

***

## 6. I just bought / renewed a Datacenter or ISP proxy - it doesn't work

After purchasing or renewing a Datacenter or ISP order, **1-2 minutes** are needed to sync the order with the proxy server. If after a few minutes the proxy still doesn't respond, please contact our [Support](../../contact-us.md).

***

## 7. How long do I have to renew a Datacenter / ISP proxy?

Renewal for Datacenter and ISP proxies is available **only within 3 days** after the rental period ends.

{% hint style="danger" %}
If the order isn't renewed within 3 days, **it is deleted permanently**. You won't be able to recover the same IP address or order after that.
{% endhint %}

We recommend enabling the <mark style="color:purple;">**Auto renew**</mark> option in the order settings so renewal is charged from your balance automatically.

***

## 8. I just bought a Mobile proxy - it doesn't work

After purchasing a Mobile proxy, the port needs to be **activated** in one of these ways:

* The <mark style="color:purple;">**Restart proxy**</mark> button in the order settings
* Following the personal **Reset URL** link from the order

{% hint style="warning" %}
If you don't use the proxy, after **3 hours** the port goes into power-saving mode. This limit can't be removed, to bring the proxy back simply hit Restart proxy or the Reset URL again.
{% endhint %}

***

## 9. Are Mobile proxies unlimited in traffic?

Yes, **Mobile proxies are unlimited in traffic**. There's no cap on the volume of downloaded gigabytes, you only pay for the port rental period.

***

## 10. Why does my IP change periodically on Mobile proxies?

Mobile proxies sit on our mobile farms and operate via real SIM cards. IP address changes depend entirely on the **carrier**:

* On average the carrier refreshes the address **once a day**.
* The carrier may initiate a pool change at any moment, and the address will change earlier.

This is a feature of how mobile internet works and **is outside our control**. If you need rotation on a timer or by hotkey, use the [IP Rotation feature in our extension](../../our-products/proxyshard-extension.md).

***

## 11. What are TTL and Sticky on Residential proxies?

* <mark style="color:purple;">**TTL**</mark> (Time-To-Live) is the session "lifetime" in seconds. Once TTL expires, the proxy chain is rebuilt and you get a new IP. Range: from 60 to 86400 seconds.
* <mark style="color:purple;">**Sticky / Random**</mark> is the session mode. <mark style="color:purple;">Sticky</mark> tries to hold the same IP within TTL, <mark style="color:purple;">Random</mark> issues a random IP on every new connection.

Full description of all Residential proxy order parameters: [How to use Residential proxies](../../our-products/residential-proxies/how-to-use-residential-proxies.md).

***

## 12. What is the Relay parameter on Residential proxies?

<mark style="color:purple;">**Relay**</mark> is the balancing (fallback) server through which your traffic enters the pool of Residential devices. The Relay is chosen based on **where you're connecting from**, to make the route shorter and more stable.

* By default, <mark style="color:purple;">**EU**</mark> is used
* Also available: <mark style="color:purple;">**RU**</mark> and <mark style="color:purple;">**UA**</mark>

{% hint style="info" %}
The Relay choice **does not** affect the endpoint IP country, it's purely a balancing server. The endpoint country is set by the <mark style="color:purple;">Country</mark> parameter in the order settings.
{% endhint %}

***

## 13. What happens if I run out of traffic on Residential proxies? Does it expire?

No, **traffic does not expire** - it stays available until you spend it. If the traffic runs out, the proxies temporarily stop working, but it's enough to click <mark style="color:purple;">**Add traffic**</mark> in the top-right corner of the order, top up the package, and the proxies will start working again immediately.

***

## 14. Why does my IP change periodically on Residential proxies?

Residential proxies are hosted on the home devices of real users who take part in a paid traffic-sharing program. These devices may:

* leave the sharing network (for example, the owner turned the device off),
* experience signal / connectivity issues.

Any of these reasons leads to an IP change during the session. We don't manage the devices in the pool directly.

{% hint style="info" %}
**If a session is misbehaving or dropping often**, there are two ways to change the address:

**Method 1.** Click <mark style="color:purple;">**Generate proxy**</mark> in the order, you'll get a new connection string.

**Method 2.** Change the <mark style="color:purple;">**SID**</mark> manually in the connection string. For example, in this string:

```
relay-eu.proxyshard.com:8080:plan-limited-country-any-sid-8dbryym0a32i:7nnrpl63344545gx
```

the login contains a fragment `sid-8dbryym0a32i`. If you change one character in it, for example to `sid-8dbryym0a324`, the IP address will change. The same thing happens "under the hood" when you click <mark style="color:purple;">Generate proxy</mark>.

<mark style="color:purple;">SID</mark> is responsible for picking the device and the IP for your session.
{% endhint %}

***

## 15. Why do I get Google / Cloudflare captchas often?

Google and Cloudflare captchas are usually **not related to the proxy itself**, but to the browser fingerprint. The most common causes:

* An outdated or low-quality antidetect browser is used
* The profile has a "sticky" / repeating fingerprint
* The browser leaks mismatched parameters (timezone, language, WebRTC, etc.)

**What to do:** generate new profile fingerprints whenever there's an issue, use quality antidetect solutions (for example the [Vision browser](../../setup-guides/antidetect-browsers/vision-browser.md)), and verify leaks at [IP Checker](../../our-products/ip-checker.md).

***

## 16. What restrictions do you have on the proxies?

On all products the following are blocked:

* Service ports often used for brute-force attacks: **22 (SSH), 23 (Telnet), 25 (SMTP)** and several others.
* Banking and government websites, and **Stripe** and **PayPal** payment processors (this is a regulatory requirement).

The full list of restrictions by port, by site, by product-specific exceptions, and the limits for Unlimited Residential proxies are in the [Limitations](../../our-products/restrictions.md) section.

***

## 17. Which payment systems are supported?

We accept payments via:

* <mark style="color:purple;">**Stripe**</mark> - bank cards, minimum payment **$5**.
* <mark style="color:purple;">**NowPayments**</mark> - cryptocurrencies (BTC, LTC, USDT, and others).

{% hint style="info" %}
**About crypto payments through NowPayments:**

* Payment via **BTC** or **LTC** may take up to **1 hour** to process, this depends on network confirmations, not on our system.
* Payment via **USDT** requires a minimum payment of **$15** and a fee on the client side. This is a NowPayments platform requirement, we have no influence over these terms.
{% endhint %}

***

## 18. Do you have an API?

Yes, we have a full user API.

* **Specification and Try-it-out:** the [User API](../../) section in this GitBook.
* **Usage examples in Russian:** [github.com/ProxyShard/proxyshard-api-examples-ru](https://github.com/ProxyShard/proxyshard-api-examples-ru)
* **Usage examples in English:** [github.com/ProxyShard/proxyshard-api-examples](https://github.com/ProxyShard/proxyshard-api-examples)

***

## 19. Which countries are available for Residential proxies?

Residential proxies cover **most countries in the world**. The full up-to-date list with cities and regions is on the [Available countries list](../../our-products/residential-proxies/available-countries.md) page.

***

## 20. Which countries are available for ISP proxies?

As of June 2026, ISP proxies are available in:

| Country | Region / Operator |
| ------- | ----------------- |
| 🇨🇿 Czech Republic | - |
| 🇺🇸 USA | Pennsylvania |
| 🇹🇷 Turkey | Türk Telekom |

***

## 21. Which countries are available for Datacenter proxies?

As of June 2026:

* 🇲🇩 Moldova
* 🇺🇦 Ukraine
* 🇳🇱 Netherlands
* 🇩🇪 Germany
* 🇵🇱 Poland
* 🇺🇸 USA (coming soon)

***

## 22. Which countries and operators are available for Mobile proxies?

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

The list is regularly expanded. The current locations and pricing are on the [Mobile proxy](https://dashboard.proxyshard.com/en/mobile-proxy) purchase page.

***

## 23. What are your prices?

| Product | Price | Period / unit |
| ------- | ----- | ------------- |
| **ISP** | **$2** | per IP per month (+$0.6 for p0f) |
| **Residential** | **$2** | per GB |
| **Premium Residential** | **$3** | per GB |
| **Datacenter** | **$0.3 / $0.4 / $0.7 / $1.2** | 3 days / week / half-month / month (+$0.3 for p0f, available with a rental of one month or more) |
| **Unlimited Residential** | **$30 / $199 / $399 / $699** | day / week / half-month / month |
| **Mobile** | **from $4 / day, $55 / month** | depends on country and operator |

{% hint style="info" %}
The exact price and available periods for each plan are shown directly on the purchase page in the [dashboard](https://dashboard.proxyshard.com/).
{% endhint %}

***

{% hint style="success" %}
Didn't find the answer to your question? Contact our [Support](../../contact-us.md), we'll reply as soon as possible.
{% endhint %}
