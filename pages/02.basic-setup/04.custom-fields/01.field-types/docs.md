---
title: 'Supported Field Types'
taxonomy:
    category:
        - docs
---

**Events Booking** supports the following custom field types.
1. **Text**  
2. **Url**
3. **Email**
4. **Number**
5. **Tel**
6. **Textarea**
7. **List**: Displays a dropdown. It allows one selection by default. To allow multiple selections, set **Multiple** to **Yes**.
8. **Chekboxes**
9. **Radio**
10. **Date**: Display a date picker allows selecting a date
11. **Time**
12. **Datetime**
13. **Heading**: Display **title of the field** as a header on registration form
14. **Message**: Displays a message on the registration form. Enter the message in the field’s **Description**.
15. **File** : Allow registrants to upload file while registering for your events. The file types which registrants can upload is controlled in **Attachment File Types** config option.
16. **Countries**: Displays the published countries in a single-select dropdown.
17. **State**: Displays the states in the selected country. The list updates when the registrant selects a different country.
18. **SQL**: Displays a dropdown populated by a SQL query. The query must meet the following requirements.
* The SQL command needs to be entered into **Default Values** property of the field
* The SQL command needs to return two columns : **value** and **text**
* Sample SQL command which you can use: **SELECT name AS value, name AS text FROM #__eb_countries WHERE published = 1 ORDER BY name** 
19. **Range**
20. **Hidden**
21. **Password**

>>>>> The form supports one country field and one state field. The list of states updates when the registrant changes the country.





>>>>> If the form has a state field without a country field, the state list comes from the Default Country in Events Booking configuration.
