# Table of contents

* [Proxyshard GitBook](README.md)
* [What is Proxyshard](about-proxyshard.md)
* [Contact us](contact-us.md)

## Our products

* [Residential proxies](our-products/residential-proxies/README.md)
  * [Standard Residential](our-products/residential-proxies/standard-residential.md)
  * [Unlimited Residential](our-products/residential-proxies/unlimited-residential-proxy.md)
  * [Premium Residential](our-products/residential-proxies/premium-residential.md)
  * [Available countries list](our-products/residential-proxies/available-countries.md)
  * [How to use Residential proxies](our-products/residential-proxies/how-to-use-residential-proxies.md)
* [Datacenter proxies](our-products/datacenter-proxies.md)
* [Mobile proxies](our-products/mobile-proxies.md)
* [ISP proxies](our-products/isp-proxies.md)
* [Network fingerprint spoofing (p0f)](our-products/p0f-spoofing.md)
* [Limitations](our-products/restrictions.md)
* [IP Checker](our-products/ip-checker.md)
* [Proxy Tester](our-products/proxy-tester.md)
* [ProxyShard Extension](our-products/proxyshard-extension.md)
* [ShardX Launcher](our-products/shardx-launcher.md)
* [About the UDP protocol](our-products/about-udp/README.md)
  * [How to install Tampermonkey and the WebRTC debug script](our-products/about-udp/tampermonkey-webrtc-debug.md)
  * [How a WebRTC leak works](our-products/about-udp/how-webrtc-leak-works.md)
  * [Where to check for WebRTC leaks](our-products/about-udp/webrtc-leak-check-tools.md)
  * [Why a TCP-only proxy is not enough!](our-products/about-udp/why-tcp-proxy-not-enough.md)
  * [Why blocking WebRTC does not protect against detection](our-products/about-udp/why-blocking-webrtc-doesnt-help.md)
  * [Results of our field tests](our-products/about-udp/field-test-results.md)
  * [Software solutions for enabling WebRTC](our-products/about-udp/webrtc-software-solutions.md)

## User API

* ```yaml
  props:
    models: true
    downloadLink: true
  type: builtin:openapi
  dependencies:
    spec:
      ref:
        kind: openapi
        spec: proxysharddoc-api
  ```

## Site navigation

* [Balance top-up](site-navigation/top-up-balance.md)
* [Purchasing and renewing proxies](site-navigation/buying-and-renewing/README.md)
  * [Datacenter proxy purchase example](site-navigation/buying-and-renewing/buying-datacenter-proxies.md)
  * [Residential proxy purchase example](site-navigation/buying-and-renewing/buying-residential-proxies.md)
  * [ISP proxy purchase example](site-navigation/buying-and-renewing/buying-isp-proxies.md)
  * [Mobile proxy purchase example](site-navigation/buying-and-renewing/buying-mobile-proxies.md)
* [Order search (Product tag)](site-navigation/order-search-product-tag.md)
* [Invoices](site-navigation/invoices.md)
* [My orders](site-navigation/my-orders.md)
* [Referral program](site-navigation/referral-program.md)

## Questions and answers

* [FAQ](faq-and-support/faq/README.md)
  * [🔥 Popular questions](faq-and-support/faq/general-questions.md)
  * [Residential proxies](faq-and-support/faq/residential-proxies.md)
    * [Why Residential proxies are not saved](faq-and-support/faq/why-residential-proxies-not-saved.md)
  * [Datacenter / ISP proxies](faq-and-support/faq/datacenter-isp-proxies.md)
  * [Mobile proxies](faq-and-support/faq/mobile-proxies.md)
  * [How to check whether a proxy works](faq-and-support/faq/how-to-check-proxy.md)
  * [Proxies are not working](faq-and-support/faq/proxy-not-working.md)
  * [The proxy location is incorrect!](faq-and-support/faq/wrong-proxy-location.md)

## Usage instructions

* [Setup instructions](setup-guides/getting-started.md)
* [ShardX Launcher](setup-guides/shardx-browser.md)
* [Windows](setup-guides/windows/README.md)
  * [Proxifier](setup-guides/windows/proxifier.md)
  * [v2rayN](setup-guides/windows/v2rayn.md)
  * [ClashX](setup-guides/windows/clashx.md)
  * [NekoRay](setup-guides/windows/nekoray.md)
  * [ProxyCap](setup-guides/windows/proxycap.md)
  * [Win2Socks](setup-guides/windows/win2socks.md)
  * [SocksCap64](setup-guides/windows/socskcap64.md)
* [macOS](setup-guides/macos/README.md)
  * [V2Box](setup-guides/macos/v2box.md)
* [Linux](setup-guides/linux/README.md)
  * [GUI apps](setup-guides/linux/gui-apps/README.md)
    * [v2rayN GUI](setup-guides/linux/gui-apps/v2rayn-gui.md)
  * [CLI apps](setup-guides/linux/cli-apps/README.md)
    * [proxychains](setup-guides/linux/cli-apps/proxychain.md)
* [iOS / Android](setup-guides/ios-android/README.md)
  * [🔥 V2Box](setup-guides/ios-android/v2box.md)
  * [Potatso](setup-guides/ios-android/potatso.md)
  * [Super Proxy](setup-guides/ios-android/super-proxy.md)
* [Antidetect browsers](setup-guides/antidetect-browsers/README.md)
  * [🔥 Vision browser](setup-guides/antidetect-browsers/vision-browser.md)
  * [AdsPower](setup-guides/antidetect-browsers/adspower.md)
* [Browsers](setup-guides/browsers/README.md)
  * [Chrome](setup-guides/browsers/chrome/README.md)
    * [🔥 ProxyShard Extension](setup-guides/browsers/chrome/proxyshard.md)
    * [ZeroOmega](setup-guides/browsers/chrome/zeroomega.md)
  * [Edge](setup-guides/browsers/edge/README.md)
    * [🔥 ProxyShard Extension](setup-guides/browsers/edge/proxyshard.md)
    * [ZeroOmega](setup-guides/browsers/edge/zeroomega.md)
  * [Opera](setup-guides/browsers/opera/README.md)
    * [🔥 ProxyShard Extension](setup-guides/browsers/opera/proxyshard.md)
    * [ZeroOmega](setup-guides/browsers/opera/zeroomega.md)
  * [Brave](setup-guides/browsers/brave/README.md)
    * [🔥 ProxyShard Extension](setup-guides/browsers/brave/proxyshard.md)
  * [Yandex Browser](setup-guides/browsers/yandex/README.md)
    * [🔥 ProxyShard Extension](setup-guides/browsers/yandex/proxyshard.md)
  * [Vivaldi](setup-guides/browsers/vivaldi/README.md)
    * [🔥 ProxyShard Extension](setup-guides/browsers/vivaldi/proxyshard.md)
  * [Safari](setup-guides/browsers/safari.md)
  * [Mozilla Firefox](setup-guides/browsers/mozilla-firefox/README.md)
    * [FoxyProxy](setup-guides/browsers/mozilla-firefox/foxyproxy.md)
* [Telegram](setup-guides/telegram.md)
* [MikroTik proxy](setup-guides/mikrotik-proxy.md)
* [OpenWrt proxy](setup-guides/openwrt-proxy.md)
* [Checker proxy](setup-guides/checker-proxy.md)
* [Template](setup-guides/template.md)

## shardx-launcher-api

* ```yaml
  type: builtin:openapi
  props:
    models: true
    downloadLink: true
  dependencies:
    spec:
      ref:
        kind: openapi
        spec: shardbrowser-api
  ```
