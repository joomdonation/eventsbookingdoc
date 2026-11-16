---
title: 'Develop payment plugin'
taxonomy:
    category:
        - docs
---

Events Booking supports multiple payment gateways, each through a payment plugin. To integrate another gateway, develop a payment plugin for it.

There are two types of payment plugin.

## Redirect base payment plugin
With this type of payment plugin, registrants will be redirected to payment gateway for processing payment. If you are developing this type of payment plugin, look at https://github.com/joomdonation/os_eb_redirect for sample plugin structure and detailed instruction

## Credit card base payment plugin
With this type of payment plugin, registrants will enter credit card information directly on your site to process payment. They won't be redirected to payment gateway. If you are developing this type of payment plugin, look at https://github.com/joomdonation/os_eb_creditcard for sample plugin structure and detailed instruction