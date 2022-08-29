---
title: Settings
description: 
published: true
date: 2022-07-28T20:53:51.491Z
tags: 
editor: markdown
dateCreated: 2021-08-25T21:33:03.053Z
---

Settings have recieved a major overhaul in 0.1.8 as can be seen below

*v0.1.0 - v0.1.7*{.version-badge} | *v0.1.8+*{.version-badge}
---|---
![ui-settings.png](/ui-settings.png)|![settings-018.png](/settings-018.png)


Many things have been moved to improve accessibility, some features have been relocated to be better grouped to their particular function, leaving configuration options that are not platform specific in the top level Settings tab. These are broken down into secondary tabs by function.

***

- [<i class="mdi mdi-application primary--text"></i>**User Interface**](#user-interface)
- [<i class="mdi mdi-format-align-center primary--text"></i>**General**](#general)
- [<i class="mdi mdi-file-code primary--text"></i>**File/Folder Watcher**](#filefolder-watcher) 
- [<i class="mdi mdi-timelapse primary--text"></i>**Timed Actions**](#timed-actions) 
- [<i class="mdi mdi-credit-card primary--text"></i>**Credits**](#credits) 
- [<i class="mdi mdi-triangle-outline primary--text"></i>**Pyramids**](#pyramids) 
- [<i class="mdi mdi-format-quote-open primary--text"></i>**Quotes**](#quotes) 
- [<i class="mdi mdi-counter primary--text"></i>**Sub Counter**](#sub-counter) 
- [<i class="mdi mdi-folder primary--text"></i>**Groups**](#groups) 
- [<i class="mdi mdi-language-csharp primary--text"></i>**C# Compiler**](#c-compiler)
{.btn-grid .my-5}

***

## User Interface



This tab formerly controled the visibility of the various tabs in Streamer.bot. The abilty to show and hide tabs has been moved to the <kbd>Right-Click</kbd> context menu of each level of tabs

---|---
![top-level-tab-context-018.png](/top-level-tab-context-018.png)|![settings-tabs-context-018.png](/settings-tabs-context-018.png)
The tab order on each level can be changed by dragging the tab to the desired position

-----

---:|---
`Minimize to Tray` | Enables streamer.bot to sent to the system tray instead of the taskbar
`Confirmation on Close` | Enables a popup warning before you close streamer.bot
`Reset Delete Confirmations` | If you have checked the box to supress action and sub-action deletion popup warnings this button re-enables them

***

## General

*v0.1.0 - v0.1.7*{.version-badge} | *v0.1.8+*{.version-badge}
---|---
![Settings General](/130132575-9efb23f4-d56f-4c6f-ba21-985ccefda2e9.png)|![settings-general-018.png](/settings-general-018.png)


### Action Queues

*v0.1.8+*{.version-badge}

> **[Action Queues](/en/Action-Queues)** have been moved to their own top-level tab in 0.1.8 and have a complete UI overhaul. Click the link for more information
{.is-info}


*v0.1.0 - v0.1.7*{.version-badge}

All **[Actions](/en/Actions)** defined in Streamerbot must be assigned to an `Action Queue`

By default all actions will trigger immediately but if actions have a duration this may lead to multiple actions happening simultaneously.

New Action Queues can be defined here by typing a name and pressing `Add` > `Blocking`

If an Action Queue is set as `Blocking` then Streamerbot will not run the next triggered action until the currently running one completes.

This can be useful for sound clips or event alerts so they play sequentially rather than all at once


### Audio Output Device

streamer.bot has the ability to play audio directly and can direct audio to a specific device on a per sub-action basis. This setting defines the default device to output to

`Use System Default when selected device is not found`

Use this checkbox to ensure Streamerbot is always able to output sound to a connected device. If you only ever want it to output to a specific device even if it is not connected, clear this setting

`Application Volume`

Defines the default volume at which Streamerbot will play audio. This setting is relative to the inate volume of the sound file being played.

Valid Range is `0% - 200%`

Volume can be overridden on a per sub-action basis if needed

***

## Twitch Accounts

*v0.1.8+*{.version-badge}

> As of  *v0.1.8+*{.version-badge} **[Twitch Account Configuration](/en/Platforms/Twitch/Accounts)**  has been relocated to `Platforms > Twitch > Accounts`
{.is-info}

*v0.1.0 - v0.1.7*{.version-badge}

![Twitch Account Settings](/119614942-c20a6e00-bdf6-11eb-9647-e56d80d9a8f1.png){.align-center}

### Broadcaster Account

If you want streamer.bot to be able to monitor chat and Twitch! events, a `Broadcaster` account must be defined

Press `Connect to Twitch` to automatically obtain a token

`Auto Connect` will set streamer.bot to connect to twitch with the defined account on startup



### Bot Account

By default any **[sub-actions](/Sub-Actions#main)** will be sent through the Broadcaster account. If you want a secondary account to send these actions / messages it can be defined here in the same way



### Refresh Categories

Use this to pull a current list of available Twitch categories. These can be used as variables in **[sub-actions](/Sub-Actions#main)** for example to change scene if category is changed to a specific game

***

## File/Folder Watcher

With the `File/Folder Watcher` feature you can specify an action to run whenever a file that matches the defined filter is modified

Folder watch actions that have been defined will show in this pane to indicate the `Folder being watched`, `The file filter`, is `Enabled` state and the **[Action](/en/Actions)** that will trigger when the conditions are met

![file-folder-watcher-018.png](/file-folder-watcher-018.png){.align-center}

<kbd>Right-clicking</kbd> inside the pane opens the context menu

### Context Menu

---:|---
`Add` | Add a new folder watch definition
`Edit` | Open the `Edit File/Folder Watcher` dialogue to modify the highlighted entry | This is the same as <kbd>Double-Clicking</kbd> the entry
`Delete` | Delete the highlighted entry
`Set Action` | Shortcut to the `Select Action` dialogue
`Enabled` | Shortcut to set the Active state of the Folder Watch entry



### Edit File Watch Dialogue

*v0.1.0 - v0.1.7*{.version-badge} | *v0.1.8+*{.version-badge}
---|---
![image](/130543487-37f328d3-55b9-4dab-8f53-c46fde0ff967.png)|![file-folder-watcher-edit-018.png](/file-folder-watcher-edit-018.png)
Can only monitor specific files | Monitors entire folders and will trigger on every match defined in the filter



> Filters can be a generic or specific as required and uses the `*` symbol as a wildcard.
> eg. `*.*` will match all files in a folder, `*.txt` will match all text files, `some*.txt` will match all text files that begin with the word `some` and so on
{.is-success}

#### Action Selector

![action-selector-018.png](/action-selector-018.png){.align-center}

The action list can be filtered using the control in the upper right to help find what you need easier.

To assign an action, select it form the list and press the `Select` button

To unassign all action press the `Clear` button

-----

The action specified will get access to the following variables:

Name | Description
----:|:------------
| `%changeType%` | The type of change | `Changed`, `Created`, `Deleted`
| `%fullPath%` | The full path to the file |
| `%fileName%` | The file name with extension |
| `%name%` | The file name without the extention |
| `%empty%` | A boolean value indicating if the file is empty |

If you have `As JSON` ticked, it will add all root elements as arguments.

If `As JSON` is not ticked, it will add the following variables if the JSON cannot be parsed:

Name | Description
----:|:------------
| `%lineCount%` | The number of lines in the file |
| `%line#%` | The line of the file, replace # with the line number you want |
| `%lineEscaped#%` | The line of the file URL encoded, replace # with the line number you want |


***

## Timed Actions

Actions to be performed either repeatedly or for a duration can be defined here.

![timed-actions-context-018.png](/timed-actions-context-018.png){.align-center}

<kbd>Right-clicking</kbd> inside the pane opens the context menu

### Context Menu

---:|---
`Add` | Add a new `Timed Action`
`Edit` | Open the `Edit Timed Action` dialogue to modify the highlighted entry | This is the same as <kbd>Double-Clicking</kbd> the entry
`Delete` | Delete the highlighted entry
`Set Action` | Shortcut to the `Select Action` dialogue
`Enabled` | Shortcut to set the Active state of the Folder Watch entry

When a timer becomes enabled its action will execute on the next occurence.

Unless manually overridden by another [action](/Actions), the `Timed action` will only execute again if both the `Interval` and `Lines` criteria have been met

### Edit Timed Action

![timed-action-edit-018.png](/timed-action-edit-018.png){.align-center}

---:|---
`Enabled` | States this timer is currently running
`Repeat` | Defines if the `Timed Action` should automatically run again once the limiting criteria are met
`Interval` | Minimum time in seconds that must elapse before the action will run again | If `Random` is checked this becomes an upper and lower bound entry
`Lines` | Any non-zero value will pause the action from running again until that many messages have been recieved in chat
`Action` | Choose the [action](Actions) to execute when the timer state becomes `Enabled`

#### Action Selector

![action-selector-018.png](/action-selector-018.png){.align-center}

The action list can be filtered using the control in the upper right to help find what you need easier.

To assign an action, select it form the list and press the `Select` button

To unassign all action press the `Clear` button


***

## [Credits](/en/Settings/Credits)

![settings-credits-018.png](/settings-credits-018.png){.align-center}

The SLCB Credits functions have been ported to Streamer.bot and can be configured here.

As the function is quite extensive, this will remain on its own page. [click here](/en/Settings/Credits) for more information

***

## Pyramids

*v0.1.0 - v0.1.7*{.version-badge} | *v0.1.8+*{.version-badge}
---|---
![Pyramids Settings](/119623512-28e05500-be00-11eb-8340-5a02c1c94521.png)|![settings-pyramids-018.png](/settings-pyramids-018.png)

Monitor chat for successful uninterrupted completion of an emote pyramid and execute an [Action](/Actions)

**0.1.8** adds the abilty to trigger a different action if someone interrupts the emote pyramid

> This feature supports emotes from Twitch!, [BetterTwitchTV](https://betterttv.com/) and [FrankerFaceZ](https://www.frankerfacez.com/)
{.is-info}

***

## Quotes

Streamer.bot has a built in quote system.



![settings-quotes-018.png](/settings-quotes-018.png){.align-center}

> You must have a category set to add quotes to the quote system, otherwise it tries to set null data which can cause a crash or invalid data structure
{.is-danger}

### Twitch Chat commands

The following Twitch! commands are hard coded into the application and can be used to `Add`, `Remove` and to `Retrieve` the quotes
```
!quote add <string>
!quote del #
!quote
```
> Please note, the add and remove commands need at least the permission level as defined in the setting `Perm to Add`
This relies on the `Role` attribute from Twitch! and as such can only be set to `Viewer` `VIP` `Moderator` or `Broadcaster`
{.is-success}


### Example messages to be used in actions for quote addition / removal
Quote addition message
```
%user%, quote has been added as #%quoteId%
```
Quote output message
```
#%quoteId%: %quote% [%quoteUser%, %quoteGame% at %quoteTime%]
```

### Additional use of the quote system
![Quote Action](/123520512-082e4800-d6a9-11eb-95f9-e5c016b42f21.png){.align-center}

You can automate the retrieval of a specific or random quote using the Get Quote Action. Once retrieved, you can reference the quote using the variables shown above in the Quote output message.

***

## Sub Counter

![settings-subcounter-018.png](/settings-subcounter-018.png){.align-center}

The Sub-counter will increment a persisted variable every time a sub is monitored by the application and save the result to a specified file.

When `subCounter` equals the `rollover` target a celebration action can be triggered
Reaching `rollover` goal will reset the counter and increment the `rolloverCount` variable

> Setting the `rollover` goal to 0 will disable the rollover function and just count subs indefinately
{.is-info}

## Groups

![settings-groups-018.png](/settings-groups-018.png){.align-center}

Chat users can be added to groups that are defined here.
Groups can be used to define permissions for **[Actions](/Actions)** or in the **[Credits](/Settings/Credits)** function

### Adding / Removing Groups

To create a group, type a name in the lower box and press `Add`

To remove a group, select it from the list and then choose `Delete` from the right-click context menu

> Once a group is defined, users can be manually added to a group by right-clicking on their name in the `Viewers` tab and choosing the group from the sub-menu.
Alternatively, you can Import / Export users from a group using the context menu
{.is-info}


### Bot Groups

The context menu can designate a group as a bot container. Accounts that appear in this group are automatically ignored from the **[Credits](/en/Settings/Credits)** function.
Other features may be made bot group aware in future releases

### Context Menu

![settings-groups-context-018.png](/settings-groups-context-018.png){.align-center}

---:|---
`Delete` | Deletes the highlighted group
`Clear` | Removes all users from a highlighted group
`Bots` | Designates a Boolean flag to indicate this group contains known bots. Users in a bot group are excluded from credits and certain functionality like First Words
`Export to File` | Save the contents of a group to an `SBGRP` file for sharing with other users or to use as a backup
`Import from File ` | Import the contents of an `SBGRP` file into the highlighted group

***



## C# Compiler

The default C# compiler in **0.1.8** is already very robust and will find its own references standard references most of the time, but if you want to include any custom dll libraries that will be automatically added to all C# sub-actions you can define them here

![settings-cs-compiler-018.png](/settings-cs-compiler-018.png){.align-center}



