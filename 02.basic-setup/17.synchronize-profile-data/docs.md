---
title: 'Synchronize Profile Data'
taxonomy:
    category:
        - docs
---

**Events Booking** has plugins to allow you to synscronize registrant's data which is stored in Events Booking with **Joomla User Profile** and third party extensions. Right now, the folllowing third party extensions are supported: **Membership Pro**, **Community Builder**, **Jomsocial**, **Jomsocial**, **EasyProfile**.

1. When a user with an existing account registers, Events Booking fills in the registration form with data from their Joomla User Profile or third-party profile.
2. When users register for an event in **Events Booking**, if he doesn't have an existing account (**Joomla account or third party extensions account**), Events Booking will create a Joomla account for him and update the profile (**Joomla User Profile or third party extensions profile**) with the data which registrant entered on registration form of the event.

## Joomla User Profile 
To synchronize data with **Joomla User Profile**, please follow the steps below:
1. Go to **System** -> **Plugins**, find and enable the plugin **Events Booking - Userprofile**
2. Go to **Events Booking -> Custom Fields** and edit the field you want to synchronize. Under **Field Mappping**, select the matching field in **Joomla User Profile** and save.
3. Repeat step #2 for all other fields you want

## Membership Pro 
To synchronize data with **Membership Pro**, please follow the steps below:
1. Go to **System** -> **Plugins**, find and enable the plugin **Events Booking - Membership Pro**
2. Go to **Events Booking -> Custom Fields** and edit the field you want to synchronize. Under **Field Mappping**, select the matching field in **Membership Pro** and save.
3. Repeat step #2 for all other fields you want

## Community Builder
This feature only works if you are using [**Community Builder**](http://extensions.joomla.org/extension/community-builder) extension on your site. If you don't use Community Builder extension, please ignore this section.

To synchronize data with **Community Builder**, please follow the steps below:

1. Go to **System** -> **Plugins**, find and publish the plugin **Event Booking - CB plugin**
2. Go to **Events Booking -> Custom Fields** and edit the field you want to synchronize. Under **Field Mapping**, select the matching field in **Community Builder** and save.
3. Repeat step #2 for all other fields you want

## Jomsocial
This feature only works if you are using [**Jomsocial**](http://www.jomsocial.com/) extension on your site. If you don't use Jomsocial extension, please ignore this section.

To synchronize data with **Jomsocial**, please follow the steps below:

1. Go to **System** -> **Plugins**, find and publish the plugin **Events Booking - Joomsocial**
2. Go to **Events Booking -> Custom Fields** and edit the field you want to synchronize. Under **Field Mapping**, select the matching field in **Jomsocial** and save.
3. Repeat step #2 for all other fields you want

## EasySocial
This feature only works if you are using [**EasySocial**](http://stackideas.com/easysocial/) extension on your site. If you don't use EasySocial extension, please ignore this section.

To synchronize data with **EasySocial**, please follow the steps below:

1. Go to **System** -> **Plugins**, find and enable plugin **Events Booking - Easysocial**
2. Go to **Events Booking -> Custom Fields** and edit the field you want to synchronize. Under **Field Mapping**, select the matching field in **EasySocial** and save.
3. Repeat step #2 for all other fields you want

## EasyProfile
This feature only works if you are using [**EasyProfile**](https://www.easy-profile.com/) extension on your site. If you don't use EasyProfile extension, please ignore this section.

To synchronize data with **EasyProfile**, please follow the steps below:

1. Go to **System** -> **Plugins**, find and publish the plugin **Events Booking - Easy Profile**
2. Go to **Events Booking -> Custom Fields** and edit the field you want to synchronize. Under **Field Mapping**, select the matching field in **EasyProfile** and save.
3. Repeat step #2 for all other fields you want

## Contact Enhanced
This feature only works if you are using [**Contact Enhanced**](https://idealextensions.com/joomla-extensions/component-contact-enhanced.html/) extension on your site. If you don't use **Contact Enhanced** extension, please ignore this section.

To synchronize data with **Contact Enhanced**, please follow the steps below:

1. Go to **System** -> **Plugins**, find and publish the plugin **Events Booking - Contact Enhanced**
2. Go to **Events Booking -> Custom Fields** and edit the field you want to synchronize. Under **Field Mapping**, select the matching field in **Contact Enhanced** and save.
3. Repeat step #2 for all other fields you want

>>>>> The integrations with **Membership Pro, EasySocial, Contact Enhanced** work in one direction. If a registrant has a profile in one of these extensions, Events Booking uses that data to fill in the registration form. If the registrant has no account in the extension, Events Booking creates a Joomla account and leaves the third-party profile data as is. This may change in a future version.
