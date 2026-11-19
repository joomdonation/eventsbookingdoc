---
title: 'Offline Payment'
media_order: 'os_eb_offline1.zip,os_eb_offline2.zip,os_eb_offline3.zip,os_eb_offline4.zip,os_eb_offline5.zip,os_eb_offline6.zip'
visible: true
---

The included **Offline Payment** plugin lets registrants pay after registering, for example by bank transfer or in cash.

On the **Payment Plugins** management screen, open **os_offline** and set **Registration Status** to the status you want to assign when someone registers:

- **Pending**: The registration awaits payment and must be approved after you receive it.
- **Paid**: The registration is approved immediately, without waiting for you to confirm receipt of payment.

Configure **Icon**, **Payment Processing Fee ($)**, and **Payment Processing Fee (%)** as needed. See [Common Plugin Parameters](/basic-setup/payment-plugins#common-plugin-parameters). Publish the plugin and save your changes.

With **Registration Status** set to **Pending**, the system marks offline registrations as **Pending** and displays instructions explaining how to pay. These instructions are also sent to registrants by email.

After receiving payment, log in to your site's administrator area, open the registration record, and change its status from **Pending** to **Paid** to approve the registration.

If you use **Offline Payment**, go to **Events Booking -> Emails & Messages** and update the following messages with your payment instructions:

1. **User email body (offline payment)**
2. **Thank you message (offline payment)**

### Additional Offline Payment Plugins

Events Booking includes one offline payment plugin by default. If you need more than one offline payment method, download and install the additional plugins below as needed.

- [os_eb_offline1.zip](os_eb_offline1.zip)
- [os_eb_offline2.zip](os_eb_offline2.zip)
- [os_eb_offline3.zip](os_eb_offline3.zip)
- [os_eb_offline4.zip](os_eb_offline4.zip)
- [os_eb_offline5.zip](os_eb_offline5.zip)
- [os_eb_offline6.zip](os_eb_offline6.zip)
