---
icon: server
---

# Datacenter proxies

<mark style="color:purple;">Datacenter proxies</mark> are proxies for high-load scenarios and tasks. They are usually hosted in data centers and provide the highest speed and stability.

<mark style="color:purple;">Datacenter proxies</mark>, like <mark style="color:purple;">ISP</mark> proxies, are issued to one user only: no sharing, meaning no more than one user per address and no hidden sharing. The addresses are <mark style="color:purple;">IPv4</mark> and also support <mark style="color:purple;">UDP</mark>.

## **How do they work?**

Inside the order, you can find several important items and options. Let's review them:

You can purchase them on the [Datacenter proxy](https://dashboard.proxyshard.com/en/datacenter-proxy) page. There, you need to specify the <mark style="color:purple;">Country</mark>, <mark style="color:purple;">Rental period</mark>, and <mark style="color:purple;">Quantity</mark>. If needed, you can enable <mark style="color:purple;">Auto renew</mark> for automatic renewal.

<figure><img src="../.gitbook/assets/image (66).png" alt=""><figcaption></figcaption></figure>

{% hint style="info" %}
After purchase, proxies start working within 1-2 minutes because the database needs to synchronize with the proxy server.
{% endhint %}

## Order field description

Let's review the <mark style="color:purple;">Order</mark> fields:

<figure><img src="../.gitbook/assets/image (67).png" alt=""><figcaption></figcaption></figure>

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

## Pros and cons of Datacenter proxies

#### <mark style="color:green;">**Pros**</mark>_<mark style="color:green;">**:**</mark>_

* **High speed**

Achieved by hosting addresses in large data centers, where 10 Gigabit broadband connectivity is possible. Ideal for high-load applications and tasks.<br>

* **Low cost**

Compared with other products, they have a very low cost because of their large quantity and easy scalability.<br>

* **Ideal for many tasks**

Suitable for all tasks that do not require masking as a real user. Such tasks may include website parsing, working with various exchanges, Facebook, Twitter, and other scenarios where there is no strict policy regarding address origin.

#### <mark style="color:red;">**Cons:**</mark>

* **Easy detectability**

These proxies may not be suitable for some tasks where DC addresses are filtered, for example DePIN projects. Such projects filter out these addresses at an early stage. For these cases, only <mark style="color:purple;">ISP</mark> / <mark style="color:purple;">Mobile</mark> / <mark style="color:purple;">Residential proxies</mark> are suitable.

{% hint style="success" %}
These drawbacks are covered by [ISP proxies](isp-proxies.md).
{% endhint %}

{% hint style="info" %}
You can learn how to configure proxies in our [Setup guide](../setup-guides/getting-started.md) section.
{% endhint %}
