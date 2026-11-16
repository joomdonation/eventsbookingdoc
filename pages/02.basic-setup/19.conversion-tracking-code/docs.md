---
title: 'Conversion Tracking Code'
published: true
---

You might want to execute some tracking code (usually javascript code like Google Analytics Ecommerce tracking) on registration complete page. For that, you can use **Conversion Tracking Code** option in Events Booking

1. Go to Events Booking -> Configuration, in General tab, look for **Conversion Tracking Code** config option.
2. Enter the full code which you want to be executed on that config option. That code will be inserted into registration complete page.

You can use the following tags and it will be replaced with the related information when the code is executed

[ID] : Will be replaced with ID of the registration record

[TRANSACTION_ID] : Will be replaced with Transaction ID of the payment

[TOTAL_AMOUNT] : The amount (before discount, tax)

[DISCOUNT_AMOUNT] :The discount amount

[TAX_AMOUNT] : The tax amount

[AMOUNT] : The actual payment amount which users have to pay (after discount, tax applied)

[PAYMENT_PROCESSING_FEE] : Payment processing fee (if enabled in the payment plugin)

[ITEM_NAME] : Description of the payment

You can use any other tags, same as the tags which you can use in email messages.