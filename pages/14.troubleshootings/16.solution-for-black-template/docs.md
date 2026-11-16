---
title: 'Solution For Black Template'
media_order: tiny-mce-parameters.png
published: true
---

If you are using a blank template for your site, Events Booking layout might not look very well. For this, you need to add some small custom template. Go to Events Booking -> Configuration, look at Custom CSS tab, put these custom css code there:

```css
#eb-categories .eb-description, #eb-event-page .eb-description, #eb-events .eb-description, #eb-categories .eb-box-heading, #eb-events .eb-box-heading, #eb-event-page .eb-box-heading
{
  background-color: transparent;
}

.table-striped tbody tr:nth-child(2n+1) td, .table-striped tbody tr:nth-child(2n+1) th
{
  background-color: transparent !important;
}

#eb-categories .eb-box-heading, #eb-events .eb-box-heading, #eb-event-page .eb-box-heading
{
  color: #fff !important;
}
```
With these small custom css, it will look better.