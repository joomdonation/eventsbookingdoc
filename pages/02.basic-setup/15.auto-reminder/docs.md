---
title: 'Setup Reminder'
media_order: 'reminder_plugin_settings.png,curl.png,event-reminder-settings.png,system-eb-reminders-plugin.png'
---

**Events Booking** alllows you setup the system to send reminder emails to registrants X-days before event start date to remind them about the event so that they won't forgot about it. If you want to use this feature:

## Configure events to allow sending reminder emails
Events Booking allows you to send up to 3 reminder emails to registrants of your events before or after your event started. When you add/edit an event, you will see three settings:

**Send First Reminder**
**Send Second Reminder**
**Send Third Reminder**

Enter the number you want for each setting (leave it empty or 0 to disable sending reminder email), choose to send before/ after event started, depends on your need.

![event-reminder-settings](event-reminder-settings.png "event-reminder-settings")

## Configure reminder email messages
Events Booking generate default reminder email messages when you first install the extension. However, it is good to review and change these default messages to meet your own need if needed. To do that, go to **Events Booking** -> **Emails & Messages**, change the following email subject & messages if you want:

*  **First Reminder Email Subject**
*  **First Reminder Email Body**
*  **Second Reminder Email Subject**
*  **Second Reminder Email Body**
*  **Third Reminder Email Subject**
*  **Third Reminder Email Body**

You can use the following tags in the email messages:
- [EVENT_DATE]
- [EVENT_TITLE]
- [FIRST_NAME]
- [LAST_NAME]
- [TRANSACTION_ID]
- [LOCATION_NAME]
- [LOCATION] (display name, address of location and allow clicking on to view that location on google map)
- [DOWNLOAD_CERTIFICATE_LINK] (if you are using certificate feature)
- [DOWNLOAD_TICKET_LINK] (if you are using ticket pdf feature)
- [REGISTRATION_DETAIL]


## Publish and configure Events Booking - Reminder plugin

To have system send reminder email to registrants, you need to go to Extensions -> Plugins, find and publish **System - Events Booking Reminder** plugin. The plugin will be run every 20 minutes to check and send reminder emails to registrants. It has following parameters, you can review and change it to meet your own need if needed

- **Number Registrants**: How many registrants the system should send reminder each time the plugin runs. You should not set it to a high value to avoid timeout during sending emails (or reach the mail limit your hosting allow to be sent each hour). Default value is 15, should be enough.
- **Send To Group Billing**: Set to Yes to send reminder to group billing person (the person who making the group registration for multiple group members)
- **Send To Group Members**: Set to Yes to send reminder to group members in group registration
- **Send To Unpublished Events**: If set to Yes, the system will send reminder emails to registrants even that event was unpublished (For example, you configure the system to unpublish the event will it is full for some reasons)
- **BCC Email**: You can enter an email here if you want to monitor the reminder email. Each time the system send reminder email to your registrants, a copy of that email will be sent to the email you entered into that setting so that you can monitor it.

![system-eb-reminders-plugin](system-eb-reminders-plugin.png "system-eb-reminders-plugin")

## Use Cron Job
By default, Events Booking uses a system plugin to trigger sending reminder emails. That mean it requires someone access to the site (search engine bots are also counted) to trigger reminder process. Sometime, it is not reliable or causes multiple reminder emails sent to registrants in case your site has a very high traffic. To address that limitation, you can setup cron job from your hosting account to trigger sending reminder instead. Please see detailed instructions below:

1. Go to **System** -> **Plugins**, find the plugin **System - Events Booking Reminder**, click on it to edit. You should see a  parameter called **Trigger Reminder Code** . Enter a secret string there

2. Setup a cron job to make a request to this URL using CURL (note that you should use the CURL so that the variable can be passed in the GET request, see [https://stackoverflow.com/questions/11375260/cron-command-to-run-url-address-every-5-minutes](https://stackoverflow.com/questions/11375260/cron-command-to-run-url-address-every-5-minutes) for detailed instructions

**https://domain.com/index.php?trigger_reminder_code=SECRETCODE**

- Replace **https://domain.com/** with URL of your site
- Replace **SECRETCODE** with the secret string which you entered in the **Trigger Reminder Code** parameter

That will make the reminder only processed when there is a request made to that URL (which should be secret as no real users will access to that URL). It will make it more reliable compare to replying a system plugin.

![curl](curl.png "curl")


## Control the time reminder emails sent
By default, the reminder emails will be sent at a random time (it depends on when there are someone access to your site - even search engine bots- or when the cron job is triggered if you use cron job). That mean the reminder email could be sent at the midnight and you might not like it

If you want the reminder emails sent at a certain time in the day already (in the Time Zone configured in **Website Time Zone** config option in **System -> Global Configuration** of your site), you can use **Time Ranges** parameter inside the plugin. For example, set it to** 5,14** will make the system only send email reminder from **5am to 2pm**. Set it to **8,10;14:18** will allow sending  reminders between **8 to 10 am and 2pm to 6pm**.

## Log reminder emails
If you want, you can config the system to log reminder emails so that you can monitor it (when it is sent, what's the actual email subject and email message...). To do that, access to Events Booking -> Configuration, look at Mails Settings section, change Log Emails Types settings to Yes.

Now, each time the system sends reminder email, a copy of that email will be logged in database. You can access to Tools -> Emails Logs to see these logged emails.

## Want to Send More Reminder Emails

Follow the instructions at and you can configure each event to send up to 6 reminder emails [https://docs.joomdonation.com/eventsbooking/tools#support-up-to-6-reminders](https://docs.joomdonation.com/eventsbooking/tools#support-up-to-6-reminders)