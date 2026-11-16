---
title: 'How to use 24-hours date format?'
visible: true
---

To switch Events Booking from its default 12-hour clock to a 24-hour clock, go to Events Booking -> Configuration and change the following settings.

- Event Date Format config option to m-d-Y H:i
- Time Format config option to H:i

See [https://www.php.net/manual/en/function.date.php](https://www.php.net/manual/en/function.date.php) for a list of supported parameters


## Change Date Format for Full Calendar
Full Calendar uses different date and time formats. To use a 24-hour clock, edit the Full Calendar menu item and set **Time Format Month** to **HH:mm**. See [https://momentjs.com/docs/#/displaying/format/](https://momentjs.com/docs/#/displaying/format/) for the supported date and time format parameters.