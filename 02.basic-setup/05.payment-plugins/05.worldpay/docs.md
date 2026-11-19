---
title: Worldpay
visible: true
---

## Plugin Configuration

On the **Payment Plugins** management screen, open **os_worldpay** and configure the following settings:

1. **Environment**: Set to **Sandbox** for test payments or **Live** for real payments.
2. **Worldpay Installation ID**: Enter the installation ID from your Worldpay account.
3. **Callback Password**: Enter the callback password configured for that Worldpay installation.
4. Configure **Icon**, **Payment Processing Fee ($)**, and **Payment Processing Fee (%)** as needed. See [Common Plugin Parameters](/basic-setup/payment-plugins#common-plugin-parameters).
5. Publish the plugin and save your changes.

## Worldpay Account Configuration

Configure your Worldpay account as follows:

1. Log in to your Worldpay merchant account and edit the installation. In **Payment Response URL**, enter:

    ```text
    https://domain.com/index.php?option=com_eventbooking&task=payment_confirm&payment_method=os_worldpay&notify=1
    ```

    Replace `https://domain.com` with your site's URL.

2. Select the **Payment Response enabled** checkbox.
