+++
title = "Adding new file formats"
date = 2014-10-01T09:15:02+02:00
updated = 2014-10-01T09:15:02+02:00
draft = false
template = "blog/page.html"

[taxonomies]
authors = ["Stefan Fiel"]
+++

Since the last release we are getting more and more requests if we can support different file formats.
Apparently it turned out, that we already support most of them but we have not added the file extension to our file filter.
This is especially true for RAW formats of image files,
we just simple don’t know all extensions of all manufacturers and we don’t have sample images from all of them for testing.

But there is a simple solution: you can easily try to add new files formats to nomacs.
You just have to use File -> Add Image Format
– this opens a dialog where you can drop (or load) your images and nomacs will tell you if the file extension is supported.
If it is supported it will display the image.
After adding the file format you can use our File Filter settings in the preferences dialog
to set nomacs as default viewer for these images.
If you have successfully added a new file format,
please drop us a note in our bug tracker and we will add the extension to nomacs.
If nomacs is unable to load you file format, please add a new feature request.
If possible attach also the image to the request so we can test it easily.

Open the “Add Image Format” Dialog

<img alt="Open the “Add Image Format” Dialog" src="add-file-format.png" width="100%"/>

and drop or load your image

<img alt="and drop or load your image" src="add-file-format2.png" width="100%"/>

— the nomacs team
