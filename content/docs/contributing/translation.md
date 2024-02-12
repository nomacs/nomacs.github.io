+++
title = "How to Translate Nomacs"
description = "How to Translate Nomacs"
date = 2024-02-08T17:47:46Z
updated = 2024-02-08T17:47:46Z
draft = false
weight = 420
sort_by = "weight"
template = "docs/page.html"

[extra]
lead = ""
toc = true
top = false
+++

nomacs uses crowdin.net as tool for translations.

After choosing a language press “Translate” to get to the translation interface
(if your language is not available, please send us a message).
It is obligatory to register at crowdin.net.
Your translation will be submitted immediately and will become available to all users
at the next day using the menu ?->”Update translations”.
First translate “nmc::DkGlobalSettingsWidget” -> “English” to the name of your language
e.g. for german “English” is translated to “Deutsch”.
This string will be displayed in the preferences when choosing the languages.

Sometime the suggestions of crowdin are fine, but often you have to change them.
You can filter for untranslated strings, or machine translated string.
Different characters are used within the strings:

- “&”: The ampersand is used as mnemonic in the menu.
       This means it is the shortcut when pressing the alt-modified.
       For example: The “File” menu is translated as “&File”,
       this means the “F” is underlined in the menu and ALT+F can be used as shortcut to access this menu.
- “%1”: This string is always replaced with strings which are needed for a meaningful message.
        In most of the cases these strings are either image names or directories
        e.g. “Could not save: %1″, here %1 will be replaced with the image name.
        Note: due to some reasons we also have to use %1 for the “°” sign like for rotating the image: “9&0%1 Clockwise”

If the string or its context is unclear,
you can use the comment field in the web interface for questions and we will try to answer them as fast as possible.

## How to apply  a new Translation on your machine

1. download the language file from crowdin
1. install Qt Creator (pick the open source installer)
1. open a command line and cd to the directory with the downloaded translations (*.ts)
1. Then type (assuming you downloaded the Catalan translation):

    - Windows (change the Qt folder accordingly)

        ```powershell
        C:\Qt\Qt5.13.0-x64\bin\lrelease.exe nomacs_ca_ES.ts
        ```

    - Linux

        ```shell
        lrelease nomacs_ca_ES.ts
        ```

Now you should have a file named `nomacs_ca_ES.qm` in the same directory.
Copy this file to the translations folder of nomacs (on windows: `C:/Program Files/nomacs/bin/translations`).
