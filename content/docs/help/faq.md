+++
title = "FAQ"
description = "Answers to frequently asked questions."
date = 2021-05-01T19:30:00+00:00
updated = 2021-05-01T19:30:00+00:00
draft = false
weight = 30
sort_by = "weight"
template = "docs/page.html"

[extra]
lead = "Answers to frequently asked questions."
toc = true
top = false
+++

## What does nomacs mean?

First, when we started with the RAW support,
the MacBeth color charts mostly did not have the colors expected when we loaded the images in nomacs.
Second, we solely supported Windows and Ubuntu in the beginning.
At this point we want to thank all the supporters who translate nomacs or build it on other OS.

## Is it possible to put the thumbnails vertically at the left edge of the screen?

Yes, you can right click on the thumbnails panel and then choose e.g. ‘Show Left’.
You can even undock the thumbnails if you do not like the nice overlay effect.

## Is it possible to stop movies such as GIF or MNG?

Yes, you can hit pause in the toolbar player or by selecting View > Stop Movie.
If you then save the image, the currently displayed frame will be written.

## What is the synchronization all about?

We are involved in image processing.
Hence, we often need to compare the same image after different processing stages.
So we wanted something that does this job faster and easier than Photoshop.
That was the initial motivation behind nomacs.

## How can I support nomacs?

Your support is always appreciated. You can either support us by:

- translating nomacs to your language
- porting nomacs to a system not yet supported (it should compile on every system that is supported by Qt)
- coding (bug fixes & additional features are always welcome)

Please see the [How to Contribute](/docs/contributing/how-to-contribute) page.

## How to translate nomacs?

Check out our short introduction on [how to translate nomacs](/docs/contributing/translation) into your language.

## Does nomacs support Windows XP and/or Vista?

The answer is yes and no.
So neither Windows XP nor Vista are supported in future developments since nomacs 3.0.
However, nomacs 2.4.6 is a pretty stable version which you can use on these operating systems.

## How to make an unattended installation of nomacs?

When using Windows you can make an unattended installation of nomacs:

```powershell
nomacs-setup-x64.msi /passive
```
