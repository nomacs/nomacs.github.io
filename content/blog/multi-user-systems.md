+++
title = "Multi User Systems"
date = 2018-07-09T16:41:04+02:00
updated = 2018-07-09T16:41:04+02:00
draft = false
template = "blog/page.html"

[taxonomies]
authors = ["Markus Diem"]
+++

in nomacs 3.10.2 we have added a better multi user support because of your feedback.

Basically you can now create default settings that are applied to all user settings after the first start-up.
Therefore, you have to export your desired defaults by `Edit > Settings > General > Export Settings` and name them `default.ini`.
If you now replace the default.ini in the nomacs install directory,
these settings will be applied if a new user starts nomacs for the first time.

– the nomacs team

HINT: the check for updates option is an issue for some large companies. Creating a default.ini with this content:

```ini
[SynchronizeSettings]
checkForUpdates=false
disableUpdateInteraction=true
```

will disable checking for updates. Additionally, users won’t be able to manually check for updates anymore.
