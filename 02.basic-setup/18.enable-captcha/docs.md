---
title: 'Enable Captcha'
---

Use the following steps to enable Captcha in Events Booking and reduce spam.

1. Configure reCAPTCHA for your site. See the Joomla instructions at [https://docs.joomla.org/J3.x:Google_ReCaptcha](https://docs.joomla.org/J3.x:Google_ReCaptcha). If your CAPTCHA plugin does not work with Events Booking, you can use the [JD Captcha](https://joomdonation.com/joomla-extensions/jd-captcha.html) plugin.
2. Go to **System** -> **Global Configuration** and set **Default Captcha** to the plugin you want to use.
3. Go to **Events Booking** -> **Configuration**, set the config option **Enable Captcha** to **Yes**.

This enables CAPTCHA on the Registration Form, Submit Event Form, and Invite Friend Form to protect them from spam.

>>> Some of third party captcha plugins like Recaptcha Version 3, HCapcha won't work for group registration in Events Booking. So if you use Group Registration, please just use invisiable repcaptcha plugin comes with Joomla core. Or you can use our [JD Captcha Plugin](https://joomdonation.com/joomla-extensions/jd-captcha.html)






