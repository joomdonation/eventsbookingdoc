---
title: 'Remaining Payment Email'
visible: true
---

Events Booking emails the administrator and the registrant when the registrant pays the remaining balance on a registration they started with a deposit.

## Email sent to administrator
- Go to Events Booking -> Emails & Messages, look at **Remaining Payment Messages** tab, find and change the two items **Remaining Payment Admin Email Subject** and **Remaining Payment Admin Email Body** to suit your needs.

The following tags are supported:
- Any custom fields show on payment form can be inserted into email message using syntax [NAME_OF_FIELD_IN_UPPERCASE] . For example [FIRST_NAME], [LAST_NAME], [ORGANIZATION], [ADDRESS], [CITY], [STATE], [COUNTRY], [PHONE], [FAX]

[PAYMENT_METHOD]
[AMOUNT] : The remaining payment amount which users pay
[REGISTRANT_ID]: ID of the registration record
[TRANSACTION_ID] : Transaction ID for the payment

- Event Information Related Tags listed at:

[Event Information](/email-tags/common-tags#event-information-tags)

[Category Information](/common-tags#category-information)

[Location Information](/email-tags/common-tags#location-information)

[Event Creator Information](/email-tags/common-tags#event-creator-information)

[Event Custom Fields Information](/email-tags/common-tags#event-custom-fields-information)

[Speakers Information](/email-tags/common-tags#speakers-information)


## Email Sent To Registrant
- Go to Events Booking -> Emails & Messages, look at **Remaining Payment Messages** tab, find and change the two items **Remaining Payment User Email Subject** and **Remaining Payment User Email Body** to suit your needs.
- Supported Tags: Same with email sent to administrator listed above
