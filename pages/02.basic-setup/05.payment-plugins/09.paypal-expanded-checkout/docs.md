---
title: 'PayPal Expanded Checkout'
media_order: 'os-paypal.png,os-paypal-advanced-settings.png,open_exchange_rate_app_id.png'
visible: true
published: true
---

## Installation

When you purchase the payment plugin, you will receive a zip file called **os_eb_paypalepc.zip**. Go to **Events Booking** -> **Payment Plugins** to install it as any other payment plugin. See [**Install Payment Plugin**](/basic-setup/payment-plugins#install-new-payment-plugin) for installation instructions if needed.

## Configuration
- Follow instructions at [https://developer.paypal.com/api/rest/#link-getclientidandclientsecret](https://developer.paypal.com/api/rest/#link-getclientidandclientsecret) , get **Client ID** and **Client Secret** of your PayPal account
- Go to Events Booking -> Payment Plugins, click on os_paypalepc payment plugin to edit, enter necessary parameters there.
- If you want to change the message displayed on payment screen, please go to **Events Booking** -> **Translation**, find the language item **EB_PAYPAL_EPC_PAYMENT_INSTRUCTIONS** and change it.

## Joomla 4, Joomla 5, Joomla 6 Note

If you are using Joomla 4.0+, it has a plugin called **System - HTTP Headers** . By default, that plugin will prevent the popup window to allow users to pay using their PayPal account. To prevent that issue, you will need to edit the plugin, change the **Cross-Origin-Opener-Policy** parameter to **same-origin-allow-popups** and it will work well
