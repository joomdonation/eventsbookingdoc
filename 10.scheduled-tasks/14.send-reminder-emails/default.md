---
title: 'Send Reminder Emails'
published: true
---

Use this task to send reminder emails to registrants a set number of days or hours before or after an event starts. It uses the reminder settings configured for each event and can also attach certificates to reminders sent after the event starts.

## Configure events to allow sending reminder emails

When you add or edit an event, configure **Send First Reminder**, **Send Second Reminder**, and **Send Third Reminder** as needed. For each reminder, enter the number of days or hours and choose whether to send it before or after the event starts. Leave the value blank or enter 0 to disable that reminder.

For example, set the first reminder to three days before the event starts and the second reminder to one day before it starts. The task checks these settings each time it runs and processes reminders that are due.

See [Setup Reminder](/basic-setup/auto-reminder) for more information about configuring event reminders. If you have enabled [support for up to six reminders](/tools#support-up-to-6-reminders), this task also processes the additional reminders.

## Create and configure the scheduled task

1. Go to **System -> Plugins** and make sure the **Task - Events Booking** plugin is enabled.
2. Go to **System -> Scheduled Tasks**, click **New** in the toolbar, and select the **Events Booking - Send Reminder Emails** task type.
3. Set the required parameters, choose how often the task should run, and save the task with its status set to **Enabled**.

If you currently use **System - Events Booking Reminder**, disable that plugin when switching to this task. The scheduled task uses its own parameters, so copy any settings you want to keep from the system plugin into the task. You can also stop any cron job that calls the system plugin's reminder URL.

## Task Basic Fields

Run this task regularly so that it has enough time to process all registrants when their reminders are due. For example, use the following values under **Basic Fields** to run it every 10 minutes.

- **Execution Rule**: Set to **Interval, Minutes**.
- **Interval in Minutes**: Set to 10.

Make sure Joomla's task scheduler is configured to execute scheduled tasks automatically.

Each run processes up to **Number of Registrants** for each enabled reminder. With the default value of 15, a run can process up to 15 first reminders, 15 second reminders, and 15 third reminders. Choose an interval that allows all reminders to be processed within the available time, taking any **Time Ranges** restriction into account.

The task keeps track of which reminders have already been processed for each registration. Later runs process the remaining registrants rather than sending the same reminder again.

## Task Parameters

- **BCC Email**: Enter an email address to receive a copy of each reminder. You can enter multiple addresses separated by commas. Leave it empty if you do not need copies.
- **Time Ranges**: Restrict sending to certain hours of the day, using the **Website Time Zone** configured under **System -> Global Configuration**. Enter each range as `from,to` using 24-hour values, and separate multiple ranges with semicolons. For example, `8,10;14,18` allows sending during the hours 8 through 10 and 14 through 18. Both endpoint hours are included, so the first range allows sending from 8:00 AM through 10:59 AM. Leave it empty to allow sending at any time. Outside these ranges, the task finishes without sending reminders.
- **Number of Registrants**: Maximum number of registrations to process for each reminder each time the task runs. The default is 15. Keep this value modest, for example 10 to 20, to avoid timeouts and stay within your hosting provider's email limits.
- **Send To Group Billing**: Set to **Yes** to send reminders to the billing person for a group registration. The default is **Yes**.
- **Send To Group Members**: Set to **Yes** to send reminders to individual group members. The default is **Yes**. Each member needs a valid email address in their registration record to receive the email.
- **Send To Unpublished Events**: Set to **Yes** to include registrants of unpublished events. For example, use this if you unpublish events when they reach capacity but still want to send reminders. The default is **No**.
- **Only Send To Paid Registrants**: Set to **Yes** to send reminders only to registrations with **Paid** status. When set to **No**, the task also includes **Pending** registrations that use an offline payment method. Pending online payments, cancelled registrations, and waiting list registrations are excluded. The default is **No**.
- **Only Send First Reminder To Checked-in Registrants**: Set to **Yes** to send the first reminder only to registrants who have checked in. This is useful for a follow-up email after the event starts. The default is **No**.
- **Only Send Second Reminder To Checked-in Registrants**: Apply the same checked-in restriction to the second reminder. The default is **No**.
- **Only Send Third Reminder To Checked-in Registrants**: Apply the same checked-in restriction to the third reminder. The default is **No**.
- **Send Certificate In First Reminder**: Set to **Yes** to attach a PDF certificate to the first reminder, subject to the conditions below. The default is **No**.
- **Send Certificate In Second Reminder**: Set to **Yes** to attach a PDF certificate to the second reminder, subject to the conditions below. The default is **No**.
- **Send Certificate In Third Reminder**: Set to **Yes** to attach a PDF certificate to the third reminder, subject to the conditions below. The default is **No**.

For a certificate to be attached, the corresponding reminder must be configured to send **after** the event starts, the registration must have **Paid** status, and the [Certificates](/advanced-features/certificates) feature must be enabled for the event. If certificate downloads are restricted to checked-in registrants, the registrant must also have checked in.

## Setup Email Subject and Email Body

Go to **Events Booking -> Emails & Messages**, find and change the following message items to customize the subject and body of each reminder.

| Reminder | Subject | Body |
| --- | --- | --- |
| First reminder | **reminder_email_subject** | **reminder_email_body** |
| Second reminder | **second_reminder_email_subject** | **second_reminder_email_body** |
| Third reminder | **third_reminder_email_subject** | **third_reminder_email_body** |

You can also customize reminder messages for an individual event or its main category. An event's message takes priority over its main category's message, which takes priority over the default message in **Emails & Messages**.

Use [Reminder Email tags](/email-tags/reminder-email), such as **[FIRST_NAME]**, **[EVENT_TITLE]**, and **[EVENT_DATE]**, to personalize the messages.
