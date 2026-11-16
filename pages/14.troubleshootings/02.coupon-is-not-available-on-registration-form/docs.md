---
title: 'Coupon is not available on registration form'
---

After creating coupon codes in Events Booking, you go to frontend of your site, try to register for an event but still don't see coupon input available for you to enter coupon code to receive discount. That might hapen because:

1. You haven't enabled coupon feature yet. Go to Events Booking -> Configuration, check and make sure **Enable Coupon** parameter set to Yes.
2. You will also check and make sure there is at least one valid coupon code is available for the event you are registering for;
- Check **Coupon Assignment** setting, set it to All Events. If it is set to All Selected Events, then please check and make sure the event you are registering for is selected in th Event parameter 
- Check and make sure current date is between **Valid From Date** and **Valid To Date** setting of the coupon. Better, leave the two settings empty.
- Check Access setting of the coupon, try to change it to Public.
