---
icon: vial
---

# Proxy Tester

<mark style="color:purple;">ProxyShard Proxy Tester</mark> lets you quickly check whether your proxies work directly on the website, without installing additional software, and even check UDP support if you use SOCKS5.

{% embed url="https://proxyshard.com/proxy-tester" %}

***

<figure><img src="../.gitbook/assets/image (46) (1).png" alt=""><figcaption></figcaption></figure>

## How to use it

1. Open [proxyshard.com/proxy-tester](https://proxyshard.com/proxy-tester)
2. Paste proxies into the text field, one per line if there are several
3. Click <mark style="color:purple;">**Test Proxy**</mark>
4. Wait for the result in the <mark style="color:purple;">History</mark> table on the right

***

## Features

| Parameter             | Value                                                                                  |
| --------------------- | -------------------------------------------------------------------------------------- |
| **Protocols**         | HTTP, SOCKS5                                                                           |
| **Maximum proxies**   | up to 100                                                                              |
| **Limit**             | 1 request per minute                                                                   |
| **Supported formats** | `IP:PORT:LOGIN:PASSWORD`, `LOGIN:PASSWORD@IP:PORT`, and other standard formats         |

***

## What the result shows

After the check, the <mark style="color:purple;">**History**</mark> table displays:

| Field             | Description                                                                                                                                                                                                    |
| ----------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **Proxy**         | IP address through which the connection was made                                                                                                                                                               |
| **Response time** | Response time in milliseconds. The lower it is, the faster the proxy                                                                                                                                            |
| **Status code**   | HTTP response code. `200` means everything is OK                                                                                                                                                               |
| **Result**        | Final status: <mark style="color:green;">**Success**</mark> (works) or <mark style="color:red;">**Failed**</mark> (does not work). Also shows the connection type (HTTP/SOCKS5) and <mark style="color:purple;">UDP</mark> support if the proxy is SOCKS5. |

***

## If the proxy fails the check

This does not always mean the proxy is faulty. Check:

* Whether the format is correct (login\password\port)
* Whether the protocol is mixed up (HTTP \ SOCKS5)
* Whether 2-3 minutes have passed since purchase (DC\ISP proxies require up to 2 minutes for synchronization)
* Whether there is any blocking by your provider

If everything is correct but the check still fails, contact [support](../contact-us.md).

{% hint style="info" %}
For more detailed diagnostics, you can check the proxy through the command line. More details: [How to check proxy functionality](../faq-and-support/faq/how-to-check-proxy.md)
{% endhint %}
