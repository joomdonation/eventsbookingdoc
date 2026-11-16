---
title: 'Google Map Error & Solution'
---

Recently, Google Map API changed their policy: Now each site must registers and use an own Google Map API Key. So if you still use default Google Map API Key shipped with Events Booking by default, you will receive some kind of errors when the map is being displayed. To solve it:

1. For now, you can go to Events Booking -> Configuration, empty the value of **Google Map API Key** config option. At the moment, it works for because for some reasons, Google allows us to use their API without an API Key. But they might changed that in the future
2. Follow the instuctions at [https://developers.google.com/maps/documentation/javascript/get-api-key](https://developers.google.com/maps/documentation/javascript/get-api-key) , register for a new Google Map API Key for your site. Then go to Events Booking -> Configuration, enter that new API Key into Google Map API Key config option, save it. Allows Google requires you to provide billing address, they give you free 200$ credit to use per month, mean free:

- **100,000 Static Maps web loads** (uses for map display on event details page or when users click on a location link)
- **10,000 Autocomplete sessions** (uses for creating locations from backend)

So unless your site is very big, you should not have to pay at all (these free usage limit is more than enough). So don't be affaid off and go ahead to register for an own API Key uses for the site

For more details about their pricing, please see [https://cloud.google.com/maps-platform/pricing/](https://cloud.google.com/maps-platform/pricing/)