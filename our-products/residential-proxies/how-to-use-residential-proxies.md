---
icon: book-open-lines
---

# How to use Residential proxies

Let's review what the proxy connection strings from the "<mark style="color:purple;">Proxy list</mark>" field represent.

<figure><img src="../../.gitbook/assets/image (37).png" alt=""><figcaption></figcaption></figure>

<mark style="color:purple;">**resident.proxyshard.com**</mark> - This is the proxy connection IP address. It is presented as a DNS name because many IPv4 addresses (balancers) are behind this address, and IPv4 addresses may change.

<mark style="color:purple;">**8080**</mark> - Connection port. Ports do not affect IP address rotation; they only change to select the protocol type.

<mark style="color:purple;">**plan-limited-country-any-sid-nd1fmhz1mfxy**</mark> - Login. It is this long because it contains the selected country, region, and other parameters specified in the order settings. The login also contains <mark style="color:purple;">**sid-sy06witplz6x**</mark>, which is responsible for the IP. Changing one character will change the IP address.

<mark style="color:purple;">**7g6d8jd1t7in**</mark> - Connection password

{% hint style="info" %}
_When creating a proxy list, proxies are not saved in the order. When new proxies are created, old proxies do not stop working. This means you can create as many additional proxies as you need at any time without losing access to old ones._
{% endhint %}

