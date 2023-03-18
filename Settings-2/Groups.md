---
title: Groups
description: Settings Reference
published: false
date: 2023-03-18T20:41:18.756Z
tags: 
editor: markdown
dateCreated: 2023-03-18T20:41:06.036Z
---

## Overview
On this tab you can change your user groups

![Image representing the Streamer.bot Settings Groups Tab](/Settings/groups/groups.png =700x)

## Configuration
### Groups
Here you will see a list of all created groups.

### Add Group
You can type in this field to add a group name.

- <kbd><i class="mdi mdi-checkbox-marked"></i> Bots</kbd> when this checkbox is checked it will categorize it under `Bot Groups`.
- <kbd><i class="mdi mdi-checkbox-blank"></i> Bots</kbd> when this checkbox is **not** checked it will categorize it under `Normal Groups`.

### Users
When a group is highlighted it will show a list of all the users in that group.

To add people to this group you can use a couple C# Methods or even directly from the `Viewers` tab, if you <kbd>right-click</kbd> on a user you can add them to the previously made groups.

## Context Menu
When <kbd>right-clicking</kbd> on a group it will open up a context menu with a few diffrent options. And those will be explained below.

### Delete
This will delete the group.

### Clear
This will clear all the users from this group.

### Bots
This will toggle this group between a `Normal Group` and a `Bot Group`.

### Export to File
This will export all the group data to a `.sbgrp` file. This will export the user data to a Streamer.bot Group file in a Compressed JSON format, it must be noted that this won't import a group, this will only import the user data on an existing group. This can be imported to everyone who you give this file.

### Import from File
This will import users from a file to an existing group. This file has been [exported](#export-to-file) previously. You can simply just click this button and select the file.

---

- [<i class="mdi mdi-chevron-left"></i>**Settings Reference *Go Back***](/Settings-2)
{.btn-grid .my-5}