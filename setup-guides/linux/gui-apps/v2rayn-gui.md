# v2rayN GUI

{% hint style="success" %}
This solution supports UDP tunneling!
{% endhint %}

## v2rayN setup.

Follow the [link](https://github.com/2dust/v2rayN/releases) to download V2rayN.

{% embed url="https://github.com/2dust/v2rayN/releases" %}

<figure><img src="../../../.gitbook/assets/image (244).png" alt=""><figcaption></figcaption></figure>

Or download the package through the console.

```bash
wget https://github.com/2dust/v2rayN/releases/download/7.14.12/v2rayN-linux-64.deb
```



## **Installation and launch**

Install the downloaded package through "<mark style="color:purple;">Discover</mark>" or install it through the command line.

<figure><img src="../../../.gitbook/assets/Image00001 (11).PNG" alt=""><figcaption></figcaption></figure>

```bash
apt install ./v2rayN-linux-64.deb
```

Then start the application through "<mark style="color:purple;">Start</mark>" or the command line.

<figure><img src="../../../.gitbook/assets/Image00002 (12).PNG" alt=""><figcaption></figcaption></figure>

{% code fullWidth="false" %}
```
v2ray
```
{% endcode %}

## **Profile setup**&#x20;

Create a new configuration and specify SOCKS / HTTP as the connection protocol.

<figure><img src="../../../.gitbook/assets/image (246).png" alt=""><figcaption></figcaption></figure>

{% hint style="info" %}
**You can find a proxy setup example in the [Setup guide](../../getting-started.md) section**
{% endhint %}

## **Connection profile setup**

Paste the proxies copied from the order into the corresponding fields, make sure to specify the configuration core (<mark style="color:purple;">Xray</mark> or <mark style="color:purple;">SingBox</mark>), and save the settings.

<figure><img src="../../../.gitbook/assets/Image00003 (6).PNG" alt=""><figcaption></figcaption></figure>

## Starting the client

Start the client by enabling <mark style="color:purple;">Tun</mark> mode.

<figure><img src="../../../.gitbook/assets/image (245).png" alt=""><figcaption></figcaption></figure>

**Done! You can now fully use the proxy by tunneling all traffic through it.**
