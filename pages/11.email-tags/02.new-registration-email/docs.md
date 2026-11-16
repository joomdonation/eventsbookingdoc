---
title: 'New Registration Email'
---

Events Booking emails the administrator and the registrant when someone registers for an event.

## Registration Email
- For the email send to the person who makes the registration and administrator, You can use all tags as described in [Common Tags](/email-tags/common-tags)
- For admin, the subject and email can be configured in **Admin Email Subject** and **Admin Email Body** message items (in **Registration Email Messages** tab). 
- For registrant, the email subject and email body is also configured in **Registration Email Messages** tab and it depends on the payment method which registrant uses for the registration:

+ If it is paid event and registrant uses offline payment method, the subject and email is configured in **User Email Subject** and **User Email Body (Offline Payment)**
+ If registrant uses an online payment method such as PayPal or the event they registered for is free, the subject and email is configured in **User Email Subject** and **User Email Body**.

Please note that if needed, you can define these messages for each event on add/edit event page in Messages tab. If you enter messages inside the event, it will override the messages defined in Events Booking -> Emails & Messages.

## Email send to group members
Events Booking emails the administrator and the registrant when someone registers for an event.

- [REGITRATION_DETAILS]: Contains all information of the registration
- [PAYMENT_METHOD]
- [PAYMENT_METHOD_NAME]
- [GROUP_BILLING_FIRST_NAME]
- [GROUP_BILLING_LAST_NAME]
- [GROUP_BILLING_EMAIL]
- [EVENT_TITLE]
- [EVENT_DATE]
- [EVENT_END_DATE]
- [TRANSACTION_ID]
- [DATE]
- [SHORT_DESCRIPTION]
- [DESCRIPTION]
- [LOCATION]
- [EVENT_LINK]
- [DOWNLOAD_CERTIFICATE_LINK]
- [ID]
- [MEMBER_DETAIL]
- For any custom fields which are collected for group members, you can use the syntax [NAME_OF_FIELD_IN_UPPERCASE] to include value of that custom field into the email message. For example [FIRST_NAME], [LAST_NAME], [EMAIL], [ADDRESS]....
