---
title: Timed Actions
description: 
published: true
date: 2022-07-09T19:59:24.019Z
tags: 
editor: markdown
dateCreated: 2021-08-25T21:32:26.506Z
---

Actions to be performed either repeatedly or for a duration can be defined here.

![timed-actions-context-018.png](/timed-actions-context-018.png){.align-center}

<kbd>Right-clicking</kbd> inside the pane opens the context menu

## Context Menu

---:|---
`Add` | Add a new `Timed Action`
`Edit` | Open the `Edit Timed Action` dialogue to modify the highlighted entry | This is the same as <kbd>Double-Clicking</kbd> the entry
`Delete` | Delete the highlighted entry
`Set Action` | Shortcut to the `Select Action` dialogue
`Enabled` | Shortcut to set the Active state of the Folder Watch entry

When a timer becomes enabled its action will execute on the next occurence.

Unless manually overridden by another [action](/Actions), the `Timed action` will only execute again if both the `Interval` and `Lines` criteria have been met

## Edit Timed Action

![timed-action-edit-018.png](/timed-action-edit-018.png){.align-center}

---:|---
`Enabled` | States this timer is currently running
`Repeat` | Defines if the `Timed Action` should automatically run again once the limiting criteria are met
`Interval` | Minimum time in seconds that must elapse before the action will run again | If `Random` is checked this becomes an upper and lower bound entry
`Lines` | Any non-zero value will pause the action from running again until that many messages have been recieved in chat
`Action` | Choose the [action](Actions) to execute when the timer state becomes `Enabled`

### Action Selector

![action-selector-018.png](/action-selector-018.png){.align-center}

The action list can be filtered using the control in the upper right to help find what you need easier.

To assign an action, select it form the list and press the `Select` button

To unassign all action press the `Clear` button

---

- [<i class="mdi mdi-chevron-left"></i> **Settings *Go Back***](/en/Settings)
{.btn-grid .my-5}