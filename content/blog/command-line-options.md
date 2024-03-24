+++
title = "Command Line Options"
date = 2015-12-17T17:56:06+01:00
updated = 2015-12-17T17:56:06+01:00
draft = false
template = "blog/page.html"

[taxonomies]
authors = ["Markus Diem"]
+++


we have improved/added command line options for nomacs:

```
Usage: nomacs.exe [options] image

Options:

-?, -h, –help                                   Displays this help.
-v, –version                                    Displays version information.
-f, –fullscreen                                 Start in fullscreen.
-p, –private                                    Start in private mode.
-m, –mode <default | frameless | pseudocolor>   Set the viewing mode <mode>.
-d, –directory <directory>                      Load all files of a <directory>.
-t, –tab <images>                               Load <images> to tabs.
–batch <batch-settings-path>                    Batch processing of <batch-settings.pnm>.
–batch-log <log-path.txt>                       Saves batch log to <log-path.txt>.
–import-settings <settings-path.nfo>            Imports the settings from <settings-path.nfo> and saves them.

Arguments:
image                                           An input image.
```
