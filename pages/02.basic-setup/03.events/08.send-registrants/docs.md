---
title: 'Send Registrants'
published: true
---

This feature allows you to send registrants list of an event (in Excel Format) to email of administrators (and owner of event if **Send Notification Email To Event Creator** config option to **Yes**). To use this feature:

1. Go to **Events Booking** -> **Emails & Messages**, look at **Registration Email Messages** tab, configure subject and body of the email:

- Send Registrants List Email Subject
- Send Registrants List Email Body

You can use any tags listed in this page [Event Information Tags](/email-tags/common-tags#event-information-tags) to include event information in the email message. You can also use [TOTAL_REGISTRANTS] tag to show total number registrants of the event in the email.

2. Go to Events Booking -> Events, check on the checkbox next to the events you want to send registrants list to administrator,  and press **Actions -> Send Registrants** button in the toolbar.

When you do that, the system will export registrants of each event to an excel file and send it to administrators (configured in Notification Emails settings inside the event or in Events Booking configuration) and the creator of the event (if configured as mentioned above)