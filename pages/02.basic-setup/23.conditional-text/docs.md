---
title: 'Conditional Text'
published: true
---

Sometime, you would want to show certain information (in emails, thank you messages, invoice...) in certain condition. For that, you can use the supported conditional text feature in Events Booking. The syntax is:

{ebShowText [TAG][OPERATOR][VALUE_TO_COMPARE]}This text will be shown if the condition return true.{/ebShowText}

- [TAG] is any tag which can be used in email messages or invoice. For example [FIRST_NAME], [LAST_NAME], [PAYMENT_METHOD_NAME].....
- [OPERATOR] is one of the supported operator: **=** (equals), **>** (greater), **<** (smaller), **~** (different) .
- [VALUE_TO_COMPARE] is the value which you want to compare with the value returned by the tag [TAG] which you are using.


Few example:

1. {ebShowText [PAYMENT_METHOD_NAME]=os_offline}This text will be shown if the payment method is os_offline {/ebShowText}
2. {ebShowText [PAYMENT_METHOD_NAME]~os_offline}This text will be shown if users use any payment methods except os_offline {/ebShowText}
3. {ebShowText [FIRST_NAME]=Tuan}This text will be shown if first name of the Registrant is Tuan {/ebShowText}
4. {ebShowText [PUBLISHED]=0}This text will be shown registration status is Pending {/ebShowText}
5. {ebShowText [PUBLISHED]=1}This text will be shown registration status is Paid {/ebShowText}
6. {ebShowText [PUBLISHED]=2}This text will be shown registration status is Cancelled {/ebShowText}
7. {ebShowText [NAME_OF_FIELD]=Yes}This text will be shown the value of custom field **name_of_field** has value **Yes**{/ebShowText}


Of if you want to have text on multi-lines:

{ebShowText [FIRST_NAME]=Tuan}
This text will be shown if data entered into first_name field is Tuan
{/ebShowText}
{ebShowText [PUBLISHED]=0}
This text will be shown if published = 0, mean registration is Pending
{/ebShowText}
{ebShowText [PUBLISHED]=1}
This text will be shown if published = 1, mean registration status is Paid
{/ebShowText}