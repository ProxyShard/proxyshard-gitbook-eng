---
icon: house-signal
---

# Residential proxies

<mark style="color:purple;">Residential proxies</mark> are hosted on real home devices. They are ideal for working with many home-ISP IP addresses and support fine-grained targeting down to operator selection.\
You can review product restrictions [here](../restrictions.md).

{% hint style="warning" %}
Addresses are issued on real home IPs. A session can change at any moment if the device in the pool leaves the traffic-sharing network. If you need a **static IP**, see [Datacenter](../datacenter-proxies.md) or [ISP proxies](../isp-proxies.md).
{% endhint %}

## Plans

| Parameter            | [Standard](standard-residential.md) | [Unlimited](unlimited-residential-proxy.md) | [Premium](premium-residential.md) |
| -------------------- | ------------------------------------ | ------------------------------------------- | --------------------------------- |
| Pool size            | 600k — 750k                          | 600k — 750k (= Standard)                    | 2.8M — 3.2M                       |
| Max connections      | 35,000                               | 5,000                                       | —                                 |
| Max speed            | 75 Mbps                              | 75 Mbps                                     | 75 Mbps                           |
| UDP support          | ✓ (except USA)                       | ✓ (except USA)                              | ✗                                 |
| Unlimited plan       | ✗                                    | ✓                                           | ✗                                 |
| Billing              | Per GB (Pay as you go)               | Day / Half-month / Month                    | Per GB (Pay as you go)            |
| Price                | **$2 / GB**                          | **$30** / day · **$399** / half-month · **$699** / month | **$3 / GB**          |

## Available locations

An up-to-date list of countries, regions, cities and operators is on a separate page:

{% content-ref url="available-countries.md" %}
[available-countries.md](available-countries.md)
{% endcontent-ref %}

## **How to start using them?**

The cost of Residential proxies is calculated based on the number of gigabytes purchased for the order. To access country selection and other parameters, you need to [**purchase** ](https://dashboard.proxyshard.com/residential-main) an order. To do this, go to the page ![](<../../.gitbook/assets/image (70).png>) and specify the number of gigabytes.<br>

<figure><img src="../../.gitbook/assets/image (71).png" alt=""><figcaption></figcaption></figure>

## Settings field description

Inside the order, you can find several important items and options. Let's review them.

<figure><img src="../../.gitbook/assets/image (73).png" alt=""><figcaption></figcaption></figure>

<mark style="color:purple;">**Traffic used**</mark> - How much has been used \ How much has been purchased

<mark style="color:purple;">**Country**</mark> - Country selection

<mark style="color:purple;">**Region**</mark> - Country region selection

<mark style="color:purple;">**City**</mark> - Region city selection

<mark style="color:purple;">**ISP**</mark> - Provider type selection (temporarily unavailable)

<mark style="color:purple;">**Session**</mark> - Session type selection. Available options are <mark style="color:purple;">Sticky</mark> and <mark style="color:purple;">Rotate</mark>.

* <mark style="color:purple;">Sticky</mark> allows you to keep one IP address and depends on the selected TTL parameter.
* <mark style="color:purple;">Rotate</mark> changes the IP on every request. The IP range pool for <mark style="color:purple;">Sticky</mark> is smaller than for <mark style="color:purple;">Rotate</mark>.

<mark style="color:purple;">**Protocol**</mark> - HTTP/SOCKS. These are the main protocols for connecting to the proxy server.

<mark style="color:purple;">**TTL**</mark> - Appears when <mark style="color:purple;">Session - Sticky</mark> is selected and controls the IP address lifetime (<mark style="color:purple;">Time to live</mark>). The minimum possible <mark style="color:purple;">TTL</mark> is 60 seconds (1 minute).

<mark style="color:purple;">**Relay**</mark> **-** Set only if there are connection issues.

<mark style="color:purple;">**Username\Password\Host\Port**</mark> - Connection data. It is also generated in the proxy list and supports conditional formatting.

{% hint style="info" %}
Proxy ports do not affect the final address you receive. They are simply the port number for the remote proxy server and nothing more!
{% endhint %}

<mark style="color:purple;">**Traffic Statistics**</mark> - Per-minute statistics for used traffic. Display may be delayed by 10-20 minutes.

<figure><img src="../../.gitbook/assets/image (78).png" alt=""><figcaption></figcaption></figure>

At the end of the order, you can find request statistics for your Residential traffic. In rare cases, display delays of up to 20 minutes may occur.

## **Setup guide**

1. Specify the settings: <mark style="color:purple;">Country</mark>, <mark style="color:purple;">Region</mark>, and other parameters if needed.

<figure><img src="../../.gitbook/assets/image (4) (1) (1).png" alt=""><figcaption></figcaption></figure>

2. The <mark style="color:purple;">HTTP</mark> or <mark style="color:purple;">SOCKS5</mark> protocol is set at your discretion <mark style="color:$info;">(as a rule, SOCKS5 is used for UDP)</mark>.

<figure><img src="../../.gitbook/assets/image (7) (1).png" alt=""><figcaption></figcaption></figure>

3. The server (<mark style="color:purple;">Relay</mark>) is specified only if there are connection issues.

<figure><img src="../../.gitbook/assets/image (5) (1) (1).png" alt=""><figcaption></figcaption></figure>

4. Other parameters are set if needed.

<figure><img src="../../.gitbook/assets/image (6) (1).png" alt=""><figcaption></figcaption></figure>

5. Click the <img src="../../.gitbook/assets/image (76).png" alt="" data-size="line"> button and copy the proxies from <mark style="color:purple;">Proxy List</mark>.

<figure><img src="../../.gitbook/assets/image (75).png" alt=""><figcaption></figcaption></figure>

Later, if you need another country, specify new settings, click <img src="../../.gitbook/assets/image (77).png" alt="" data-size="line">, and reinstall the new proxies in the application from which the connection is made.

{% hint style="info" %}
Additional information about connection formatting is available at this [link](how-to-use-residential-proxies.md).
{% endhint %}

{% hint style="warning" %}
Proxies in "Proxy List" are not saved because this is a dynamic field. You can generate many proxies for different locations: old proxies will not stop working when new proxies are generated.
{% endhint %}

## What tasks they fit

Social media and multi-accounting, crypto exchanges (Binance, Bybit and others), Polymarket, web scraping, SEO monitoring, ad verification, e-commerce analytics, price monitoring, geo-targeted website testing.

## Pros and cons of Residential proxies

#### <mark style="color:green;">Pros:</mark>

* **Flexible billing** — Pay as you go or an unlimited subscription (Unlimited)
* **IP rotation** — change addresses on demand or by timer (TTL)
* **Wide geo-targeting** — select country, region, city and operator
* **Home-origin addresses** — IPs are registered to home ISPs
* **UDP support** — available on Standard and Unlimited (except the USA location)

#### <mark style="color:red;">Cons:</mark>

* **Possible speed drops** — depends on the internet quality of the end device; this is a specific of the product
* **Dynamic IP** — the address may change at any moment; if you need a static IP, see [ISP](../isp-proxies.md) or [Datacenter](../datacenter-proxies.md)
* **No p0f support** — planned, stay tuned for updates
* **UDP is unavailable in the USA location** on Standard and Unlimited

{% hint style="success" %}
No UDP or need a static address? [ISP proxies](../isp-proxies.md) cover both.
{% endhint %}

{% hint style="info" %}
You can learn how to configure proxies in our [Setup guide](../../setup-guides/getting-started.md) section.
{% endhint %}
