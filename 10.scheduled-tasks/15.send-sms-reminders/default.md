---
title: 'Send SMS Reminders'
published: true
---

Use this task to send SMS reminders to registrants a set number of days or hours before or after an event starts. It uses the reminder settings configured for each event and sends messages through your configured SMS gateway plugin.

The task processes the first and second SMS reminders. SMS reminders and [reminder emails](/scheduled-tasks/send-reminder-emails) use the same event timing settings, but their messages and sending status are separate.

## Configure events to allow sending SMS reminders

1. Install, configure, and enable the SMS gateway plugin you want to use. See [SMS Reminders](/basic-setup/sms-reminder#publish-and-configure-sms-plugin) for the gateway plugins and installation instructions.
2. Make sure the registration form collects the registrant's phone number in the **phone** field. Use the phone number format required by your SMS gateway. For group registrations, collect each member's phone number if you want to send reminders to individual members.
3. When you add or edit an event, set **Enable SMS** to **Yes**.
4. Configure **Send First Reminder** and **Send Second Reminder** as needed. For each reminder, enter the number of days or hours and choose whether to send it before or after the event starts. Leave the value blank or enter 0 to disable that reminder.

If **Enable SMS** is not displayed, create and enable the scheduled task described below, then reopen the event.

For example, set the first reminder to one day before the event starts and the second reminder to two hours before it starts. The task checks these settings each time it runs and processes reminders that are due.

For reminders sent after the event starts, the task only processes registrations within 60 days of the event start when using days, or within 100 hours when using hours. Choose reminder timing within these limits.

## Create and configure the scheduled task

1. Go to **System -> Plugins** and make sure the **Task - Events Booking** plugin is enabled.
2. Go to **System -> Scheduled Tasks**, click **New** in the toolbar, and select the **Events Booking - Send SMS Reminders** task type.
3. Set the required parameters, choose how often the task should run, and save the task with its status set to **Enabled**.

If you currently use **System - Events Booking SMS** only for reminders, disable that plugin when switching to this task and stop any cron job that calls its reminder URL. Keep your SMS gateway plugin enabled. The scheduled task uses its own parameters, so copy any reminder settings you want to keep from the system plugin into the task.

If you also use **System - Events Booking SMS** to notify administrators about new registrations, keep that plugin enabled. Enter a secret value in its **Trigger Reminder Code** parameter and stop any cron job that calls the system plugin's reminder URL. This prevents site visits from triggering reminders through the system plugin while allowing it to continue sending new registration notifications. The scheduled task sends the registrant reminders independently.

## Task Basic Fields

Run this task regularly so that it has enough time to process all registrants when their reminders are due. For example, use the following values under **Basic Fields** to run it every 10 minutes.

- **Execution Rule**: Set to **Interval, Minutes**.
- **Interval in Minutes**: Set to 10.

Make sure Joomla's task scheduler is configured to execute scheduled tasks automatically.

Each run processes up to **Number of Registrants** for each enabled SMS reminder. With the default value of 15, a run can process up to 15 first reminders and 15 second reminders. Choose an interval that allows all reminders to be processed within the available time, taking any **Time Ranges** restriction into account.

When the SMS gateway plugin reports that a batch has been processed, the task marks that reminder as sent for those registrations. Later runs process the remaining registrants. This sending status is separate from confirmation that a message was delivered to the recipient's phone.

## Task Parameters

- **Time Ranges**: Restrict sending to certain hours of the day, using the **Website Time Zone** configured under **System -> Global Configuration**. Enter each range as `from,to` using 24-hour values, and separate multiple ranges with semicolons. For example, `8,10;14,18` allows sending during the hours 8 through 10 and 14 through 18. Both endpoint hours are included, so the first range allows sending from 8:00 AM through 10:59 AM. Leave it empty to allow sending at any time. Outside these ranges, the task finishes without sending reminders.
- **Number of Registrants**: Maximum number of registrations to process for each SMS reminder each time the task runs. The default is 15. Keep this value modest, for example 10 to 20, to avoid timeouts and stay within your SMS gateway's sending limits.
- **Send To Group Billing**: Set to **Yes** to send reminders to the billing person for a group registration. The default is **Yes**.
- **Send To Group Members**: Set to **Yes** to send reminders to individual group members. The default is **Yes**. Each member needs a phone number in their registration record to receive the SMS.
- **Send To Unpublished Events**: Set to **Yes** to include registrants of unpublished events. For example, use this if you unpublish events when they reach capacity but still want to send reminders. The default is **No**.
- **Only Send To Paid Registrants**: Set to **Yes** to send reminders only to registrations with **Paid** status. When set to **No**, the task also includes **Pending** registrations that use an offline payment method. Pending online payments, cancelled registrations, and waiting list registrations are excluded. The default is **No**.
- **Only Send To Checked-in Registrants**: Set to **Yes** to send both SMS reminders only to registrants who have checked in. This is useful for follow-up messages after the event starts. The default is **No**.

## Setup SMS Reminder Messages

Go to **Events Booking -> Emails & Messages**, open **SMS Messages**, and customize the following message items.

| Reminder | Message item | Message key |
| --- | --- | --- |
| First reminder | **First Reminder SMS** | **first_reminder_sms** |
| Second reminder | **Second Reminder SMS** | **second_reminder_sms** |

Leave a message empty if you do not want to send that SMS reminder. The task uses these messages for all events.

Use tags such as **[FIRST_NAME]**, **[EVENT_TITLE]**, **[EVENT_DATE]**, **[LOCATION_NAME]**, and **[LOCATION_ADDRESS]** to personalize the messages. See [SMS Reminders](/basic-setup/sms-reminder#configure-sms-reminder-messages) for more supported tags.

For example:

> Hello [FIRST_NAME], this is a reminder that [EVENT_TITLE] starts on [EVENT_DATE] at [LOCATION_NAME]. We look forward to seeing you.
