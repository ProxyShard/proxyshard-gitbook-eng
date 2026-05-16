---
icon: signal
---

# Mobile proxies

Mobile proxies are proxies hosted on modems and support <mark style="color:purple;">UDP</mark>. They offer a wide choice of locations and operators. They are an ideal solution for those who need to work through a specific operator and a specific device type.

{% hint style="danger" %}
1\) Device fingerprint switching (p0f) is not available in all countries. p0f switching does not work in: Germany, France, Indonesia, Poland (Orange), Ukraine (Lifecell). See the full list of restrictions on the [Restrictions](restrictions.md) page.

2\) Not available to users in Russia without using a VPN.
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

## Pros and cons of Mobile proxies

#### <mark style="color:green;">Pros:</mark>

* **Bypassing exchange and service restrictions**

Many crypto exchanges and DeFi platforms introduce regional restrictions. With mobile proxies, you can easily change geolocation by accessing platforms from real users' IP addresses. This helps work with platforms without the risk of being blocked.<br>

* **Increased anonymity and tracking protection**

The crypto industry is tightly controlled, and platforms often track user activity. Mobile proxies mask the real IP, prevent transaction tracking, and create the appearance of working from different devices and locations.<br>

* **Bot trading and automation**

Trading and arbitrage strategies require many accounts and automated interaction with exchanges. Mobile proxies allow bots to work without country-selection restrictions and protect against IP bans because they are not filtered by most fraud systems on the market.<br>

* **Multi-accounting and antidetect browsers**

Exchanges often use multi-accounting. Mobile proxies + antidetect browsers, such as Vision or Octo, allow each account to look unique and reduce the risk of bans.<br>

* **Access to ICO, IDO, and Airdrop**

Many projects distribute tokens only to users from specific regions. With proxies, you can change your location and participate in drops even if access is initially restricted.<br>

* **Increased security in P2P transactions**

When exchanging crypto on P2P platforms, such as Binance P2P or LocalBitcoins, Mobile proxies protect against scammers by hiding the real IP and preventing tracking attempts.

#### <mark style="color:red;">Cons:</mark>

* **High cost**

Mobile proxies are more expensive than Datacenter or Residential proxies. This is because they use IP addresses of real users rather than server infrastructure.

* **One active IP**

With Mobile proxies, you purchase one port that can be used with only one profile because only one IP address is assigned behind the port. This does not allow flexible simultaneous setup across several profiles, since all of them would use the same address.

{% hint style="info" %}
You can learn how to configure proxies in our [Setup guide](../setup-guides/getting-started.md) section.
{% endhint %}
