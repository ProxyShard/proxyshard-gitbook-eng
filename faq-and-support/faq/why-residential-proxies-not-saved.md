---
icon: arrows-rotate
---

# Why Residential proxies are not saved

{% hint style="info" %}
This is normal behavior. Residential proxies are dynamic, and storing generated sessions in Proxy List simply makes no sense.
{% endhint %}

## Why it works this way

Residential proxies differ from [Datacenter](../../our-products/datacenter-proxies.md) and [ISP](../../our-products/isp-proxies.md) proxies because proxy IP addresses are hosted on real residential devices.

Each generation creates a new session with a unique identifier, to which an IP is temporarily bound. That is why the list is not saved: it becomes outdated immediately after rotation.

## Old sessions do not disappear

{% hint style="success" %}
When you generate new proxies with different settings, **the old ones continue to work** and do not change their parameters. Each session exists separately from the others.
{% endhint %}

### Example

Suppose you generated German proxies:

```
relay-eu.proxyshard.com:8080:plan-limited-country-de-sid-aaaaaaaaa:xxxxxxxxx
```

Let's break down the connection string:

| Part                      | Value                                                                              |
| ------------------------- | ---------------------------------------------------------------------------------- |
| `relay-eu.proxyshard.com` | Load balancing server (relay)                                                      |
| `8080`                    | Server port                                                                        |
| `plan-limited`            | Proxy tariff (`limited` - regular, `unlimited` - unlimited, `premium` - premium)   |
| `country-de`              | Connection country: Germany (`de`)                                                 |
| `sid-aaaaaaaaa`           | Unique session ID to which the IP address is bound                                 |
| `xxxxxxxxx`               | Connection password                                                                |

If after that you generate, for example, US proxies, a new string with `country-us` and another `sid` will appear. But the German session `sid-aaaaaaaaa` **will not go anywhere** and will continue working with the same IP until the session expires.

{% hint style="warning" %}
If you need a permanent IP, use [Datacenter](../../our-products/datacenter-proxies.md) or [ISP proxies](../../our-products/isp-proxies.md)\
Proxies from these sections have a static IP and are issued only to one user
{% endhint %}
