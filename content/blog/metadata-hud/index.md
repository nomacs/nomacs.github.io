+++
title = "Metadata HUD"
date = 2015-04-15T13:19:51+02:00
updated = 2015-04-15T13:19:51+02:00
draft = false
template = "blog/page.html"

[taxonomies]
authors = ["Markus Diem"]
+++

We have upgraded the Metadata HUD panel. At a first glance it looks pretty much as in previous versions.
<img alt="Metadata HUD" src="metadata-0000.png" width="100%"/>

If you right click the panel, there will be a few new options:
<img alt="Metadata Panel - Context Menu" src="metadata-0001.png" width="100%"/>

Similar to the Thumbnail preview, you can choose where to display the panel.
If the panel is in Horizontal Layout (Top or Bottom) you can choose the number of columns.
If the data does not fit to the current window size, a scroll bar will appear.

But the most important improvement is the key selection.
Up to now you were only able to select pre-defined exif keys.
Since exif values are pretty dynamic, you can now choose an image which has special entries.
If you click Change Entries, this dialog will appear:
<img alt="key selection" src="metadata-0002.png" width="100%"/>

The dialog lists all exif entries of the currently loaded image.
Checking an entry there will add the entry to the metadata HUD.
