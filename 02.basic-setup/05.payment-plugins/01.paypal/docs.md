---
title: PayPal
media_order: 'os-paypal.png,open_exchange_rate_app_id.png,os_eb_paypal1.zip,os_eb_paypal2.zip,os_eb_paypal3.zip,os_eb_paypal4.zip,os_eb_paypal5.zip,paypal_rest_api_parameters.png'
visible: true
---

On the **Payment Plugins** management screen, open **os_paypal** and configure the following settings:

1. **Environment**: Set to **Sandbox** for test payments or **Live** for real payments.
2. **PayPal Email**: When **Environment** is **Live**, enter the PayPal ID or email address of the account that will receive payments.
3. **Sandbox PayPal Email**: When **Environment** is **Sandbox**, enter the PayPal ID or email address of your sandbox account.
4. **Icon**: To display an icon instead of the payment method title, choose an icon from the dropdown.
5. **Locale**: Enter the PayPal locale, for example `en_US`.
6. **Payment Processing Fee ($)**: To charge registrants a fixed payment processing fee, enter the amount here.
7. **Payment Processing Fee (%)**: To charge registrants a payment processing fee calculated as a percentage, enter the percentage here.
8. **Use Custom Certs**: Leave this set to **No** unless our support team asks you to enable it.
9. **Enable Log**: Leave this set to **No** unless our support team asks you to enable logging for troubleshooting.

Only the PayPal email field for the selected **Environment** is displayed.

Publish the plugin and save your changes.

![PayPal payment plugin configuration](os-paypal.png)

## Advanced Settings

If you have a PayPal business account, follow [PayPal's instructions for getting a Client ID and Client Secret](https://developer.paypal.com/api/rest/#link-getclientidandclientsecret). Enter these credentials in the **Advanced** tab of the **os_paypal** payment plugin to allow administrators to refund registration payments from the site's administrator area.

Use the credential fields for the **Environment** selected in the **Basic** tab:

| Environment | Client ID Parameter | Client Secret Parameter |
| --- | --- | --- |
| Sandbox | **Sandbox Client ID** | **Sandbox Client Secret** |
| Live | **Client ID** | **Client Secret** |

Only the fields for the selected environment are displayed. Use credentials from the PayPal account that receives the payments, then save your changes.

![PayPal REST API parameters](paypal_rest_api_parameters.png "PayPal REST API parameters")

## Enable PayPal IPN

In some cases, IPN might be disabled in your PayPal account. If you need to enable it, for example at the request of our support team, follow the [PayPal IPN setup instructions](https://developer.paypal.com/docs/api-basics/notifications/ipn/IPNSetup/#setting-up-ipn-notifications-on-paypal). When PayPal asks for the IPN URL, enter your site's URL, for example `https://domain.com/index.php`. Replace `https://domain.com` with your site's URL.

## IPN Troubleshooting Instructions

If PayPal payments are not working on your site, our support team may ask you to collect information to help investigate the issue:

1. Log in to your site's administrator area and go to **Events Booking -> Payment Plugins**. Open **os_paypal** and set **Enable Log** to **Yes**, then save your changes.
2. Register for an event and make a payment.
3. Log in to the PayPal account that receives the payment and open the [IPN History page](https://www.paypal.com/cgi-bin/webscr?cmd=_display-ipns-history).
4. Find the IPN message for that payment, open its details, and take a screenshot.
5. Send us the screenshot in a support ticket. We will use it to guide you through the next checks.

After troubleshooting, set **Enable Log** back to **No** and save your changes.

## Requirements

- Your site must be hosted on a publicly accessible server. PayPal cannot reach a site on your local computer to notify Events Booking about payments.
- Your site must be in online mode so that PayPal can send payment notifications to Events Booking.
- Your site's frontend must be accessible without password protection, such as an `.htaccess` password. This protection is sometimes used during development, but it prevents PayPal from sending payment notifications to Events Booking.

## Use PayPal with an Unsupported Currency

PayPal supports only the currencies on its [supported currencies list](https://developer.paypal.com/docs/reports/reference/paypal-supported-currencies/). If your site uses a currency that PayPal does not support, Events Booking needs to convert the payment amount to USD before sending it to PayPal. Events Booking uses [Open Exchange Rates](https://openexchangerates.org/) for this conversion. To use the service:

1. [Register for a free Open Exchange Rates account](https://openexchangerates.org/signup/free).
2. Check your email for the APP ID, or log in and open the [App IDs page](https://openexchangerates.org/account/app-ids). Enter the APP ID in the **Open Exchange Rate APP ID** setting in Events Booking.

![Open Exchange Rates APP ID setting](open_exchange_rate_app_id.png "Open Exchange Rates APP ID setting")

## Extra PayPal Payment Plugins

You may need multiple PayPal payment plugins on your site, for example to charge a different payment processing fee for each plugin. Download and install the additional PayPal payment plugins below as needed.

If you only need to use a different PayPal account for each event, you do not need these additional PayPal payment plugins. Edit the event, open the **Advanced Settings** tab, and enter the PayPal account that should receive payments for that event.

- [os_eb_paypal1.zip](os_eb_paypal1.zip)
- [os_eb_paypal2.zip](os_eb_paypal2.zip)
- [os_eb_paypal3.zip](os_eb_paypal3.zip)
- [os_eb_paypal4.zip](os_eb_paypal4.zip)
- [os_eb_paypal5.zip](os_eb_paypal5.zip)
