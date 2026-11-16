---
title: 'Prevent Overlap Registration'
visible: true
published: true
---

This plugin prevents users from registering for an event that overlaps with one they have already registered for. It identifies logged-in users by their Joomla user ID and other users by the email address entered on the registration form. To use it, go to **System** -> **Plugins** and enable **Events Booking - Prevent Overlap Registration**.

- If the event does not have event end date, it will be considered as overlap with other events if the event date of that event is between start date and end date of one of the events which the user registered before.
- If the event has event end date, it will be considered as overlap with other events in one of the 3 cases before:

1. event_date is between the start and end date of the other event
2. event_end_date is between the start and end date of the other event
3. One of the registered event is between start date and end date of the current being registered event


Be careful when you enable this plugin. You only need to enable it if you really want to prevent overlap registration.
