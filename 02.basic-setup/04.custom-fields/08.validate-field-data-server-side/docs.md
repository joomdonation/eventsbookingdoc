---
title: 'Validate Field Data - Server Side'
---

In addition to [client side validation](http://eventbookingdoc.joomservices.com/basic-setup/custom-fields/validate-field-data-client-side), Events Booking has supported server-side validation in PHP since version 3.5.0. You can use built-in validators or implement your own. To apply them to a field, edit the field and enter the rules in **Server Validation Rules**.
## Built-in validators

Events Booking uses the **Valitron Validation** library to validate custom field data. See https://github.com/vlucas/valitron#built-in-validation-rules for the built-in validators.

The syntax which you can enter into **Server Validation Rules** is **rule1|rule2:param1,param2**. Basically:
- To validate the field with more than one rule, separate the rules with the | character.
- You can add parameters to rule by adding : character after rule name, list of parameters separated by commas

Examples:
* **min:10**: will force the field to be a a number greater than or equal 10
* **max:10**: will force the field to be a a number smaller than or equal 10
* **length:10**: will force the field to be a string with exactly 10 characters
* **lengthMin:10**: will force the field to be a string has at least 10 characters
* **lengthMax:10**: will force the field to be a string has maximum 10 characters
* **lengthBetween:5,15**: will force the field to be a string with minimum 5 characters and maximum 15 characters

## Build custom validators

To validate a field using your own logic, create a custom validator as follows.

1. Create a field **custom_validator.php** and upload it to **components/com_eventbooking/helper** folder on your site
2. Edit that file, add the code like below to the file:

```php
<?php
/**
 * @package            Joomla
 * @subpackage         Event Booking
 * @author             Tuan Pham Ngoc
 * @copyright          Copyright (C) 2010 - 2018 Ossolution Team
 * @license            GNU/GPL, see LICENSE.php
 */

defined('_JEXEC') or die;

Valitron\Validator::addRule('my_custom_rule', function($field, $value, array $params, array $fields) {
    if (strlen($value) != 9)
	{
			return false;
	}
	
    return true;
}, 'The field must has exactly 9 characters');

Valitron\Validator::addRule('my_custom_rule2', function($field, $value, array $params, array $fields) {
    if ($value != 9)
	{
			return false;
	}
	
    return true;
}, 'The field must has value = 9');


```
Each rule contains a block of code like that with the following parameters:
- $field: Name of the field which the rule is applied
- $value: Value of that field
- $params: Array of parameters which users passed to the rule when setting up the server validation rules
- $fields: Array contains data of other fields in the form

See [https://github.com/vlucas/valitron#adding-custom-validation-rules](https://github.com/vlucas/valitron#adding-custom-validation-rules) for more detailed instructions from the original library

4. Edit the field and enter **my_custom_rule** in **Server Validation Rules**. When a registrant submits the form, Events Booking runs my_custom_rule to validate the value.

## Custom error message
When data for a field is not valid, the system will show an error message to registrants so that they will know about the error and correct it. Yoi should set up a clear error message for the field in **Validation error message** setting like [FIELD_NAME] must be a string with maximum 20 characters..., [FIELD_NAME] must be an integer number between 10 and 20....