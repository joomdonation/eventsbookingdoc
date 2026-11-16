---
title: 'Link To Event Or Registration Form Of Old Event'
published: true
---

Sometime, you can see that click on Details button or Register button of your current event link to an old or not-existing event. It causes by how the routing works in Events Booking. To address this issue, there are two ways :

1. Go to Events Booking -> Configuration, look at SEF Router Settings tab, set Insert Event ID config option to Yes. It will insert ID of the event to the URL, so it will never be the same with an old or deleted event and it will prevent the issue from happening.
2. If you do not like the ID of the event to be added to URL,  go to Events Booking, then Tools -> Purge URLs to remove the cached URLs. After that, access to the original page which display events again, and click on the button, it will be linked to the right event

