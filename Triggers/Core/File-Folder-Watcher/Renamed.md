---
title: Renamed
description: File/Folder Watcher Triggers Reference
published: true
date: 2023-03-14T21:44:00.489Z
tags: 
editor: markdown
dateCreated: 2023-03-14T21:42:54.378Z
---

## Overview
This triggers when a file gets renamed in the folder you're watching.

For a detailed guide on how the File/Folder Watcher works in Streamer.bot see [this page](/Settings/File-Folder-Watcher).

## Configuration
### Watcher
Select any or a specific watcher from the Settings --> File/Folder Watcher tab

## Variables
Name | Description
----:|:------------
`watcherFolder` | The folder you're watching for changes e.g. `C:\Desktop\Example-Folder`
`watcherFilter` | The filter of this watcher e.g. `*.*`
`oldFullPath` | The previous full path e.g. `C:\Desktop\Example-Folder\Example.txt`
`oldFilename` | The previous full file name e.g. `Example.txt`
`fullPath` | The full path of the file e.g. `C:\Desktop\Example-Folder\Example-2.txt`
`fileName` | The full file name including the file extension e.g. `Example-2.txt`
`changeType` | The change type e.g. `Renamed`
{.vars-table}

---

- [<i class="mdi mdi-chevron-left"></i>**File/Folder Watcher Triggers Reference *Go Back***](/Triggers/Core/File-Folder-Watcher)
{.btn-grid .my-5}