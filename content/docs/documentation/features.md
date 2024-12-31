+++
title = "Features"
description = "Features"
date = 2024-12-20T19:01:00Z
updated = 2024-12-20T19:01:00Z
draft = false
weight = 420
sort_by = "weight"
template = "docs/page.html"

[extra]
lead = ""
toc = true
top = false
+++

## Image formats

Updated 2024-12-20.

| Provider                   | Read and write                                               | Read only                                                                         |
|----------------------------|--------------------------------------------------------------|-----------------------------------------------------------------------------------|
| Qt Built-in                | BMP, JPG, JPEG, PNG, PPM, XBM, XPM                           | GIF, PBM PGM                                                                      |
| Compile with `ENABLE_RAW`  |                                                              | The formats that LibRaw supports (e.g. cr2, crw, nef, arw, mrw, rw2)              |
| Compile with `ENABLE_TIFF` | TIFF (multi-page)                                            |                                                                                   |
| Compile with Qt SVG        | SVG                                                          |                                                                                   |
| Qt Image formats plugin    | ICNS, JP2, TIFF, WBMP, WEBP                                  | MNG, TGA                                                                          |
| KImageFormats plugin       | AVIF, DDS, EPS, HEIF, JXL, JXR, EXR, PCX, QOI, SGI, PIC, TGA | ANI, RAW, XCF, KRA, ORA, PXR, PFM, PHM, Photoshop documents, HDR, SCT, Sun Raster |
