---
title: 'Registration status is Pending after making payment'
visible: true
---

If a test registration stays Pending after payment through PayPal instead of changing to Active, check the settings below.

1. First, please make sure your site is public accessible, so:

- If your site runs on localhost, move it to a live server that is accessible over the internet.
- In System - Global Configuration, set Offline to No so PayPal can reach your site.
- If the frontend is password-protected, for example through .htaccess or your server settings, turn off that protection so PayPal can reach the site.

2. Make sure PayPal IPN is enabled in your PayPal account (the one which receives payment)

By default, PayPal IPN is turned on in your PayPal account. Each time a payment processed, PayPal will send an IPN message to Events Booking to notify this payment. If for some reason, PayPal IPN is turned off on your PayPal account, Membership Pro won't work and you will need to turn it on.

- Follow the instructions at [https://www.jotform.com/help/276-How-to-Enable-IPN-for-Paypal](https://www.jotform.com/help/276-How-to-Enable-IPN-for-Paypal) to enable PayPal IPN in the PayPal account which receive payment on your site. PayPal will ask for IPN URL, simply enter URL of your site into that parameter
- Go to Events Booking -> Payment Plugins, click on os_paypal payment plugin to edit, set Log IPN Messages parameter to Yes. 

After that, try to register again, make payment. If it still doesn't work, submit a support ticket sending us super admin account of your site so that we can check and correct it for you