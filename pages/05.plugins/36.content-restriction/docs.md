---
title: 'Content Restriction'
---

Make part of a Joomla article available only to registrants of selected events. It also works on other pages that run Joomla content plugins, such as K2 items.

To use this plugin, follow these steps.
1. Go to Extensions, Plugins, find and publish the plugin **Content - Events Booking Content Restriction**
2. Edit the article you want to display this event, enter this syntax **{ebrestriction ids="ID_OF_EVENTS"}The restricted text goes here{/ebrestriction}**:
- **ID_OF_EVENTS** is IDs of the events - comma separated. For example **{ebrestriction ids="1,2,4,5"}The restricted text goes here{/ebrestriction}** will only show the text **The restricted text goes here** if the current logged in user has registered for at least one event with ID = 1 or ID = 2 or ID = 4 or ID = 5.
- If you use this syntax **{ebrestriction ids="\*"}The restricted text goes here{/ebrestriction}**, the text **The restricted text goes here** will be shown if the current logged in user has registered for at least one event in your system