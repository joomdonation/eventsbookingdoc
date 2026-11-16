---
title: 'Failure Payment Notification'
published: true
---

Notify selected recipients, typically administrators, when a registration payment fails.

## Configure The Plugin
Go to **System -> Plugins** and enable **Events Booking - Failure Payment Notification**. Adjust the following settings as needed.

- **Notification Emails**: Enter emails you want to receive a notification, comma separated. For example email1@domain.com,email2@domain.com. If you leave it empty, the **Notification Emails**  in event or in Events Booking -> Configuration will receive notifications.
- **Subject**: Subject of the notification email.
- **Message**: Message of the notification email.

## Supported Tags
- Use [REASON] tag to show reason of payment failure (returned by payment gateway)
- You can use any tags listed here [https://docs.joomdonation.com/eventsbooking/email-tags/common-tags](/email-tags/common-tags),  for example: [FIRST_NAME], [LAST_NAME] , [ID] , [EVENT_TITLE]...

