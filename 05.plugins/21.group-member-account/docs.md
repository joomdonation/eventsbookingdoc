---
title: 'Group Member Account'
published: true
---

If **User Registration Integration** is enabled, a group registration creates an account for the person completing the billing information. Enable **Events Booking - Group Member Account** to create a separate user account for each group member.

### Requirement

This plugin creates accounts only for Group Registration. Member information collected through the shopping cart or ticket types does not create user accounts.

### Configuration
In Joomla, to create user account, we need to have following information :

1. **Username**

- You can create a custom field called **username** set **Display In** parameter to **Group Member Form** to allow entering username for each group member. If you do not create that field, the system will use **email** of the user as the account

2. **Name**

You should have at least first_name field (or both first_name and last_name fields) collected for each group member. That data will be used to populate name of the user account.

3. **Email**

Make sure email field is collected for each group member. Without email, there will be no user account created

**4. Password**

This is controlled by **Password Data** parameter in the plugin.

- If you want, you can create a field called password to allow entering password for each group member. The **Display In** setting of the field, if created, should be set to **Group Member Form** (same as the username field). In this case, set **Password Data** parameter to **Manually**
- If you don't want to enter password for each group member, set **Password Data** to one of the following values: **Random** (the system will generate random password for the account), **Username** (the system will use username as the password for the account), **Email** (the system will use email as the password for the account)

### Username is already exist

If there is an existing user account with the username or email, the system won't create a new user account. It will assign the group member record to that existing account instead

