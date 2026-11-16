---
title: 'How to use 24-hours date format?'
visible: true
---

Date Format in Events Booking is configurable. To use 24-hours date format (instead of 12-hours format by default), please go to Events Booking -> Configuration, change:

- Event Date Format config option to m-d-Y H:i
- Time Format config option to H:i

See [https://www.php.net/manual/en/function.date.php](https://www.php.net/manual/en/function.date.php) for list of supported parameters


## Change Date Format for Full Calendar
Full Calendar is a modern javascript calendar application, so the date format configuration is different. To change Time Format in Full Calendar to 24 hours format, you need to edit the menu item you created, change **Time Format Month** to parameter to **HH:mm** . See [https://momentjs.com/docs/#/displaying/format/](https://momentjs.com/docs/#/displaying/format/) for list of supported parameters which you can use to change Date and Time format in Full Calendar