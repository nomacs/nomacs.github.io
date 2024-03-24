+++
title = "Release Candidate 0.4"
date = 2012-07-25T13:04:21+02:00
updated = 2012-07-25T13:04:21+02:00
draft = false
template = "blog/page.html"

[taxonomies]
authors = ["Markus Diem"]
+++

after one year of development, nomacs has become something that we call stable.
so we released nomacs 0.4.0 Release Candidate today.
For now it’s just windows – nomacs will be released in the next few days for all Operating Systems supported.

new features include:

- Caching images – results in very short loading time
- Thumb run-through – fast folder preview
- Save widget state – widgets remember if they were displayed the last time
- Additional supported formats – \*.mrw (Minolta Raw) and \*.rw2 (Panasonic Raw)
- Improved  RAW display – colors are now more intensive
- Go To – you can jump to whatever file you like using the new Go To dialog (CTRL+G)
- Unattended installation parameters – improves batch installation for Windows

and as usual we have fixed some bugs:

- RAW images for Linux – nomacs did not load raw images with libraw > 0.14.0
- Save dialog – is now a native OS dialog -> speed up
- \*.bmp save – error message removed
- Transparency & edit – handling of transparent images (e.g. crop) is corrected
- … and a bunch of small fixes

Please note that the cacher is deactivated by default.
We did so to save RAM for those who use nomacs in order to display every-day-images.
Give it a try by changing the preferences: Settings > Resources > Cache Settings

— the nomacs team
