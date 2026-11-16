---
title: 'Export Registrants PDF'
published: true
media_order: registrants-export-pdf.png
---

Beside allow export registrants into Excel, Events Booking also allows you to export registrants into a simple PDF file. Similar to [Export Registrants](/registrants-management/export-registrants), you can filter registrants you want to export (for example, select an event, choose status filter or event check on the checkboxes next to the registration record before clicking on **Actions -> Export PDF** button in the toolbar to export these filtered registrants into PDF.

![registrants-export-pdf](registrants-export-pdf.png "registrants-export-pdf")

## Customized PDF Layout

Due to limitation of PDF, the exported PDF file could not contains any fields. It only contains some very basic fields and you might want to customize it to meet your need. In this case, you will need to modify the layout file in **components/com_eventbooking/themes/default/common/registrants_pdf.php**

Once the change is done and works for your need, please move that modified file to administrator/templates/isis/html/com_eventbooking/common folder so that the change won't be lost when you update to future releases of the extension

If you use this feature from frontend registrants management, the modified file need to be copied to PATH_TO_TEMPLATE/html/com_eventbooking/common folder, too (PATH_TO_TEMPLATE is path to the template uses for frontend of your site)