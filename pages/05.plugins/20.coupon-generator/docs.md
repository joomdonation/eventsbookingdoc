---
title: 'Coupon Generator'
media_order: coupon-generator.png
---

This plugin allows you to generate coupon code and send to registrants when they register for certain events in your site. Registrants, can then use that coupon code to get discount while registering for other events on your site.

## Enable and Configure the plugin

1. Go to **System** -> **Plugins**, find and enable the plugin **Events Booking - Auto Coupon Generation**
2. Now, when you add/edit an event, you will see a new tab **Coupons Generator** to allow you to setup the coupon code which will be sent to registrants of this event

![Coupon generator](coupon-generator.png)

* **Discount**: Enter the discount for the coupon. Discount can be set to a fixed amount (for example 10$) or by percent (for example 10% of subscription fee).
* **Event IDs**: Enter IDs of the events which the coupon can be used for - comma separated. If you leave it empty, the generated coupon can be used for any events
* **Times**: How many times this coupon code can be used. Usually, it should be 1
* **Valid From Date**: If you choose a date, the coupon code can only be used from the selected date.
* **Valid To Date**: If you chose a date, the coupon code can only be used before the selected date. After that date, the coupon code cannot be used anymore.

## How the generated coupon can be sent to registrant
With above setup, when users register and paid for the registration, the coupon code will be genreated and send to them via email:
* If you use [REGISTRATION_DETAIL] tag, the coupon code will be part of that tag
* You can also insert the tag [AUTO_COUPON_CODE] to show that coupon code in the email sent to registrant