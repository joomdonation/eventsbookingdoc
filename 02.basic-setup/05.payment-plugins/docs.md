---
title: 'Payment Plugins'
media_order: 'payment-plugins.png,install-payment-plugin.png'
taxonomy:
    category:
        - docs
---

For a paid event (price > 0), registrants need to pay to complete their registration.

Choose which payment methods registrants can use to pay online. **Events Booking** comes with five payment plugins: **Paypal** (PayPal Payments Standard), **Authorize.net** (AIM), **Eway**, **Worldpay**, and **Offline Payment**. Additional plugins are sold separately for $24.99 each. See [Events Booking Payment Plugins](https://joomdonation.com/payment-plugins/events-booking-payment-plugins.html) for the available plugins.

Open Payment Plugins in any of these three ways.
1. Go to **Components -> Events Booking -> Payment Plugins**
2. Open Events Booking **Dashboard**, then click the **Payment Plugins** icon.
3. From any **Events Booking** page, go to **Setup -> Payment Plugins**.

![Payment Plugins Mamangement](payment-plugins.png)


## Common Tasks

### Uninstall un-used payment plugins
Unpublish any payment plugins you do not want to offer. You can do this in either of two ways.
1. Click on the **green (published) icon** in the **Published** column.
2. Select the checkbox next to the payment plugin, then click **Unpublish** in the toolbar.

### Change title of payment plugin

Use a title that helps registrants recognize the payment method. For example, you can change **Authorize.net** to **Credit Card**.

Open the payment plugin, change its title, and click Save in the toolbar.

### Translate Payment Plugin Title
To show the plugin title in the language the registrant uses, follow these steps.
1. Use a language item for title of the payment plugin. For example, change the title to OS_PAYPAL instead of PayPal
2. Go to **Events Booking -> Translation**, click **New Item** in the toolbar. Then enter a new language item for the payment method title. Save your changes.
3. Translate the new language item which you just created.

### Using icons for payment methods
Events Booking displays payment method titles on the registration form by default. Since version 2.12.0, you can choose to display icons instead.

Open the payment plugin and choose an icon in Icon. If the icon you want is unavailable, upload it to **media/com_eventbooking/assets/images/paymentmethods**. Then select it from the list.

### Make a payment plugin selected by default

Events Booking selects the first payment plugin on the registration form by default. To select a different one, move it to the top of the list.

## Install New Payment Plugin

If you need a payment plugin that **Events Booking** does not include, check whether it is available at [Events Booking Payment Plugin](http://joomdonation.com/payment-plugins/events-booking-payment-plugins.html). You can also develop a plugin yourself or hire someone to develop it. Once you have the plugin, install it as follows.
1.  Go to **Events Booking -> Payment Plugins**
2.  Scroll to the bottom of the page.
3.  Click **Choose File** to select the payment plugin.
4.  Click **Install** to process the installation.

![Install Payment Plugin](install-payment-plugin.png)

Follow the guide for your payment method to install or configure its plugin.

- [PayPal](/basic-setup/payment-plugins/paypal)
- [Authorize.Net](/basic-setup/payment-plugins/authorize-net)
- [Offline Payment](/basic-setup/payment-plugins/offline-payment)
- [Eway](/basic-setup/payment-plugins/eway)
- [Worldpay](/basic-setup/payment-plugins/worldpay)
- [PayPal Pro](/basic-setup/payment-plugins/paypal-pro)
- [Stripe](/basic-setup/payment-plugins/stripe)
- [Stripe Checkout](/basic-setup/payment-plugins/stripe-checkout)
- [PayPal Expanded Checkout](/basic-setup/payment-plugins/paypal-expanded-checkout)
- [Payrexx](/basic-setup/payment-plugins/payrexx)
- [Square Hosted Checkout](/basic-setup/payment-plugins/square-hosted-checkout)
- [Authorize.net Accept Hosted](/basic-setup/payment-plugins/authorize-net-accept-hosted)
- [Rapyd Hosted Checkout](/basic-setup/payment-plugins/rapyd-hosted-checkout)
- [Mollie](/basic-setup/payment-plugins/mollie)
- [Redsys](/basic-setup/payment-plugins/redsys)
