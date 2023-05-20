---
title: Groups
description: Settings Reference
published: false
date: 2023-03-18T20:46:35.297Z
tags: 
editor: markdown
dateCreated: 2023-03-18T20:41:06.036Z
---

## Overview
On this tab you can change your user groups

![Image representing the Streamer.bot Settings Groups Tab](/Settings/groups/groups.png =700x)

## Configuration
### Groups
Here you will see a list of all the created groups.

### Add Group
To add a group you need to give it a name and choose if you want it to be a bots group or not. Then simply click the `Add` button.

- <kbd><i class="mdi mdi-checkbox-marked"></i> Bots</kbd> when this checkbox is checked it will categorize the group under `Bot Groups`.
- <kbd><i class="mdi mdi-checkbox-blank"></i> Bots</kbd> when this checkbox is **not** checked it will categorize the group under `Normal Groups`.

### Users
When a group is highlighted it will show a list of all the users in that group.

To add people to this group you can use a couple C# Methods or an easier method is to do it directly from the `Viewers` tab, if you <kbd>right-click</kbd> on a user you can add them to the previously made groups.

## Context Menu
When <kbd>right-clicking</kbd> on a group it will open up a context menu with a few diffrent options. And those will be explained below.

### Delete
This will delete the group.

### Clear
This will clear all the users from this group.

### Bots
This will toggle this group between a `Normal Group` and a `Bot Group`.

### Export to File
This will export all the user data to a `.sbgrp` file. This will export it to a Streamer.bot Group file in a Compressed JSON format, it must be noted that this file won't import a group because this will only import the user data on an existing group. 

This file can be shared if you want to share groups with diffrent people.

### Import from File
This will import users from a file to an existing group. This file has been [exported](#export-to-file) previously. You can simply just click this button and select the file.

---

- [<i class="mdi mdi-chevron-left"></i>**Settings Reference *Go Back***](/Settings-2)
{.btn-grid .my-5}