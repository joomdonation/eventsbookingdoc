---
title: 'Develop Events Booking plugin'
taxonomy:
    category:
        - docs
---

You can write plugins to extend **Events Booking**. The bundled plugins are in **plugins/eventbooking** on your site.

**Events Booking** triggers the following events. Your plugin can listen for them to add behavior to the extension.

## onEditEvent

This event is triggered on add/edit event form. It usually used to allows you to display a form to allow admin control the necessary settings for your event. A sample is the Joomla Groups plugin which allows admin to select which user groups registrants of the event will be added to when he registers and pay for the event.

```php
public function onEditEvent($row)
{
}
```
- **$row**: The table object (instance of **EventbookingTableEvent** class) stores information of event being adding/editing.

## onAfterSaveEvent

This event is triggered after the event is saved to database. It is usually used to save the settings data which you displayed on event add/edit screen so that you can used that settings data later

```php
public function onAfterSaveEvent($row, $data, $isNew)
{
	
}
```

- **$row**: The table object (instance of **EventbookingTableEvent** class) stores information of event being saved.
- **$data**: Array contains all post data from add/edit event form.
- **$isNew**: True if new event is added, false if existing event is being updated.

## onAfterStoreRegistrant

This event is triggered after the registration record record is saved to database (before payment is processed)

```php
public function onAfterStoreRegistrant($row)
{
	
}
```

- **$row**: The table object (instance of **EventbookingTableEvent** class) stores information of stored registration record. From $row object, you can access to any fields from **eb_registrants** table:

+ $row->id : ID of registration record
+ $row->event_id: ID registered event
+ $row->user_id : ID of user who registered for event
+ $row->first_name: First Name of registrant
+ $row->last_name: Last Name of registrant
+ $row->email: Email of registrant
+ $row->payment_method: The payment method registrant uses to make payment
+ $row->transaction_id: Transaction ID of payment for the registration.

$row object only allows you to access to data of core fields like first_name, last_name, email, address... If you want to get data from certain none core fields, you can use the following code:

```php
$data = EventbookingHelperRegistration::getRegistrantData($row);

echo $data['name_of_field']; // Will return value for a custom field with name = **name_of_field**
```

## onAfterPaymentSuccess
This event is triggered when status of the registration record changed from Pending to Paid (after payment is completed or admin change status of registration record from Pending to Paid in case registrant using offline payment method for the registration)

```php
public function onAfterPaymentSuccess($row)
{
	
}
```

- **$row**: The table object (instance of **EventbookingTableEvent** class) stores information of the registration record. From $row object, you can access to any fields from **eb_registrants** table. You can see explanation from **onAfterStoreRegistrant**  above to see how to access to the necessary information from your plugin.

## onEventDisplay

This event is triggered on frontend event detail page. You can write a plugin to handle this event to display more information of the event on event details page if needed. Look at **jcomments** plugin in the package to see how this event can be used.

```php
public function onEventDisplay($row)
{
	
}
```

- **$row** is an object stores information of event being displayed. From this object, you can access to any event information such as ID, Title, Event Date, Event End Date....

+ $row->id : ID of event
+ $row->title: Title of the event
+ $row->main_category_id: ID of main category of event
+ $row->event_date : Event Date
+ $row->event_end_date: Event End Date
+ $row->location_id: ID of the location of event.


## onEditField

This event is triggered on add/edit custom field form. It usually used to allows you to display a form to allow admin control the necessary settings for your custom field.

```php
public function onEditField($row)
{
}
```
- **$row**: The table object (instance of **EventbookingTableField** class) stores information of custom field being adding/editing.

## onAfterSaveField

This event is triggered after the custom field is saved to database. It is usually used to save the settings data which you display on custom field add/edit screen so that you can used that settings data later

```php
public function onAfterSaveField($row, $data, $isNew)
{
	
}
```

- **$row**: The table object (instance of **EventbookingTableField** class) stores information of custom field being saved.
- **$data**: Array contains all post data from add/edit custom field form.
- **$isNew**: True if new field is added, false if existing field is being updated.

## Use to Events Booking Code From Outside

Sometimes, you might want to use Events Booking code from outside the component, for example, from module or plugin. For that, the first thing you need to do is add this line of code to make sure all classes in Events Booking is autoload-able:

```php
// Require library + register autoloader
require_once JPATH_ADMINISTRATOR . '/components/com_eventbooking/libraries/rad/bootstrap.php';
```

#### To use public methods from a model class, you can use code like this:

```php
// Register the class with Joomla auto loader
JLoader::register('EventbookingModelUpcomingevents', JPATH_ROOT . '/components/com_eventbooking/model/components/com_eventbooking/model/upcomingevents.php');

/* @var EventbookingModelUpcomingevents $model */
$model = RADModel::getTempInstance('Upcomingevents', 'EventbookingModel', ['table_prefix' => '#__eb_']);

$model->setState('id', 1);
$rows = $model->getData();
```

#### To get all data for a registration record (both core fields and none core fields)

```php
$data = EventbookingHelperRegistration::getRegistrantData($row);

echo $data['first_name'];
echo $data['last_name'];
echo $data['name_of_field'];

```

#### Useful static methods:

```php
$config = EventbookingHelper::getConfig(); // Return $config object which allows accessing to any config variables

$message = EventbookingHelper::getMessages(); // Return $message object which allows accessing to any message items.
```