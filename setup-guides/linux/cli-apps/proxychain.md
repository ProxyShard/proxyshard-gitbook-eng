# proxychains

## Proxychains4 setup

Install the proxychains4 package from the repository

```bash
apt install proxychains4
```

## **Configuration setup**

Open the configuration at <mark style="color:$info;">**/etc/proxychains4.conf**</mark> and specify the protocol and proxy connection details in it.

<figure><img src="../../../.gitbook/assets/image (247).png" alt=""><figcaption></figcaption></figure>

{% hint style="info" %}
**You can find a proxy setup example in the [Setup guide](../../getting-started.md) section**
{% endhint %}

## **Checking operation**

After specifying the connection settings, you can check functionality by sending a request to ifconfig.me.

```
proxychains curl ifconfig.me
```

**If the check confirms that your IP address has changed, you can now start using your proxies!**
