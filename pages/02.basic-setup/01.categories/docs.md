---
title: Categories
media_order: 'categories.png,new_category.png'
taxonomy:
    category:
        - docs
process:
    markdown: true
    twig: true
---

**Events Booking** lets you organize events into categories and subcategories. You can nest categories at any depth.

Open the categories management page in any of these three ways.

1. Go to **Events Booking -> Categoires**.
2. Open the Events Booking Dashboard and click the Categories icon.
3. From any Events Booking page, go to **Setup -> Categories**.

![Categories](categories.png)

## Add new category
Click **New** in the toolbar to create a category. The form below opens.

![Add New Category](new_category.png)


### General Information
<table class="table table-stripped table-bordered table-considered">
<thead>
<tr><th width="15%">Property</th><th>Description</th></tr>
</thead>
<tbody>
<tr>
<td><strong>Name</strong></td>
<td>The category name visitors see.</td>
</tr>
<tr>
<td><strong>Alias</strong></td>
<td>The alias is used in URLs for the category and its events. If you leave it blank, Events Booking generates an alias from the category name.</td>
</tr>
<tr>
<td><strong>Parent</strong></td>
<td>Choose a parent category, or select <strong>Select Category</strong> to create a top-level category.</td>
</tr>
<tr>
<td><strong>Image</strong></td>
<td>Choose the image to display in the categories list and on the category details page.</td>
</tr>
<tr>
<td><strong>Layout</strong></td>
<td>Choose how to display events from this category. The four supported layouts are Default Layout, Table Layout, Calendar Layout, and Timeline Layout.</td>
</tr>
<tr>
<td><strong>Color</strong></td>
<td>Choose the color used for events in this category on the calendar.</td>
</tr>
<tr>
<td><strong>Background color</strong></td>
<td>Choose the background color for events in this category on the calendar.</td>
</tr>    
<tr>
<td><strong>Keywords</strong></td>
<td>An optional comma-separated list of keywords and/or phrases to be used in the HTML output.</td>
</tr>
<tr>
<tr>
<td><strong>Meta Description</strong></td>
<td>An optional paragraph to be used as the description of the page in the HTML output. This will generally display in the results of search engines.</td>
</tr>
<tr>
<td><strong> Access Level</strong></td>
<td>Choose who can see this category. Select Public for a category everyone can see.</td>
</tr>
<tr>
<td><strong> Submit Event Access Level</strong></td>
<td>Choose the access level required to submit events to this category from the frontend.</td>
</tr>    
<tr>
<td><strong>Custom Detail URL</strong></td>
<td>Enter a custom URL for the category page if you need one, such as when you build the page with a page builder. Otherwise, leave the field blank.</td>
</tr>        
 <tr>
<td><strong>Payment Methods</strong></td>
<td>Choose the payment methods available for events in this category. An event can override this setting. If you leave it blank, all published payment methods are available.</td>
</tr>           
<tr>
<td><strong>Description</strong></td>
<td>Enter a description to display on the categories list page.</td>
</tr>
</tbody>
</table>

### Messages

Messages entered here override the global messages in Events Booking -> Emails & Messages for events in this category. Events Booking chooses the message for each event in the following order.

- Messages configured for the event.
- Messages configured for the category.
- Global messages configured in Events Booking -> Emails & Messages.