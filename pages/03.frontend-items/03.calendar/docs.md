---
title: Calendar
media_order: 'calendar.png,calendar_parameters.png'
---

Calendar menu option displays your events on a nice calendar. Users can browse for your events per month, per week or per day from this calendar

![Calendar](calendar.png)

To use this layout, you need to ceate a menu item to link to **Monthly Calendar** menu option of **Events Booking**. Beside common Joomla menu items parameters, this menu option supports the following parameters specific to Events Booking:

### Details tab
- **Category**: If you select a category here, only events from that selected category will be displayed. 

### Options tab

![Calendar menu parameters](calendar_parameters.png)

- **Categories**: You can select some categories in this parameter and only events from these selected categories will be displayed.
- **Exclude Categories**: You can select some categories in this parameter and events from these selected categories won't be displayed.
- **Location**: You can choose a location in this parameter and only events from that location will be displayed.
- **Default Month**: Choose the month which you want to display events from when the Calendar is first loaded. Set it to **Current Month** to display events from current month.
- **Default Year**: Enter the year which you want to display events from when the calendar is first loaded. Leave it empty to display events from current year.
- **Hide Past Events**: If set to **Yes**, past events (event date smaller than current date) won't be displayed in the calendar. If set to **No**, both past and future events will be displayed. Set it to **Use Global Configuration** to use the value of **Hide Past Events** which you set in Events Booking configuration.
- **Hide Children Events**: If you don't want to display children events (created by additional dates plugins or recurring events), set this parameter to **Yes**. By default, it is **No** and both parent and children events will be displayed.
- **Link Event To Registration Form**: If set to Yes, users will be redirected to Registration Form of the event to process registration when they click on event title in calendar. If set to No, users will see event details page when click on event title.
- **Show Event Icon**: If set to Yes, there will be an icon displayed next to event title on the calendar.
- **Hide Full Events**: If set to Yes, full events won't be displayed in the calendar.
- **Override Menu Item ID**: By default, the current menu item will be used as default active menu to generate links to event detail page from the calendar. If for some reasons, you want to use different menu item (for example, when this menu item is a Homepage and you want to navigate to different page when users click on event on this calendar, enter the active menu item you want into this parameter). Usually, this should be empty.
- **Intro Text**: If you want to have some text displayed at the beginning of this page, enter that text into this parameter.