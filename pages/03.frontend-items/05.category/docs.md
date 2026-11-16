---
title: Category
media_order: 'upcoming_events_timeline_layout.png,upcoming_events_columns_layout.png,upcoming_events_default_layout.png,upcoming_events_table_layout.png,category_menu_options.png'
---

**Category** page displays list of events from a certain category. Users can access to this category page from Categoires page, from menu item or from Categories module. From this page, users can see list of events, click on an event to see details information of that event or click on register buttons to register for the event they want. Similar to upcoming events, there are 4 menu options/lauouts you can use to display events

## Category - Timeline Layout
![Category - Timeline Layout](upcoming_events_timeline_layout.png)

To use this layout, you need to create a menu item to link to **Category - Timeline Layout** menu item type of **Events Booking**. Personal, I think this is the nicest layout to display events from a category. 

## Category - Default Layout
![Category - Default layout](upcoming_events_default_layout.png)

To use this layout, you need to create a menu item to link to **Category - Default Layout** menu item type of **Events Booking**. 

## Category - Table Layout
![Category - Table layout](upcoming_events_table_layout.png)

To use this layout, you need to create a menu item to link to **Category - Table Layout** menu item type of **Events Booking**. 

## Category - Columns Layout
![Category - Columns layout](upcoming_events_columns_layout.png)

To use this layout, you need to create a menu item to link to **Category - Columns Layout** menu item type of **Events Booking**. 

## Menu parameters
All the menu options to display upcoming events have same set of parameters. Beside common Joomla menu items parameters, these menu options support the following parameters specific to Events Booking:

### Details tab
- **Category**: If you choose a category in this parameter, the system will display all children categories of that selected category, otherwise, top level categories will be displayed

### Options tab
- **Display Events Type**: Choose the event type which will be displayed on this menu item:

+ **Use Global**:  Depend on **Hide Past Events** config option. If the config option set to Yes, only upcoming events will be displayed. If set to No, all events will be displayed.
+ **All Events**: Will display both past and future events.
+ **Upcoming Events**: Only display upcoming events. Past Events won't be displayed.
+ **Past Events**: Only display past events (event date smaller than current date).
- **Categories**: You can select some categories in this parameter and only events from these selected categories will be displayed.
- **Exclude Categories**: You can select some categories in this parameter and events from these selected categories won't be displayed.
- **Locations**: You can select some locations in this parameters and only events from these selected locations will be displayed.
- **Speakers**: You can select some speakers here and only events have these speakers will be displayed.
- **From Date**: If you you select a date here, only events with **Event Date** greater than or equal this selected date will be displayed.
- **To Date**: If you select a date here, only events with **Event Date** smaller than or equal this selected date will be displayed.
- **City**: If you enter a city here, events belong to that City will be displayed.
- **Hide Past Events**: If set to **Yes**, past events (event date smaller than current date) won't be displayed in the calendar. If set to **No**, both past and future events will be displayed. Set it to Use **Global Configuration** to use the value of Hide Past Events which you set in Events Booking configuration.
- **Hide Children Categories**: Control whether sub-categories of the current displayed category (category selected in **Select Category** parameter in **Details** tab) are displayed. Set to Yes to have these sub-categories displayed and set to No to have these sub-categories hidden.
- **Hide Children Events**: If you don't want to display children events (created by additional dates plugin plugins or recurring events), set this parameter to Yes. By default, it is No and both parent and children events will be displayed.
- **Only Show Featured Events**: Set to Yes if you only want featured events to be displayed on this page. Set to No and both featured and none-featured events will be displayed.
- **Number Events**: The number of events displayed per page. If there are more upcoming events than that number, pagination will be displayed to allow navigating to different pages to view other events.
- **Default Duration Filter**: Choose the duration and only events within this selected duration will be displayed. Supported duration including: **Today**, **Tomorrow**, **This Week**, **Next Week**, **This Month**, **Next Month**.
- **Order By**: Choose the ordering of events displayed on this page. Supported options: **Use Configuration**, **Event Title**, **Event Date**, **Ordering**.
- **Order Direction**: Choose the order direction for events displayed on this page. Supported options: **Use Configuration**, **ASC**, **DESC**.
- **Override Menu Item ID**: By default, the current menu item will be used as default active menu to generate links to event detail page from the calendar. If for some reasons, you want to use different menu item (for example, when this menu item is a Homepage and you want to navigate to different page when users click on event on this calendar, enter the active menu item you want into this parameter). Usually, this should be empty.
- **Intro Text**: If you want to have some text displayed at the beginning of this page, enter that text into this parameter. Please note that this text will only be displayed if you do not select any category in **Select Category** parameter in Details tab. If you select a category there, **Description** of the selected category will be displayed instead of this **Intro Text**.

![Category Menu Options](category_menu_options.png)