---
title: 'Use Email Logs'
published: true
---

Sometime, you could see that email could not be delivered to administrator or registrants from your site. To troubleshot this problem, you can use Emails Logs feature in the extension:

1. Go to Events Booking -> Configuration, set **Log Emails** config option to **Yes**
2. Then register for the event again. If the event is a paid event, you will need to pay for the subscription (or use offline payment method) for the email to be sent.
3. Access to Events Booking, then Tools -> Emails Logs. There it will display logged emails:
- If you see the email for your test registration logged there, that mean Events Booking has called Joomla! API to send email to registrant and administrator already. If they do not receive email for some reasons, try to change to use a different email. If it still does not work, you need to contact the hosting provider, ask them to check to see why email is not delivered (it's the job of mail server to deliver email, so if email could not be delivered, it is out of Events Booking control)
- If you do not see email logged, that mean there is something wrong with Events Booking. In this case, please submit a support ticket so that we can check it further.