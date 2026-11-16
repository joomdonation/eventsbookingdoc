---
title: 'Code customization (override)'
---

Since version 2.10.2, Events Booking has supported code overrides for static methods and model, view, and controller classes. Overrides let you customize the extension while keeping your changes through updates.

## Override static methods (helper methods)

Events Booking helper classes are in components/com_eventbooking/helper. You can override the following static methods.

1. EventbookingHelper::formatCurrency
2. EventbookingHelper::formatInvoiceNumber
3. EventbookingHelper::downloadCertificates
4. EventbookingHelper::generateInvoicePDF
5. EventbookingHelperData::prepareRegistrantsExportData
6. EventbookingHelperData::excelExport
7. EventbookingHelperCart::addEvents
8. EventbookingHelperCart::updateCart
9. EventbookingHelperData::calculateDiscount
10. EventbookingHelperMail::sendEmails
11. EventbookingHelperMail::sendRegistrationApprovedEmail
12. EventbookingHelperMail::sendRegistrationCancelledEmail
13. EventbookingHelperMail::sendWaitinglistEmail
14. EventbookingHelperMail::sendWaitingListNotificationEmail
15. EventbookingHelperMail::sendDepositPaymentEmail
16. EventbookingHelperMail::sendNewEventNotificationEmail
17. EventbookingHelperMail::sendReminder
18. EventbookingHelperMail::sendSecondReminder
19. EventbookingHelperMail::sendDepositReminder
20. EventbookingHelperMail::sendRequestPaymentEmail
21. EventbookingHelperJquery::validateForm()
22. EventbookingHelperRegistration::buildTags
23. EventbookingHelperRegistration:calculateCartRegistrationFee
24. EventbookingHelperRegistration:calculateRegistrationFees
25. EventbookingHelperRegistration::calculateIndividualRegistrationFees
26. EventbookingHelperRegistration::calculateGroupRegistrationFees
27. EventbookingHelperRegistration::getFormFields
28. EventbookingHelperRegistration::getRegistrationRate
29. EventbookingHelperRegistration::userRegistrationCB
30. EventbookingHelperRegistration::needInvoice
31. EventbookingHelperRegistration::getInvoiceNumber
32. EventbookingHelperRegistration::buildDepositPaymentTags
33. EventbookingHelperRegistration::calculateRemainderFees


To customize a method in one of these classes, please folow the steps below:

1. Create folder **override** under components/com_eventbooking/helper folder 
2. Create a php file (same name with the php file which contains the method you want to override, for example **helper.php**, **mail.php**, **jquery.php**, **data.php**, **registration.php**

3. Add a blank class into that PHP file. The class name must follow this Rule: It has the word **Override** inserted after **EventbookingHelper** compare to the original class name and extends the original class. For example:

```php
/**
 * EventbookingHelperOverrideHelper class
 *
 * This class can be used to override some common methods used in EventbookingHellper class. It is needed when you need to
 * override these methods without having to worry about losing the customization while updating to future releases of Events Booking
 */
class EventbookingHelperOverrideHelper extends EventbookingHelper
{
}


/**
 * EventbookingHelperOverrideMail class
 *
 * This class can be used to override some common methods used in EventbookingHellperMail class. It is needed when you need to
 * override these methods without having to worry about losing the customization while updating to future releases of Events Booking
 */
class EventbookingHelperOverrideMail extends EventbookingHelperMail
{

}


/**
 * EventbookingHelperOverrideJquery class
 *
 * This class can be used to override some common methods used in EventbookingHelperOverrideJquery class. It is needed when you need to
 * override these methods without having to worry about losing the customization while updating to future releases of Events Booking
 */
class EventbookingHelperOverrideJquery extends EventbookingHelperJquery
{
}


/**
 * EventbookingHelperOverrideRegistration class
 *
 * This class can be used to override some common methods used in EventbookingHelperOverrideJquery class. It is needed when you need to
 * override these methods without having to worry about losing the customization while updating to future releases of Events Booking
 */
class EventbookingHelperOverrideRegistration extends EventbookingHelperRegistration
{
}


/**
 * EventbookingHelperOverrideData class
 *
 * This class can be used to override some common methods used in EventbookingHelperOverrideJquery class. It is needed when you need to
 * override these methods without having to worry about losing the customization while updating to future releases of Events Booking
 */
class EventbookingHelperOverrideData extends EventbookingHelperRegistration
{
}

```

4. Copy the original code of the method you want to override into the class you defined above and customize it to suit your needs. Please note that these classes extends the original class, so you can call any (public/protected) methods in the parent class.

Also, if in the code of original method has code to check if method support override like this, you will have to remove it from copied code, otherwise, you will get error

```php
if (EventbookingHelper::isMethodOverridden('EventbookingHelperOverrideMail', 'sendEmails'))
{
	EventbookingHelperOverrideMail::sendEmails($row, $config);

	return;
}
```


You can see the skeleton of the override code for these methods here https://github.com/joomdonation/eventbooking-override-skeleton/tree/master/helper/override

## Override method in a controller class

If you need to override a method inside a controller, please follow the steps below:

1. Create folder **override** under components/com_eventbooking/controller folder (or under  administrator/components/com_eventbooking/controller if you want to override a backend controller)
2. Create a php file (same name with the php file which contains the method you want to override, for example **register.php**, **event.php**, **registrant.php**)
3. Add a blank class into that PHP file. The class name must follow this Rule: It has the word **Override** inserted after **EventbookingController** compare to the original class name and extends the original class. For example:

```php
/**
 * EventbookingControllerOverrideRegister class
 *
 * This class is used to show you how to override a controller class in Events Booking.
 */
class EventbookingControllerOverrideRegister extends EventbookingControllerRegister
{

}
```
4. Copy the original code of the method you want to override into the class you defined above and customize it to suit your needs. Please note that these classes extends the original class, so you can call any (public/protected) methods in the parent class. See https://github.com/joomdonation/eventbooking-override-skeleton/blob/master/controller/override/register.php for sample of controller override

## Override method in a model class

If you need to override a method inside a model, please follow the steps below:

1. Create folder **override** under components/com_eventbooking/model folder (or under  administrator/components/com_eventbooking/model if you want to override a backend model)
2. Create a php file (same name with the php file which contains the method you want to override, for example **register.php**, **list.php**, **categories.php**)
3. Add a blank class into that PHP file. The class name must follow this Rule: It has the word **Override** inserted after **EventBookingModel** compare to the original class name and extends the original class. For example:

```php
/**
 * EventbookingModelOverrideRegister class
 *
 * This class is used to show you how to override a model class in Events Booking.
 */
class EventBookingModelOverrideRegister extends EventBookingModelRegister
{

}
```
4. Copy the original code of the method you want to override into the class you defined above and customize it to suit your needs. Please note that these classes extends the original class, so you can call any (public/protected) methods in the parent class. See https://github.com/joomdonation/eventbooking-override-skeleton/blob/master/model/override/register.php for a sample of override model classs.

## Override method in a view class

If you need to override a method inside a view, please follow the steps below:

1. Create folder **override** under components/com_eventbooking/view folder (or under  administrator/components/com_eventbooking/view if you want to override a backend model)
2. Create a new folder - the name of this folder must be the same with name of the view you want to override, for example **register**, **registrants**, **search**...
3. Create a php file - same name with the php file which contains the method you want to override, usually html.php, put it into the above folder
4. Add a blank class into that PHP file. The class name must follow this Rule: It has the word **Override** inserted after EventbookingView compare to the original class name and extends the original class. For example:

```php
/**
 * Class EventbookingViewOverrideRegisterHtml
 *
 * This class is used to show you how to override a view class in Events Booking.
 */
class EventbookingViewOverrideRegisterHtml extends EventbookingViewRegisterHtml
{
}
```
5. Copy the original code of the method you want to override into the class you defined above and customize it to suit your needs. Please note that these classes extends the original class, so you can call any (public/protected) methods in the parent class. See https://github.com/joomdonation/eventbooking-override-skeleton/blob/master/view/override/register/html.php for sample of override view class
