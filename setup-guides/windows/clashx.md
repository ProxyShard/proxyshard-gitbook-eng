# ClashX

{% hint style="success" %}
This solution supports UDP tunneling!
{% endhint %}

## **ClashX** setup

Go to the official GitHub page of the ClashX project and download the required archive version for your OS. The example shows setup on Windows OS ([Clash.for.Windows-0.20.39-win.7z](https://github.com/lantongxue/clash_for_windows_pkg/releases/download/0.20.39/Clash.for.Windows-0.20.39-win.7z)).

{% embed url="https://github.com/lantongxue/clash_for_windows_pkg/releases" %}

<figure><img src="../../.gitbook/assets/image (170).png" alt=""><figcaption></figcaption></figure>

## **Starting ClashX**

Then unpack the archive and run "Clash for Windows.exe" as _<mark style="color:red;">**administrator**</mark>_, as shown in the example below:

<figure><img src="../../.gitbook/assets/image (172).png" alt="" width="563"><figcaption><p>Unpacking the archive to the desktop</p></figcaption></figure>

<figure><img src="../../.gitbook/assets/image (162).png" alt="" width="375"><figcaption><p>Run as administrator</p></figcaption></figure>

## **Program setup**

After starting the program, go to "<mark style="color:purple;">Profiles</mark>" and open the <mark style="color:purple;">config.yaml</mark> file editor.

<figure><img src="../../.gitbook/assets/image (159).png" alt="" width="375"><figcaption></figcaption></figure>

## **Configuration file setup**

Set the file configuration as in the example below, specifying your proxies from the order:

```yaml
proxies:
  - name: "ProxyShard-Germany-testname"
    type: socks5
    server: 123.123.123.123
    port: 1234
    username: proxy_login
    password: password_login
    udp: true

proxy-groups:
  - name: "Auto"
    type: select
    proxies:
      - ProxyShard-Germany-testname

rules:
  - PROCESS-NAME,chrome.exe,Auto
  - MATCH,DIRECT
```

In the end, it should look approximately like this:

<figure><img src="../../.gitbook/assets/image (158).png" alt="" width="563"><figcaption><p>Configuration example</p></figcaption></figure>

{% hint style="info" %}
**You can find a proxy setup example in the [Setup guide](../getting-started.md) section**
{% endhint %}

<pre><code>proxies:
  - name: "ProxyShard-Germany-testname"       | Here you set the proxy name
    type: socks5                              | Protocol type 
    server: 123.123.123.123                   | Proxy address or domain 
    port: 1234                                | Proxy port
    username: proxy_login                     | Proxy login                    
    password: password_login                  | Proxy password 
    udp: true                                  
proxy-groups:
  - name: "Auto"
    type: select
    proxies:
      - ProxyShard-Germany-testname              

rules:
  - PROCESS-NAME,<a data-footnote-ref href="#user-content-fn-1">chrome.exe</a>,Auto   | Select a specific application for proxying
  - MATCH,DIRECT      | In our example, the Chrome browser is used,
                      | but it can be any application, for example discord.exe  
                      | - MATCH,DIRECT : Indicates that all traffic that is not Chrome
                      | will be routed not to the proxy, but to your main interface               
</code></pre>

## **Checking the configuration**

After configuring it, open "Proxies", select the "Global" option, and check the config you set up in step 4.

<figure><img src="../../.gitbook/assets/image (160).png" alt="" width="563"><figcaption></figcaption></figure>

If the check fails and you get "Failed", compare the configuration file and make sure all proxy data was entered correctly. If the settings are correct, you will get a successful check result as shown in the screenshot below.

<figure><img src="../../.gitbook/assets/image (161).png" alt=""><figcaption></figcaption></figure>

## **Installing and enabling the TAP interface**

Next, go to "General" and install the TAP interface on your computer. It will create a new interface to which the proxy will be bound.

After installing the TUN interface, enable TUN Mode, as shown in the 4th frame of the screenshot.

<figure><img src="../../.gitbook/assets/image (163).png" alt="" width="563"><figcaption></figcaption></figure>

## **Checking functionality**

If everything starts successfully, open the application for which you configured the config (step 4) and enjoy your programs working with UDP traffic proxying!<br>

In our example, Chrome was proxied, and we can check it with [checkers](../../our-products/about-udp/webrtc-leak-check-tools.md).

<figure><img src="../../.gitbook/assets/image (164).png" alt="" width="563"><figcaption></figcaption></figure>

<figure><img src="../../.gitbook/assets/image (165).png" alt="" width="563"><figcaption></figcaption></figure>

If the check or proxying [does not work](../../faq-and-support/faq/proxy-not-working.md), make sure you definitely started ClashX as administrator and completed steps 4 through 6 correctly.

## **Additional. Adding multiple proxies and switching between them**

To quickly switch between proxies, add new proxies to the configuration from step 4. Names like "ProxyShard-DE-testname1" are arbitrary and can be set as you prefer.

The key point after adding them is to also specify the proxy in "proxy-group", as shown below:

```yaml
proxies:
  - name: "ProxyShard-DE-testname1"
    type: socks5
    server: 123.123.123.123
    port: 42651
    username: LOgin
    password: pasSSWORD
    udp: true
    
  - name: "ProxyShard-NL-testname2"
    type: socks5
    server: 123.123.123.123
    port: 42651
    username: LOgin
    password: pasSSWORD
    udp: true

  - name: "ProxyShard-RO-testname3"
    type: socks5
    server: 123.123.123.123
    port: 42651
    username: LOgin
    password: pasSSWORD
    udp: true

proxy-groups:
  - name: "Auto"
    type: select
    proxies:
      - ProxyShard-DE-testname1
      - ProxyShard-NL-testname2
      - ProxyShard-RO-testname3

rules:
  - PROCESS-NAME,chrome.exe,Auto
  - MATCH,DIRECT
```

If you specified everything correctly, additional connection points will appear in "Proxies". The connection will be made depending on the selected settings profile (just click any of them).

<figure><img src="../../.gitbook/assets/image (166).png" alt=""><figcaption></figcaption></figure>

[^1]: application to proxy
