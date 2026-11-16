---
title: 'Enable Captcha'
---

If you want to enable Captcha to Events Booking to prevent spams, please follow the instructions below:

1. Configure your site to use recaptcha, see instructions from Joomla documentation at [https://docs.joomla.org/J3.x:Google_ReCaptcha](https://docs.joomla.org/J3.x:Google_ReCaptcha). If you are using a captcha plugin which is not working well with Events Booking, consider using our [JD Captcha](https://joomdonation.com/joomla-extensions/jd-captcha.html) plugin.
2. Go to **System** -> **Global Configuration**, make sure **Default Captcha** config option set to the captcha plugin which you want to use.
3. Go to **Events Booking** -> **Configuration**, set the config option **Enable Captcha** to **Yes**.

When you do that, captcha will be enabled on Registration Form, Submit Event Form, Invite Friend Form to protect Events Booking from being spammed

>>> Some of third party captcha plugins like Recaptcha Version 3, HCapcha won't work for group registration in Events Booking. So if you use Group Registration, please just use invisiable repcaptcha plugin comes with Joomla core. Or you can use our [JD Captcha Plugin](https://joomdonation.com/joomla-extensions/jd-captcha.html)






