+++
title = "ubuntu launchpad repository"
date = 2012-01-30T15:16:10+01:00
updated = 2012-01-30T15:16:10+01:00
draft = false
template = "blog/page.html"

[taxonomies]
authors = ["Stefan Fiel"]
+++

we have create launchpad repositories for Ubuntu.
This will make it easier to install nomacs for Ubuntu and to keep it up-to-date.
To install nomacs using this repository you have to add “ppa:nomacs/stable” to your list.
You can do this by typing

```sh
sudo add-apt-repository ppa:nomacs/stable
```

in a console.
After updating the repositories you should be able to install nomacs using your favorite package manager

You have also the possibility to install the daily builds of nomacs by adding “ppa:nomacs/daily” but these builds are considered as experimental.

Have fun!

— the nomacs team
