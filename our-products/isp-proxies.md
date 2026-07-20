---
icon: fire
---

# ISP proxies

<mark style="color:purple;">ISP proxies</mark>, like <mark style="color:purple;">Datacenter</mark> proxies, are issued to one user only: no sharing, meaning no more than one user per address and no hidden sharing. The addresses are <mark style="color:purple;">IPv4</mark> and support <mark style="color:purple;">UDP</mark>.

<mark style="color:purple;">ISP proxies</mark> combine the benefits of both <mark style="color:purple;">Residential</mark> proxies and <mark style="color:purple;">Datacenter</mark> proxies. They are as stable and static as <mark style="color:purple;">Datacenter</mark> proxies, but they use IP addresses registered to home internet providers, like <mark style="color:purple;">Residential</mark> proxies.

This makes them one of the best options for working with Tier-1 sites and services that are sensitive to the <mark style="color:purple;">IP</mark> type. And with <mark style="color:purple;">UDP</mark> support they become practically undetectable.\
\
A recent update for <mark style="color:purple;">ISP</mark> proxies added the ability to switch the fingerprint (<mark style="color:purple;">p0f</mark>).

{% embed url="https://dashboard.proxyshard.com/en/isp-proxy" %}

## Characteristics

| Parameter      | Value                              |
| -------------- | ---------------------------------- |
| IP type        | IPv4 (home ISP)                    |
| Sharing        | No — one IP per user               |
| Connection limit | 2,500 per IP                     |
| UDP support    | ✓                                  |
| p0f support    | ✓ (+$0.6 / IP per month)           |
| Price          | **$2** / IP per month              |

## Available locations

| Country |
| ------- |
| 🇹🇷 Turkey |
| 🇺🇸 USA |
| 🇨🇿 Czechia |

{% hint style="info" %}
The list of locations is constantly expanding.
{% endhint %}

## **How do they work?**

Inside the order, you can find several important items and options. Let's review them:

You can purchase them on the [ISP proxy](https://dashboard.proxyshard.com/en/isp-proxy) page. There, you need to specify the <mark style="color:purple;">Country</mark>, <mark style="color:purple;">Rental period</mark>, and <mark style="color:purple;">Quantity</mark>. If needed, you can enable <mark style="color:purple;">Auto renew</mark> for automatic renewal.

<figure><img src="../.gitbook/assets/image (57).png" alt=""><figcaption></figcaption></figure>

{% hint style="info" %}
After purchase, proxies start working within 1-2 minutes because the database needs to synchronize with the proxy server.
{% endhint %}

## Order field description

Let's review the <mark style="color:purple;">Order</mark> fields:

<mark style="color:purple;">User ID</mark> - This User ID is used for internal order identification. Sometimes we request it when you contact technical support.

<mark style="color:purple;">Status</mark> - Order status. Possible statuses:

* <mark style="color:green;">**Active**</mark> - Active order
* <mark style="color:orange;">**On-Hold**</mark> - Waiting for payment after the rental period expires
* <mark style="color:red;">**Cancelled**</mark> - Cancelled order

{% hint style="danger" %}
Orders with the "<mark style="color:$danger;">**Cancelled**</mark>" status **cannot be restored** three days after the rental period ends.
{% endhint %}

<mark style="color:purple;">Price</mark> - Product price per month

<mark style="color:purple;">Username</mark> - Proxy login

<mark style="color:purple;">Password</mark> - Proxy password

<mark style="color:purple;">Next Due Date</mark> - Next charge date

<mark style="color:purple;">Copy proxy</mark> - Button for copying proxies to the clipboard

<mark style="color:purple;">HTTP/SOCKS</mark> - Proxy protocol type selection

<mark style="color:purple;">Re-generate</mark> - Change the proxy password

<mark style="color:purple;">Auto renew</mark> - Toggle for enabling/disabling monthly product renewal <mark style="color:purple;">(funds are charged from the account balance on the date specified at purchase)</mark>

## What tasks they fit

Any crypto exchanges, Polymarket, stable web scraping sessions, SEO monitoring, e-commerce price monitoring, marketplace checks, ad verification, brand monitoring, testing sites from a home-ISP ASN, QA of authorization and user scenarios, website availability monitoring, account management.

## Pros and cons of ISP proxies

#### <mark style="color:green;">Pros:</mark>

* **Real ISP addresses** — IPs are listed under real home internet providers (in geolocation databases the ASN type is provider, not hosting)
* **Reliable home-ISP carriers**
* **Wide channel with minimal latency**
* **Static addresses, one user only** — the IP does not change during the rental
* **p0f and UDP support**

#### <mark style="color:red;">Cons:</mark>

* **Price** — higher than Datacenter proxies
* **Number of available locations** — integration with real providers is extremely complex, but we keep expanding the list

{% hint style="info" %}
You can learn how to configure proxies in our [Setup guide](../setup-guides/getting-started.md) section.
{% endhint %}
