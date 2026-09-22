---
icon: server
---

# Purchasing ISP proxies

{% hint style="info" %}
You need sufficient [funds](../top-up-balance.md) on your balance to pay for an order.
{% endhint %}

## Purchasing proxies

To purchase [ISP proxies](https://dashboard.proxyshard.com/isp-proxy):

1. Open `ISP Proxy`.
2. Select the proxy country in `Proxy region`.
3. Select a payment period in `Billing cycle`.
4. Enter the number of proxies in `Number of proxies`.
5. Enable `Auto renew` if you want the order to renew automatically.
6. If needed, enable `Enable p0f settings` and enter the number of slots in `Total slots`.
7. If you have a promo code, enter it in `Promocode` and click `Apply`.
8. Review the order total and click `Buy now`.

<figure>
  <picture>
    <source srcset="../../.gitbook/assets/isp-purchase-form_black.png" media="(prefers-color-scheme: dark)">
    <img src="../../.gitbook/assets/isp-purchase-form_white.png" alt="ISP proxy purchase form">
  </picture>
</figure>

## Payment and activation

After you click `Buy now`, an invoice with the `Unpaid` status opens. Check the `Total amount`, then click `Pay with Wallet`. The payment flow is the same as in the [Datacenter proxy guide](buying-datacenter-proxies.md#paying-for-the-order).

After payment, the order appears under `Active products` and in [`My orders`](https://dashboard.proxyshard.com/products).

{% hint style="warning" %}
The proxies become available within 1-2 minutes while the order is being synchronized.
{% endhint %}

## Managing and renewing an order

<figure>
  <picture>
    <source srcset="../../.gitbook/assets/isp-order-details_black.png" media="(prefers-color-scheme: dark)">
    <img src="../../.gitbook/assets/isp-order-details_white.png" alt="Managing an ISP proxy order">
  </picture>
</figure>

When `Auto renew` is enabled, the system attempts to renew the order 1-2 hours before the current billing period ends. If the balance is sufficient, the payment is charged automatically.

If automatic renewal is disabled or the balance is insufficient, the order moves to the `On-hold` status. To renew it manually, open the order, click `Renew`, and pay the invoice.

See [Order fields](../../our-products/isp-proxies.md#order-fields) for details about `Status`, `Product tag`, access credentials, p0f settings, and the other fields.

{% hint style="danger" %}
An order with the `Canceled` status cannot be renewed. An unpaid order moves to this status after three days.
{% endhint %}
