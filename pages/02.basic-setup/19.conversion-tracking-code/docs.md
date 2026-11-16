---
title: 'Conversion Tracking Code'
published: true
---

Use **Conversion Tracking Code** to run tracking code, such as JavaScript for Google Analytics ecommerce tracking, on the registration completion page.

1. Go to Events Booking -> Configuration, in General tab, look for **Conversion Tracking Code** config option.
2. Enter the full tracking code in that setting. Events Booking inserts it into the registration complete page.

Events Booking replaces the following tags with registration and payment details when the code runs.

[ID] : The registration record ID.

[TRANSACTION_ID] : The payment transaction ID.

[TOTAL_AMOUNT] : The amount (before discount, tax)

[DISCOUNT_AMOUNT] :The discount amount

[TAX_AMOUNT] : The tax amount

[AMOUNT] : The amount due after discounts and tax.

[PAYMENT_PROCESSING_FEE] : Payment processing fee (if enabled in the payment plugin)

[ITEM_NAME] : Description of the payment

You can also use any other tags supported in email messages.