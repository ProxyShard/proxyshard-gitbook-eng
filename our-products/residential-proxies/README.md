---
icon: house-signal
---

# Residential proxies

<mark style="color:purple;">Residential proxies</mark> are proxies hosted on real home devices, with <mark style="color:purple;">UDP</mark> support in <mark style="color:purple;">Standard\Unlimited</mark> packages. You can view the differences between products [<mark style="color:purple;">here</mark>](../../). They are ideal for working with many IP addresses from home ISPs and support detailed targeting down to operator selection. You can view product restrictions [here](../restrictions.md).

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

## Differences between Premium\Standard\Unlimited packages

### <mark style="color:purple;">Standard Residential</mark>

These proxies are a pool of devices that have passed non-strict address filtering and have an average number of devices and available countries. This plan is most often chosen for process automation tasks where <mark style="color:purple;">UDP</mark> support is also required.

<figure><img src="../../.gitbook/assets/image (5) (1).png" alt=""><figcaption></figcaption></figure>

### <mark style="color:purple;">Unlimited Residential</mark>

These proxies are a pool based on the "Standard" plan. They have the same countries and devices, but no limit on the amount of traffic used. Rental is available for "Day", "Half month", and "Month". There is a connection limit: no more than 5000 connections of any type are allowed (ESTAB\FIN\_WAIT and others). With a monthly subscription, it is also possible to increase the connection limit; contact Support for details. This plan is most often chosen for process automation tasks with high traffic consumption where <mark style="color:purple;">UDP</mark> support is also required.

### <mark style="color:purple;">Premium Residential</mark>

The Premium pool consists of some of the best IPs for different goals and tasks. The main advantages of the traffic are:

1. Flexible targeting, down to operator selection
2. A larger list of available countries, regions, and cities
3. A larger number of IP addresses

The downside of this plan is the absence of UDP and Unlimited plan options.

<figure><img src="../../.gitbook/assets/image (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

## Pros and cons of Residential proxies

#### <mark style="color:green;">Pros:</mark>

* **Bypassing exchange and service restrictions**

Many crypto exchanges and DeFi platforms introduce regional restrictions, for example Binance restricts access for users from certain countries. With Residential proxies, you can easily change geolocation by accessing platforms from real users' IP addresses. This helps work with platforms without the risk of being blocked.<br>

* **Increased anonymity and tracking protection**

The crypto industry is tightly controlled, and platforms often track user activity. Residential proxies mask the real IP, prevent transaction tracking, and create the appearance of working from different devices and locations.<br>

* **Bot trading and automation**

Trading and arbitrage strategies require many accounts and automated interaction with exchanges. Residential proxies allow bots to work without country-selection restrictions and protect against IP bans because they are not filtered by most fraud systems on the market.<br>

* **Multi-accounting and antidetect browsers**

Exchanges often use multi-accounting. Residential proxies + antidetect browsers, such as Vision or Octo, allow each account to look unique and reduce the risk of bans.<br>

* **Access to ICO, IDO, and Airdrop**

Many projects distribute tokens only to users from specific regions. With proxies, you can change your location and participate in drops even if access is initially restricted.<br>

* **Increased security in P2P transactions**

When exchanging crypto on P2P platforms, such as Binance P2P or LocalBitcoins, Residential proxies protect against scammers by hiding the real IP and preventing tracking attempts.

#### <mark style="color:red;">Cons:</mark>

* **High cost**

Residential proxies are more expensive than Datacenter alternatives. This is because they use IP addresses of real users rather than server infrastructure.

* **Possible speed and latency issues**

Because requests pass through real people's devices, **speed may vary** depending on network load, proxy location, and the end user's internet connection quality. For tasks that require high speed, such as bot trading, this can be critical. In these situations, Datacenter or ISP proxies are recommended.

* **Limited lifetime of a single IP**

IP addresses in Residential proxies may **change frequently** because users may disconnect their devices from the sharing network. Although we provide the option to increase the rental period by specifying TTL, it is not 100% guaranteed and usually does not exceed 2 days.

{% hint style="success" %}
These drawbacks are covered by [ISP proxies](../isp-proxies.md).
{% endhint %}

{% hint style="info" %}
You can learn how to configure proxies in our [Setup guide](../../setup-guides/getting-started.md) section.
{% endhint %}
