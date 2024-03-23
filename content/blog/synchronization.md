+++
title = "Synchronization"
date = 2014-11-17T16:33:35+01:00
updated = 2014-11-17T16:33:35+01:00
draft = false
template = "blog/page.html"

[taxonomies]
authors = ["Stefan Fiel"]
+++

With the synchronization it is possible that multiple viewers perform the same action (like panning, zooming, etc.).
This feature is useful when comparing two images.

## Synchronization on the same computer

For synchronization on the same computer at least two instances of nomacs have to run.
Via the “Sync”-Menu it is possible to connect to all viewers
or a specific viewer can be chosen by selecting the image title of this viewer.
Additionally it is possible to connect two viewers by keeping the CTRL and ALT key pressed
and drag from the image of one viewer to the other.
For actions which should be performed on all connected instances the ALT key has to be kept pressed
(e.g. hold the ALT key pressed and use the mouse wheel for zooming on all connected viewers).

Possible actions which can be performed:

- Panning ALT+mouse
- Zooming ALT+mouse
- load next/previous File (ALT+right resp. ALT+left)
- synchronize zoom level and position in the image with CTRL+D
- overlay the two images and change the opacity of one image with CTRL+TAB
- arrange synchronized viewers with CTRL+SHIFT+TAB

## Synchronization in the local network (LAN)

First you have to enable “network sync” in the network preferences of nomacs on all computers you want to use.
To synchronize viewers via the local network one nomacs has to start the server using the menu.
The viewer on the other computer can then connect to the server.
Additional to the actions on the same computer (see above) images can also be sent over the network by pressing ALT+I
(or using the menu:  Sync -> Send Image).

In the settings dialog actions can be forbidden for all clients (see Settings-Network).
So you can forbid a client e.g. to zoom into your image and/or to send you new images.

Note: If a server connects to another server in the network,
all clients of this server disconnect and establish a new connection to the target server.
Also the server of the current viewer is stopped.
