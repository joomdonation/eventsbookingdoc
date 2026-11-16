---
title: 'Failure Payment Notification'
published: true
---

This plugin allows sending notification emails to users you want (usually administrators) when a payment for registration failure for some reasons.

## Configure The Plugin
To use this plugin, you need to go to **System -> Plugins**, find and enable **Events Booking - Failure Payment Notification** plugin. It has following parameters, you can be changed it to meet your own need:

- **Notification Emails**: Enter emails you want to receive notification, comma separated. For example email1@domain.com,email2@domain.com. If you leave it empty, the **Notification Emails**  in event or in Events Booking -> Configuration will receive notifications.
- **Subject**: Subject of the notification email.
- **Message**: Message of the notification email.

## Supported Tags
- Use [REASON] tag to show reason of payment failure (returned by payment gateway)
- You can use any tags listed here [https://docs.joomdonation.com/eventsbooking/email-tags/common-tags](/email-tags/common-tags),  for example: [FIRST_NAME], [LAST_NAME] , [ID] , [EVENT_TITLE]...

