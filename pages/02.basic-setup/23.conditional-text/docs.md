---
title: 'Conditional Text'
published: true
---

Use conditional text to display information in an email, thank-you message, or invoice only when a condition is met. Use the following syntax.

{ebShowText [TAG][OPERATOR][VALUE_TO_COMPARE]}This text will be shown if the condition return true.{/ebShowText}

- [TAG] is any tag you can use in an email or invoice, such as [FIRST_NAME], [LAST_NAME], or [PAYMENT_METHOD_NAME].
- [OPERATOR] is one of the supported operators: **=** (equals), **>** (greater than), **<** (less than), or **~** (does not equal).
- [VALUE_TO_COMPARE] is the value to compare with the value returned by [TAG].


The following examples show how to use the operators.

1. {ebShowText [PAYMENT_METHOD_NAME]=os_offline}This text will be shown if the payment method is os_offline {/ebShowText}
2. {ebShowText [PAYMENT_METHOD_NAME]~os_offline}This text will be shown if users use any payment methods except os_offline {/ebShowText}
3. {ebShowText [FIRST_NAME]=Tuan}This text will be shown if first name of the Registrant is Tuan {/ebShowText}
4. {ebShowText [PUBLISHED]=0}This text will be shown registration status is Pending {/ebShowText}
5. {ebShowText [PUBLISHED]=1}This text will be shown registration status is Paid {/ebShowText}
6. {ebShowText [PUBLISHED]=2}This text will be shown registration status is Cancelled {/ebShowText}
7. {ebShowText [NAME_OF_FIELD]=Yes}This text will be shown the value of custom field **name_of_field** has value **Yes**{/ebShowText}


You can also display text on multiple lines.

{ebShowText [FIRST_NAME]=Tuan}
This text will be shown if data entered into first_name field is Tuan
{/ebShowText}
{ebShowText [PUBLISHED]=0}
This text will be shown if published = 0, mean registration is Pending
{/ebShowText}
{ebShowText [PUBLISHED]=1}
This text will be shown if published = 1, mean registration status is Paid
{/ebShowText}