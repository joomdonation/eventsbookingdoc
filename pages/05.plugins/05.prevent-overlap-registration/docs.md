---
title: 'Prevent Overlap Registration'
visible: true
published: true
---

This plugin is used to prevent users from registering for event which overlap time with the events which he registered before. If he is logged in, the system will check base on Joomla User ID of his account, otherwise, the check will be based on the email he entered on registration form. To use this feature, Go to **System** -> **Plugins**, find the plugin **Events Booking - Prevent Overlap Registration**, enable it.

- If the event does not have event end date, it will be considered as overlap with other events if the event date of that event is between start date and end date of one of the events which the user registered before.
- If the event has event end date, it will be considered as overlap with other events in one of the 3 cases before:

1. event_date is between the start and end date of the other event
2. event_end_date is between the start and end date of the other event
3. One of the registered event is between start date and end date of the current being registered event


Be careful when you enable this plugin. You only need to enable it if you really want to prevent overlap registration.
