---
title: MPDF
taxonomy:
    category:
        - docs
published: true
---

By default, Events Booking uses TCPDF library to generate PDF (invoices, member cards). While it is good, does not have good support for css and good documentation, so we decided to implement a new plugin called **Events Booking - MPDF** to address these limitations. 

- If you use **Joomla 3 or Joomla 4**, please download the plugin at [https://joomdonation.com/downloads/plg_eventbooking_mpdf.zip](https://joomdonation.com/downloads/plg_eventbooking_mpdf.zip)
- If you use **Joomla 5**, **Joomla 6**, [https://joomdonation.com/downloads/plg_eventbooking_mpdf_joomla5.zip](https://joomdonation.com/downloads/plg_eventbooking_mpdf_joomla5.zip)

2. Go to **System** -> **Install** -> **Extensions**, install the downloaded plugin.
3. Go to **System** -> **Plugins**, find and enable **Events Booking - MPDF** plugin.
4. Access to Events Booking , then **Tools -> Download MPDF Fonts** to download fonts required for MPDF library to work. These fonts have large size, so we could not ship with Events Booking package by default.
5. The best thing about MPDF is that it supports css very well (see [https://mpdf.github.io/css-stylesheets/introduction.html](https://mpdf.github.io/css-stylesheets/introduction.html) for full documentation), so you should enter necessary css code to improve the layout of the generated PDF file. There are two ways to enter css code for PDF layouts as described below:

## Use PDF CSS config option
1. Go to **System** -> **Plugins**, make sure **Editor - CodeMirror** plugin is enabled.
2. Go to **Events Booking** -> **Configuration**, look at **PDF Settings** tab, look at **PDF CSS** and enter css code to change appearance of PDF file there.

## Enter CSS Code into CSS file directly

- The common css code for PDF can be entered into **plugins/eventbooking/mpdf/css/pdf.css**
- The css code for **PDF Invoices** can be entered into **plugins/eventbooking/mpdf/css/invoice.css**
- The css code for **PDF Tickets** can be entered into **plugins/eventbooking/mpdf/css/ticket.css**
- The css code for **PDF Certificates** can be entered into **plugins/eventbooking/mpdf/css/certificate.css**


## Use Custom Font
The MPDF library only supports certain fonts. If you want to use custom TTF fonts :
- Upload these font files to plugins/eventbooking/mpdf/mpdf/ttfonts folder.
- Create file **plugins/eventbooking/mpdf/config.php** with the content below (You actually can just rename the file **plugins/eventbooking/mpdf/config.php.dist** and adjust it) :

```php
<?php
/**
 * @package        Joomla
 * @subpackage     Events Booking
 * @author         Tuan Pham Ngoc
 * @copyright      Copyright (C) 2010 - 2023 Ossolution Team
 * @license        GNU/GPL, see LICENSE.php
 */

defined('_JEXEC') or die;

// This is a sample config.php file which can be used to load custom font into MPDF, see https://mpdf.github.io/fonts-languages/fonts-in-mpdf-7-x.html for documentation
return [
	'fontdata'     => [ // lowercase letters only in font key
		'frutiger' => [
			'R' => 'Frutiger-Normal.ttf',
			'I' => 'FrutigerObl-Normal.ttf',
		],
	],
	'default_font' => 'frutiger',

	// You can also pass following custom config keys with it values to override default settings if needed

	//	'default_font_size' => 10,
	//	'margin_left'       => 0,
	//	'margin_top'        => 0,
	//	'margin_right'      => 0,
	//	'margin_bottom'     => 0,
	//	'margin_footer'     => 0,
];
```

As you can see from the code above, frutiger is font family, **Frutiger-Normal.ttf** is the font file for Regular style, **FrutigerObl-Normal.ttf** is the font file for Italic style. See [https://mpdf.github.io/fonts-languages/fonts-in-mpdf-7-x.html](https://mpdf.github.io/fonts-languages/fonts-in-mpdf-7-x.html) for more details documentation

5. Use css font-family to set font use to generate PDF if needed [](https://developer.mozilla.org/en-US/docs/Web/CSS/font-family)

```css
<style>
body
{
 font-family: "Times New Roman";
}   
</style>
```