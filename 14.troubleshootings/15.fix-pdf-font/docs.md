---
title: 'Fix PDF Font'
media_order: tiny-mce-parameters.png
published: true
---

If special characters render incorrectly in PDF invoices or tickets, select a PDF font that supports your language.

1. Log in to the administrator area of your site
2. Open this URL to download all available PDF fonts into your site https://domain.com/administrator/index.php?option=com_eventbooking&task=tool.download_and_set_font
(replace **https://domain.com/administrator** with administrator URL of your site)
3. Go to Events Booking -> Configuration and open the PDF Settings tab. Use **PDF Font** to select a font that displays the characters for your language.

- Maybe you should try to choose from one of the following first **freesans**, **dejavuserif** or **Freeserif**. These UTF8 fonts should work for your language.
- If not, try to Google for the font for your language. Something like "TCPDF font for German language", "TCDPF font for Greek language". If you see some font, then choose it from the above config option.