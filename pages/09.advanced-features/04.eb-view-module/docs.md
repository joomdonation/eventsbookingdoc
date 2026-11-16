---
title: 'EB View Module'
---

>>>This module is now deprecated and should be used for Events Booking older than 4.1.0 only. From Events Booking 4.1.0, please use [Easy View Module](/advanced-features/easy-view-module) which is much simpler to setup.


This is a special feature allow you to display a view in the extension (Calendar, Full Calendar, Upcoming events, Category, Event Detail, Registration Form of an event) inside a module on your site. (Normally, you will have to create a menu item to display a view in the extension)

1. Go to Extensions -> Modules, create a new instance of **Events Booking - View** module, assign it to the position you want in the template
2. Click on the module to edit and setup the value you want for the below parameters:

### The View parameter
You can choose the View you want to display in this parameter. It can be:
1. **Calendar**: Display Monthly Calendar like [http://joomdonationdemo.com/eventbooking/calendar](http://joomdonationdemo.com/eventbooking/calendar) in the module
2. **Full Calendar**: Display Full Calendar like [http://joomdonationdemo.com/eventbooking/full-calendar](http://joomdonationdemo.com/eventbooking/full-calendar) in the module
3. **Categories**: Display list of categories like [http://joomdonationdemo.com/eventbooking/events-categories](http://joomdonationdemo.com/eventbooking/events-categories) in the module
4. **Category**: Display events from a category like [http://joomdonationdemo.com/eventbooking/events-categories/joomla-events](http://joomdonationdemo.com/eventbooking/events-categories/joomla-events) in the module
5. **Event Detail**: Display details information of an event like [http://joomdonationdemo.com/eventbooking/events-categories/joomla-events/jandbeyond](http://joomdonationdemo.com/eventbooking/events-categories/joomla-events/jandbeyond) in the module
6. **Upcoming Events**: Display upcoming events (from one or all categories) like [http://joomdonationdemo.com/eventbooking](http://joomdonationdemo.com/eventbooking/) in the module
7. **Registration Form**: Display registration form of an event like [http://joomdonationdemo.com/eventbooking/zend-framework-1-fundamentals/individual-registration](http://joomdonationdemo.com/eventbooking/zend-framework-1-fundamentals/individual-registration) in the module
8. **Events Archive**: Display past events (from one or all categories) like [http://joomdonationdemo.com/eventbooking/features/other-features/events-archive](http://joomdonationdemo.com/eventbooking/features/other-features/events-archive) in the module
9. **Registration History**: Display registration history of a user in the module

### The Query String parameter
This paramer allow us to set query variables use for each view. It has this format **param1=value1&param2=value2&param3=value3**.... The query variables you can set depends on the View you want to display in the module as explained below:

1. **Calendar**:  Sample query string **id=3&month=4&year=2018&Itemid=138**. All the variables are optional.
- **id=3** means the system will display events from category = 3 in the module. If this variable is omitted, the system will display events from all categories.
- **month=4**  means the system will display events in April. If you leave it empty, the system will display events from current month.
- **year=2018** means the system will display events from 2018. If you leave it empty, the system will display events from current year.
- **Itemid=138** This is a special variable. In case you include this variable in query string, two things will happens: The system will use that menu item (ID = 138 in the sample) as default active menu item to generate link to the events diplayed in this module and it will also uses menu parameters to display the view (for example, show/hide page heading, page heading....). Usually, this could be ID of a hidden menu item to link to Calendar menu option of Events Booking (or a default menu item - for example, if you only have a menu item to link to upcoming events menu option of Events Booking on your site, you can use ID of that menu item here, too)

2. **Full Calendar**: Sample query string **Itemid=138**. The variable is optional
In case full calendar menu option, the only variable you can set for query string is **Itemid**. You should create a hidden menu item to link to full calendar menu option so that you can control what will be displayed in the calendar in the menu parameters (for example, show week/month/day button, date format....) and then set Query string Itemid=ID_OF_THAT_MENU_ITEM

3. **Categories**: Sample query string id=2&limit=20&Itemid=138. All variables are optional
- id=2 mean the system will all children categories of category with ID = 2 in the module. If you leave it empty, top level categories (parent = 0) will be displayed
- limit=20 will display max 20 categories in the module
- Itemid=138 means the system will use menu item with ID = 138 as default active menu item to generate link to each category (and also use settings of that menu item like show page heading, page heading...to display in the module, too). Usually, this could be ID of a hidden menu item to link to Categories menu option of Events Booking (or a default menu item - for example, if you only have a menu item to link to upcoming events menu option of Events Booking on your site, you can use ID of that menu item here, too)

4. **Category**: Sample query string id=2&layout=timeline&limit=20&Itemid=138. All variables are optional
- id=2 means the system will display events from category with id=2 in the module. If you don't have this variable here, events from all categories will be displayed
- layout=timeline will display events using timeline layout. It can have one of the following values (default,timeline,table,columns). If this variable is not added to Query String, default layout will be displayed
- limit=20 will display max 20 events in the module
- Itemid=138 means the system will use menu item with ID = 138 to generate link to each event display in the module (and also use settings of that menu item like show page heading, page heading...) to display in the module, too. Usually, this could be a hidden menu item to link to category menu option of Events Booking (or a default menu item - for example, if you only have a menu item to link to upcoming events menu option of Events Booking on your site, you can use ID of that menu item here, too)

5. **Event Detail**: Sample query string id=2&Itemid=138
- id=2 means the system will display event id=2 in the module.This is a required variable and needs to be id of a valid event
- Itemid=138 means the system will use menu item with ID = 138 to generate links in the module like register button links (and also use settings of that menu item like show page heading, page heading...) to display in the module, too. Usually, this could be a hidden menu item to link to event details menu option of Events Booking (or a default menu item - for example, if you only have a menu item to link to upcoming events menu option of Events Booking on your site, you can use ID of that menu item here, too)

6. **Upcoming events**: Sample query string id=2&layout=timeline&limit=20&Itemid=138. All variables are optional
- id=2 means the system will display events from category with id=2 in the module. If you don't have this variable here, events from all categories will be displayed
- layout=timeline will display events using timeline layout. It can have one of the following values (default,timeline,table,columns). If this variable is not added to Query String, default layout will be displayed
- limit=20 will display max 20 events in the module
- Itemid=138 means the system will use menu item with ID = 138 to generate link to each event display in the module (and also use settings of that menu item like show page heading, page heading...) to display in the module, too. Usually, this could be a hidden menu item to link to upcoming events menu option of Events Booking (or a default menu item - for example, if you only have a menu item to link to upcoming events menu option of Events Booking on your site, you can use ID of that menu item here, too)

7. **Registration Form**: Sample query string event_id=2&Itemid=138
- event_id=2 means the system will display registration form of event with ID = 2 in the module.
- Itemid=138 means the system will use menu item with ID = 138 as active menu item. Usually, this could be a hidden menu item to link to registration form of that event (or a default menu item - for example, if you only have a menu item to link to upcoming events menu option of Events Booking on your site, you can use ID of that menu item here, too)

8. **Events Archive**: Sample query string id=2&layout=table&limit=20&Itemid=138
- id=2 means the system will display events from category with id=2 in the module. If you don't have this variable here, events from all categories will be displayed
- layout=table will display events using table layout. It can have one of the following values (default,table). If this variable is not added to Query String, default layout will be displayed
- limit=20 will display max 20 events in the module
- Itemid=138 means the system will use menu item with ID = 138 to generate link to each event display in the module (and also use settings of that menu item like show page heading, page heading...) to display in the module, too. Usually, this could be a hidden menu item to link to upcoming events archive menu option of Events Booking (or a default menu item - for example, if you only have a menu item to link to upcoming events menu option of Events Booking on your site, you can use ID of that menu item here, too)

9. **Registration History**: Sample query string Itemid=138
Itemid=138 means the system will use menu item with ID = 138 to as acive menu item generate links displayed in the module (and also use settings of that menu item like show page heading, page heading...) to display in the module, too. Usually, this could be a hidden menu item to link to registration history menu option of Events Booking





