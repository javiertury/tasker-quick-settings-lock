# Tasker Disable Quick Settings on Lockscreen
Automatically disable quick settings if your screen is locked in Cyanogenmod and Lineage OS 14. These tasks and profiles are for the android app [Tasker](http://tasker.dinglisch.net/). Requires root.

# Installation
The folder `quick-setttings-lock` in this repo contains 2 folders, `profiles` and `tasks`. Copy those 2 folders to your android device, preferably to `/sdcard/Tasker`. Make sure that your device is rooted.
  1. Open tasker and then touch and hold on `TASKS` tab until a menu pops up.
  2. Select `import`.
  3. Browse the directory in which you put your `tasks` directory and open it.
  4. Import each profile one by one
  5. Repeat steps 1-5 for the `profiles` directory to the tab `PROFILES`.
  6. Enable the imported profiles.

# Description

These tasks and profiles automatically disable quick settings on the lockscreen and enable it again when the screen is unlocked. Some times when you have your android phone in your pocket and your screen turns on, it messes up you quick settings. For example it turns on/off do not disturb, turns wifi on/off ... which can lead you to miss important notifications or to get noisy notifications when your phone should stay silent. This has been reported as [issue 37010638](https://issuetracker.google.com/issues/37010638), but it's not likely that google fixes it any time soon.

There are 2 differences with other tasker solutions. The first one is that this one keeps the current state of quick settings on a global variable, it is not restored to a fixed configuration. The second one is that the task `Quick Settings Disable` is idempotent. That is, if for whatever reason it is run twice or more without having triggered `Quick Settings Enable` before, the state is not altered. The next `Quick Settings Enable` will still restore you quick settings tiles. Simple and reliable.
