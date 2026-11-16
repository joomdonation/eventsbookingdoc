---
title: 'Common Tags'
published: true
---

The list of tags below could be used on all kind of emails

## Event Information Tags
- [EVENT_ID]
- [EVENT_TITLE]
- [ALIAS]
- [PRICE_TEXT]
- [EVENT_DATE]
- [EVENT_END_DATE]
- [EVENT_DATE_DATE]
- [EVENT_DATE_TIME]
- [EVENT_END_DATE_DATE]
- [EVENT_END_DATE_TIME]
- [CANCEL_BEFORE_DATE]
- [SHORT_DESCRIPTION]
- [DESCRIPTION]
- [EVENT_CAPACITY]
- [INDIVIDUAL_PRICE]
- [EVENT_LINK]

## Category Information
- [MAIN_CATEGORY_NAME] : Name of main category of event
- [CATEGORY_NAME]: Contain name of all categories of the event. In case there are multiple categories, it is comma separated
- [CATEGORY_LINK] : Link to the category from frontend of website.

## Location Information
- [LOCATION_NAME]
- [LOCATION_ADDRESS]
- [LOCATION_DESCRIPTION]
- [LOCATION]: Name of location and it is linked to the map of location 
- [LOCATION_NAME_ADDRESS] : Contains both name and address of location

## Event Creator Information:
- [EVENT_CREATOR_NAME]
- [EVENT_CREATOR_USERNAME]
- [EVENT_CREATOR_EMAIL]
- [EVENT_CREATOR_ID]

## Event Custom Fields Information
If you use event custom fields to add more information about the event, you can include value of these custom fields in emails & messages using the syntax [NAME_OF_FIELD_IN_UPPERCASE]

For example, if we have a field with name **field_speaker**, you can include value of that field using tag **[FIELD_SPEAKER]**

If you have a field with name **field_hours**, you can include value of that field using **[FIELD_HOURS]** tag.

## Speakers Information
[SPEAKERS] : Contain name of all speakers for the event. (Name of speakers are comma separated)

## Registration Information
- [REGISTRATION_DETAIL]: Contains full information of registration
- [COUPON_CODE]
- [USER_ID]
- [USERNAME]
- [NAME] : First Name + Last Name
- [GROUP_MEMBERS_NAMES] : Name of all group members in a group registration, comma separated
- [GROUP_MEMBERS]: List all group members in a group registration.
- [NUMBER_REGISTRANTS]
- [INVOICE_NUMBER]
- [TRANSACTION_ID]
- [REGISTRANT_ID]: ID of registration record
- [ID] : ID of registration record
- [DATE] : Current Date
- [PAYMENT_DATE]
- [REGISTER_DATE] : Date of the registration
- [REGISTER_DATE_TIME]: Date of the registration including time
- [PAYMENT_METHOD] : Title of payment method
- [PAYMENT_METHOD_NAME] : Name of payment method such as os_paypal, os_offline
- [REGISTRATION_STATUS]: Pending, Paid, Cancelled, Waiting List, Waiting List Cancelled.
- [PAYMENT_STATUS]: For registration which uses deposit payment only. Possible values: Partial Payment, Deposit Paid, Full Payment
- [PUBLISHED]: 0: Pending, 1: Paid, 2: Cancelled
- [SUBSCRIBE_NEWSLETTER]: Show if registrant check on checkbox to join newsletter or not

## Custom Fields Data
For any custom fields which is displayed on event registration form, it can be included in the email using syntax [NAME_OF_FIELD_IN_UPPERCASE] . For example [FIRST_NAME] ,[LAST_NAME], [ADDRESS]....


## Payment Amount Data
- [REGISTRATION_RATE]
- [TAX_RATE]: Tax rate of the registration
- [TOTAL_AMOUNT]: The payment amount before discount, tax applied. 
- [TOTAL_AMOUNT_MINUS_DISCOUNT]: [TOTAL_AMOUNT] - [DISCOUNT_AMOUNT]
- [DISCOUNT_AMOUNT]: Discount amount for the registration
- [LATE_FEE]: Late fee (if available) applied for registration
- [PAYMENT_PROCESSING_FEE]
- [AMOUNT]: The final amount which registrants have to pay for the registration. 
- [DEPOSIT_AMOUNT]: The deposit amount which user pay for registration. It will be zero if users choose Full Payment for registration
- [DUE_AMOUNT]: The remaining amount which users have to pay, [AMOUNT]  - [DEPOSIT_AMOUNT]. In case users choose Full Payment, it is 0.

## Links
- [CANCEL_REGISTRATION_LINK] : Link to cancel registration if registration is enabled
- [DEPOSIT_PAYMENT_LINK] : Link to complete remaining payment for a registration which uses deposit payment
- [PAYMENT_LINK]: Link to complete payment for registration (in case users did not pay or they are on waiting list and you want to send link to ask them to make payment to become registrant)
- [DOWNLOAD_CERTIFICATE_LINK]
- [DOWNLOAD_TICKET_LINK]

## Ticket Types Data
In case you are using ticket types, for your event, the following tags are available:
- [TICKET_TYPES]: Contains all ticket types and it's quantity which registrant choose for the registration
- [TICKET_TYPES_TABLE]: Contains all ticket types of the registration displayed in a table.
