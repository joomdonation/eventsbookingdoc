---
title: 'Synchronize Profile Data'
taxonomy:
    category:
        - docs
---

**Events Booking** has plugins to allow you to synscronize registrant's data which is stored in Events Booking with **Joomla User Profile** and third party extensions. Right now, the folllowing third party extensions are supported: **Membership Pro**, **Community Builder**, **Jomsocial**, **Jomsocial**, **EasyProfile**.

1. When users register for an event in **Events Booking**, if he has an existing account, the data stored in his profile (**Joomla User Profile or third party extensions profile**), the data from his profile will be used to fill-in registration form automatically so that he won't have to type the information again.
2. When users register for an event in **Events Booking**, if he doesn't have an existing account (**Joomla account or third party extensions account**), Events Booking will create a Joomla account for him and update the profile (**Joomla User Profile or third party extensions profile**) with the data which registrant entered on registration form of the event.

## Joomla User Profile 
To synchronize data with **Joomla User Profile**, please follow the steps below:
1. Go to **System** -> **Plugins**, find and enable the plugin **Events Booking - Userprofile**
2. Go to **Events Booking -> Custom Fields**, click on the custom field you want to synchronize data to edit, look at **Field Mappping** parameter, select the corresponding field in **Joomla User Profile** which will be synchronized with this field. Save it.
3. Repeat step #2 for all other fields you want

## Membership Pro 
To synchronize data with **Membership Pro**, please follow the steps below:
1. Go to **System** -> **Plugins**, find and enable the plugin **Events Booking - Membership Pro**
2. Go to **Events Booking -> Custom Fields**, click on the custom field you want to synchronize data to edit, look at **Field Mappping** property, select the corresponding field in **Membership Pro** which will be synchronized with this field. Save it.
3. Repeat step #2 for all other fields you want

## Community Builder
This feature only works if you are using [**Community Builder**](http://extensions.joomla.org/extension/community-builder) extension on your site. If you don't use Community Builder extension, please ignore this section.

To synchronize data with **Community Builder**, please follow the steps below:

1. Go to **System** -> **Plugins**, find and publish the plugin **Event Booking - CB plugin**
2. Go to **Events Booking -> Custom Fields**, click on the custom field you want to synchronize data to edit, look at **Field Mapping** property, select the corresponding field in **Community Builder** which will be synchronized with this field. Save it.
3. Repeat step #2 for all other fields you want

## Jomsocial
This feature only works if you are using [**Jomsocial**](http://www.jomsocial.com/) extension on your site. If you don't use Jomsocial extension, please ignore this section.

To synchronize data with **Jomsocial**, please follow the steps below:

1. Go to **System** -> **Plugins**, find and publish the plugin **Events Booking - Joomsocial**
2. Go to **Events Booking -> Custom Fields**, click on the custom field you want to synchronize data to edit, look at **Field Mapping** property, select the corresponding field in **Jomsocial** which will be synchronized with this field. Save it.
3. Repeat step #2 for all other fields you want

## EasySocial
This feature only works if you are using [**EasySocial**](http://stackideas.com/easysocial/) extension on your site. If you don't use EasySocial extension, please ignore this section.

To synchronize data with **EasySocial**, please follow the steps below:

1. Go to **System** -> **Plugins**, find and enable plugin **Events Booking - Easysocial**
2. Go to **Events Booking -> Custom Fields**, click on the custom field you want to synchronize data to edit, look at **Field Mapping** property, select the corresponding field in **EasySocial** which will be synchronized with this field. Save it.
3. Repeat step #2 for all other fields you want

## EasyProfile
This feature only works if you are using [**EasyProfile**](https://www.easy-profile.com/) extension on your site. If you don't use EasyProfile extension, please ignore this section.

To synchronize data with **EasyProfile**, please follow the steps below:

1. Go to **System** -> **Plugins**, find and publish the plugin **Events Booking - Easy Profile**
2. Go to **Events Booking -> Custom Fields**, click on the custom field you want to synchronize data to edit, look at **Field Mapping** property, select the corresponding field in **EasyProfile** which will be synchronized with this field. Save it.
3. Repeat step #2 for all other fields you want

## Contact Enhanced
This feature only works if you are using [**Contact Enhanced**](https://idealextensions.com/joomla-extensions/component-contact-enhanced.html/) extension on your site. If you don't use **Contact Enhanced** extension, please ignore this section.

To synchronize data with **Contact Enhanced**, please follow the steps below:

1. Go to **System** -> **Plugins**, find and publish the plugin **Events Booking - Contact Enhanced**
2. Go to **Events Booking -> Custom Fields**, click on the custom field you want to synchronize data to edit, look at **Field Mapping** property, select the corresponding field in **Contact Enhanced** which will be synchronized with this field. Save it.
3. Repeat step #2 for all other fields you want

>>>>> Please note that the integration between Events Booking and **Membership Pro, EasySocial, Contact Enhanced** is one way only. When users register for an event in Events Booking and has profile data in the three above extensions, that profile data will be used to fill-in registration form automatically so that users won't have to type it again. However, if users don't have account in the above extensions and register for an event in Events Booking, Events Booking will only create a Joomla account for the user, not updating his profile data in the above extensions yet. This might be changed in the future but not possible for now
