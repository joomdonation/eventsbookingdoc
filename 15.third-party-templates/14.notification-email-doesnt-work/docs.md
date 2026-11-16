---
title: 'Notification Email doesn''t work'
---

If registrants don’t receive confirmation emails and administrators don’t receive notifications, check the following settings.

1. Log in to your site’s administrator area. Go to System - Global Configuration, open the Server tab, and find the mail settings. Send a test email and check whether it arrives. If it doesn’t, review the mail settings or contact your hosting provider.
2. Go to Events Booking -> Configuration and find Mail Settings. If From Name and From Email contain custom values, clear both and test again. If email works with the default values from Global Configuration, correct the custom values or leave the fields blank.
3. Test with a different email address. If delivery works for one address but fails for another, ask your hosting provider to check the mail server.
4. Go to Events Booking -> Configuration, there is a setting called Log Emails Types. Choose to log New Registration Emails, then test it again. After completing the subscription, go to Events Booking -> Registrants for example, access to Tools -> Emails  Logs. If you see some emails displays there, that mean Events Booking already calls Joomla API for sending email. If email is not delivered for some reason, it is a problem with mail server of your hosting provider. Please try to contact them, ask them to check their server logs to see why email is not delivered. They should be able to check and tell you the reasons so that you can correct it.