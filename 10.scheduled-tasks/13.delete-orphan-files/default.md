---
title: 'Delete Orphan Files'
published: true
media_order: delete_orphan_files.png
---

If your registration form uses a **File** custom field, users can upload a file without completing registration. This task deletes those unused uploads to free up server space.

## Create and configure the scheduled task

1. Go to **System -> Plugins** and make sure the **Task - Events Booking** plugin is enabled.
2. Go to **System -> Scheduled Tasks**, click **New** in the toolbar to create a new scheduled task for **Events Booking - Delete Orphan Files** task type.
3. Set the required parameters and save the task.


## Task Basic Fields
Running this task every few days should be enough. Use the following values under **Basic Fields**.

- **Execution Rule**: Set to **Interval, Days**
- **Interval in Days**: Set to the number you want, for example, if you set it to 1, the task will be run every 1 days. 
- **Execution Time (UTC)**: Choose the time of day to run the task, such as 10:00 AM.
- **Hours to delete orphan files after**: Enter number of hours here. By default, the system keeps these orphan files for 72 hours, mean 3 days. You can lower the number if required, but should keep it for at least 24 hours, just in case something happens with payment process, the file still be kept