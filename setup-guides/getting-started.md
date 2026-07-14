---
icon: clipboard-list
---

# Setup guide

## **Adding a proxy list from the order to programs**

To add proxies to different programs, open your [order](https://dashboard.proxyshard.com/products) on the website and copy the proxies:

{% hint style="warning" %}
**Please note that in all examples, the connection is made through&#x20;**<mark style="color:purple;">**SOCKS5**</mark>**.** \
\
**To find the connection port for:**\
\
<mark style="color:purple;">**Datacenter\ISP**</mark> - set the switch to <mark style="color:purple;">SOCKS5</mark> in the <mark style="color:purple;">Proxy list</mark> field

<p align="center"><img src="../.gitbook/assets/image (40).png" alt=""></p>

<mark style="color:purple;">**Residential proxy**</mark> - in the order settings, set "<mark style="color:purple;">Protocol</mark>" to <mark style="color:purple;">SOCKS5</mark>

<p align="center"><img src="../.gitbook/assets/image (42).png" alt="" data-size="original"></p>

<mark style="color:purple;">**Mobile proxy**</mark> - no additional actions are required in the order; the port connection works through both <mark style="color:purple;">HTTP</mark> and <mark style="color:purple;">SOCKS5</mark>
{% endhint %}

## Example for <mark style="color:purple;">Datacenter/ISP</mark> proxies

Open the [order](https://dashboard.proxyshard.com/products) and copy the proxy from <mark style="color:purple;">Proxy List</mark>.

<figure><img src="../.gitbook/assets/image (35).png" alt=""><figcaption></figcaption></figure>

212.14.123.184 - proxy connection IP address

22334 - proxy connection port

KDKKKEI - proxy connection login

KDKKEIID3 - proxy password



## Example for <mark style="color:purple;">Residential proxies</mark>:

Specify the required proxy parameters, for example country/protocol, and click "<mark style="color:purple;">Generate proxy</mark>".

<figure><img src="../.gitbook/assets/image (260).png" alt=""><figcaption></figcaption></figure>

Copy the generated proxies from <mark style="color:purple;">Proxy List</mark>, or copy the individual connection fields if the program does not support pasting a full line.&#x20;

Below is a screenshot showing which fields correspond to "Server":"Port":"Login":"Password".

<figure><img src="../.gitbook/assets/image (36).png" alt=""><figcaption></figcaption></figure>
