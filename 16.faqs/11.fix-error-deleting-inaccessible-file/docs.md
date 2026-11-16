---
title: 'Fix Error Deleting Inaccessible File'
---

You may see the following error when updating Events Booking.

> Joomla\Filesystem\File::delete: Failed deleting inaccessible file autoload.php

The error is related to Joomla 3.9.0 API changes. See [https://github.com/joomla/joomla-cms/issues/23504](https://github.com/joomla/joomla-cms/issues/23504) for details.

To apply the workaround, follow these steps.

1. Open the file libraries/vendor/joomla/filesystem/src/File.php

2. Find this line of code:

```php
if (!Path::canChmod($file))
```

Change it to:

```php
if (!Path::canChmod($file) && false)
```
Run the update again.