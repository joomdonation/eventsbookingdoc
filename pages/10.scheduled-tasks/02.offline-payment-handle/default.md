---
title: 'Offline Payment Handle'
media_order: task-eventsbooking-offline-payment-handle.png
published: true
---

Use this task if you enable the [**Offline Payment**](/basic-setup/payment-plugins/offline-payment) plugin. It can remind registrants to pay if you have not received payment after a set number of days. It can also cancel registrations that remain unpaid after the interval you configure.

1. Go to **System -> Plugins** and make sure the **Task - Events Booking** plugin is enabled.
2. Go to **System -> Scheduled Tasks**, click **New** in the toolbar to create a new scheduled task for **Events Booking - Offline Payment Handle** task type.
3. Set the required parameters and save the task.


## Task Basic Fields
Run this task several times a day. Each run processes 10 to 15 registrants. Use the following values under **Basic Fields**.

- **Execution Rule**: Set to **Interval, Hours**
- **Interval in Hours**: Set to the number you want, for example, if you set it to 1, the task will be run every 1 hour.

## Task Parameters
- **Number Days To Send Reminder**: Enter number of days into this parameter (for example, 7 days). Then if users choose to use offline payment and did not send payment to you within 7 days (after registration/before event date), the system will send reminder email to them.
- **Number Days To Cancel Registration**: It is 0 by default, mean the system won't cancel registration, even if no payment received. If you want the system to cancel registration automatically if payment is not received within certain number of days (after registration/before event date), enter the number here (for example, set it to 10 days after registration or 3 days before event date).
- **Number Registrants**: Number of registrants the system will process each time the task is executed. You should not set it to a high number to avoid timeout, set it to 10 to 20 should be enough.
- **Events**: If you only want to handle this process for certain events only, choose these events here. Otherwise, registrants from all events will be processed.
- **Send Reminder and Cancel Registration Base On**:  Choose how the system will get list of registrants to process base on **Registration Date** or **Event Date**

## Setup Email Subject and Email Body

Go to **Events Booking -> Emails & Messages**, find and change the following message items to customize the subject and body of the email if needed:

- **offline_payment_reminder_email_subject**
- **offline_payment_reminder_email_body**