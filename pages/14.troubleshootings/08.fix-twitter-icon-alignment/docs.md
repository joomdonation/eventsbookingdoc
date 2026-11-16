---
title: 'Fix twitter share icon alignment'
visible: true
---

Sometime, the twitter share icon  on event details page is not aligned properly (with facebook share icon). To fix that issue, Please go to Events Booking -> Configuration, look at Custom CSS tab, put this custom css code below, save it and the issue should be fixed

```css
#rsep_twitter {
margin-top: 4px;
}

