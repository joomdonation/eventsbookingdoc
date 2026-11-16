---
title: 'Event Without Specific Date'
visible: true
---

Sometime, you will want to create an event without knowing exactly the event date yet. In this case, you can set Event Date to this special date **2099-12-31 00:00:00**. With that setup, when event is displayed, instead of displaying that date, the system will display this text **To be confirmed** (You can go to Events Booking -> Configuration, find and change EB_TBC language item to change that text to meet your need if needed)

>>> Some severs might not be able to handle the large date 2099-12-31 00:00:00, and if it happens on your site (the date could not be saved and be empty, change to use 2030-12-31 00:00:00)