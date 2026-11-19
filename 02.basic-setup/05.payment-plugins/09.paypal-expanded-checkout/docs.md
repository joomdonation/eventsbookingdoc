---
title: 'PayPal Expanded Checkout'
media_order: 'os-paypal.png,os-paypal-advanced-settings.png,open_exchange_rate_app_id.png'
visible: true
published: true
---

## Installation

After purchasing the plugin, go to **Events Booking** -> **Payment Plugins** and install **os_eb_paypalepc.zip**. See [**Install Payment Plugin**](/basic-setup/payment-plugins#install-new-payment-plugin) for the steps.

## Configuration

1. Follow [PayPal's instructions for getting a Client ID and Client Secret](https://developer.paypal.com/api/rest/#link-getclientidandclientsecret) to get the credentials for your PayPal account.
2. Go to **Events Booking -> Payment Plugins**, open **os_paypalepc**, and enter the required parameters. Save your changes.
3. To change the message displayed on the payment screen, go to **Events Booking -> Translation**, find the language item **EB_PAYPAL_EPC_PAYMENT_INSTRUCTIONS**, and update its text.

## Joomla 4, Joomla 5, Joomla 6 Note

Joomla 4.0 and later include the **System - HTTP Headers** plugin. Its default settings prevent the popup window used to pay with a PayPal account from working. To resolve this, edit the plugin, set **Cross-Origin-Opener-Policy** to **same-origin-allow-popups**, and save your changes.
