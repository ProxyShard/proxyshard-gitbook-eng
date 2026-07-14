---
icon: flask-vial
---

# How to check whether a proxy works

If the proxies do not connect, or you want to make sure everything is working, there are two simple ways to check.

***

## Method 1: Proxy Tester on the website

The fastest option.&#x20;

Open our [Proxy Tester](https://proxyshard.com/proxy-tester), paste the proxy into the field, and click **Test Proxy**.

Read more about features and formats in the [Proxy Tester](../../our-products/proxy-tester.md) article.

***

## Method 2: Check via curl (command line)

This method is suitable when you need to quickly check the connection directly from your computer. It works on Windows, macOS, and Linux.

### Windows

Open Command Prompt: press <mark style="color:blue;">WIN+R</mark>, enter `cmd`, and press Enter.

### macOS / Linux

Open Terminal (on macOS, via Spotlight or the Applications > Utilities folder).

***

### Checking an HTTP proxy

```bash
curl -x http://USERNAME:PASSWORD@PROXY_IP:PORT -I https://www.google.com
```

Example with real data:

```bash
curl -x http://KWFFEKf:LDLFEPF@88.99.123.233:44454 -I https://www.google.com
```

### Checking a SOCKS5 proxy

```bash
curl --socks5 USERNAME:PASSWORD@PROXY_IP:PORT -I https://www.google.com
```

Example:

```bash
curl --socks5 KWFFEKf:LDLFEPF@88.99.123.233:44454 -I https://www.google.com
```

***

### How to interpret the result

{% hint style="success" %}
**The proxy works.** If the response contains `HTTP/1.1 200 OK` or `HTTP/2 200`, the connection was successful.
{% endhint %}

{% hint style="danger" %}
**The proxy does not work.** If you receive an error such as `Connection refused`, `Connection timed out`, or `Could not resolve proxy`, the connection failed.
{% endhint %}

### What to do if it does not connect

1. Recheck the username, password, IP, and port. A common mistake is mixing up **HTTP** and **SOCKS5** ports
2. Try connecting through a VPN to rule out blocking by your ISP
3. Wait 2-3 minutes after purchase: the servers need time to update
4. If nothing helped, contact [support](../../contact-us.md)
