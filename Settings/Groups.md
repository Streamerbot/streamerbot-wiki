---
title: Groups
description: 
published: true
date: 2022-08-30T20:20:10.878Z
tags: 
editor: markdown
dateCreated: 2021-08-25T21:32:38.641Z
---

![settings-groups-018.png](/settings-groups-018.png)

Chat users can be added to groups that are defined here.
Groups can be used to define permissions for **[Actions](/Actions)** or in the **[Credits](/Settings/Credits)** function

## Adding / Removing Groups

To create a group, type a name in the lower box and press `Add`

To remove a group, select it from the list and then choose `Delete` from the right-click context menu

> Once a group is defined, users can be manually added to a group by right-clicking on their name in the `Viewers` tab and choosing the group from the sub-menu.
Alternatively, you can Import / Export users from a group using the context menu
{.is-info}


## Bot Groups

The context menu can designate a group as a bot container. Accounts that appear in this group are automatically ignored from the **[Credits](/en/Settings/Credits)** function.
Other features may be made bot group aware in future releases

## Context Menu

![settings-groups-context-018.png](/settings-groups-context-018.png)

---:|---
`Delete` | Deletes the highlighted group
`Clear` | Removes all users from a highlighted group
`Bots` | Designates a Boolean flag to indicate this group contains known bots. Users in a bot group are excluded from credits and certain functionality like First Words
`Export to File` | Save the contents of a group to an `SBGRP` file for sharing with other users or to use as a backup
`Import from File ` | Import the contents of an `SBGRP` file into the highlighted group
