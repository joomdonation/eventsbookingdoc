---
title: 'Content Restriction'
---

This plugin allows you to restrict access to part of Joomla article to registrants of the events you want only (or on any page which implement Joomla content plugin like in K2 item). 

If you want to use this plugin:
1. Go to Extensions, Plugins, find and publish the plugin **Content - Events Booking Content Restriction**
2. Edit the article you want to display this event, enter this syntax **{ebrestriction ids="ID_OF_EVENTS"}The restricted text goes here{/ebrestriction}**:
- **ID_OF_EVENTS** is IDs of the events - comma separated. For example **{ebrestriction ids="1,2,4,5"}The restricted text goes here{/ebrestriction}** will only show the text **The restricted text goes here** if the current logged in user has registered for at least one event with ID = 1 or ID = 2 or ID = 4 or ID = 5.
- If you use this syntax **{ebrestriction ids="\*"}The restricted text goes here{/ebrestriction}**, the text **The restricted text goes here** will be shown if the current logged in user has registered for at least one event in your system