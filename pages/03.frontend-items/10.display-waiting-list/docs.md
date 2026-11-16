---
title: 'Display Waiting List'
media_order: 'registrants-list.png,view-registrants-list-permission.png'
taxonomy:
    category:
        - docs
---

If you let users join a waiting list when an event is full, you can display that list on the frontend.

## Enable viewing registrants list

1. Go to **Events Booking -> Configuration**, look at **Themes** tab, find the config options **Show Number Waiting List
**  and  **Show List Of Waiting List** , set it to **Yes**.
2. **Permission configuration**: Go to **Events Booking -> Configuration** (or any pages in Events Booking in the administrator area), click the **Options** button in the toolbar, select the user group(s) you want to allow viewing registrants list (for example, Public group), set **View Registrant List** permission to **Allowed**. Please note that permission settings in Joomla are inherited, so when you enable this permission for a user group (**Public** in this example), all it's children groups (Registered, Editor, Publisher.... in this example) will have this permission allowed, too.

![view-registrants-list-permission](view-registrants-list-permission.png "view-registrants-list-permission")

## Control what information is displayed on registrants list
By default, Events Booking only display the following information on registrants list page: **First Name, Last Name, Number Registrants, Registration Date**. If you want to display additional fields, you will need to go to Events Booking -> Custom Fields, click on the custom fields you want to display to edit, set **Show On Public Registrants List** parameter to Yes.

You can also display an event’s waiting list using the **Events Booking - Waiting List** plugin. See [https://docs.joomdonation.com/eventsbooking/plugins/waiting-list](https://docs.joomdonation.com/eventsbooking/plugins/waiting-list).
