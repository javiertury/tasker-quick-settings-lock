# Tasker Disable Quick Settings on Lockscreen
Disable quick settings on your lockscreen. Compatible with Cyanogenmod and Lineage OS 14-16. This repository contains tasks and profiles for [Tasker](http://tasker.dinglisch.net/), an app to automatize tasks. Requires root.

# Installation
The folder `quick-settings-lock` in this repo contains 2 folders, `profiles` and `tasks`. Copy those 2 folders to your phone under the directory `/sdcard/Tasker`. If the directory doesn't exist, create it. Make sure that your device is rooted.
  1. Open tasker. Touch and hold the tab `TASKS`. A menu will pop up.
  2. Select `import`.
  3. Browse `/sdcard/Tasker/tasks` and open it.
  4. Import each task one by one
  5. Touch and hold the tab `PROFILES`. A menu will pop up.
  6. Select `import`.
  7. Browse `/sdcard/Tasker/profiles` and open it.
  8. Import each profile one by one
  9. Enable the imported profiles.

# Description

These tasks and profiles hide quick settings from your lockscreen. Actually, many people think that Android should do this by default. This has been reported as [issue 37010638](https://issuetracker.google.com/issues/37010638), but Google doesn't pay attention to this issue.

There are 2 main advantages over other existing tasker configurations. These tasks restore your last quick settings tiles, not some fixed preset. Also the task `Quick Settings Disable` is idempotent. That is, even if `Quick Settings Disable` is run many consecutive times, it will still remember your original tiles, and the next `Quick Settings Enable` will restore them. Simple and reliable.
