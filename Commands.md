---
title: Commands
description: Define and configure chat commands with Streamer.bot
published: true
date: 2022-07-01T19:44:33.935Z
tags: commands
editor: markdown
dateCreated: 2021-08-25T21:31:22.243Z
---

## Overview

![commands-018.png](/commands-018.png =x400)

This tab is used to view and define chat commands you want Streamer.bot to watch for and the actions each should perform. 

<kbd>Right-click</kbd> anywhere in the pane to show the context menu. This will show diffrent options depending what was highlighted.

![commands-context-018.png](/commands-context-018.png)

## Context Menu

---|---
`Add` | Create a new command
`Edit` | Edit the highlighted command | This is the same as <kbd>double-clicking</kbd> on the command
`Delete` | Deletes the highlighted command
`Set Action` | Shortcut to the `Select Action` dialogue | Selected action will assign to the main [Action](/en/Actions) for the command
`Set Cooldown Action` | Shortcut to the `Select Action` dialogue | Selected action will assign to the cooldown [Action](/en/Actions) for the command
`Group` | Assign the command to a pre-defined group | Groups can be created in the `Edit Command` dialogue by typing directly into the dropdown control
`Enabled` | Shortcut to toggle the command on and off
`Copy Command Id` | Copies the unique ID string for the highlighted command to the clipboard


***

## Edit Command Dialogue

Command settings are defined on the `Edit Command` dialogue window

![edit-command-018.png](/edit-command-018.png)


### Mode
Mode | Description | Notes
---|---|---
`Basic` | Commands must match (one of) the exact strings entered | Basic commands must use a location option : `Start`, `Anywhere` or `Exact`
`Regex` | Commands will trigger if the regex returns true for any part of the message entered in chat 


### Location

| Location | Description |
|     ---:|--------------|
| `Start` | The command must be typed as the first character in a line of chat or it will be ignored |
| `Exact` | The command typed in chat must match the string defined in the command exactly with no trailing characters|
| `Anywhere` | Command will trigger if the string is entered anywhere in a line of chat, regardless of what comes before or after |

### Command(s)

This is the exact string that Streamer.Bot is monitoring chat for. Commands may have multiple trigger strings / aliases, enter them one per line.
> The cooldowns and counters on a command is common across all its aliases. If you want an action to be be triggered by multiple commands and have each have its own cooldown you sould create each separately
{.is-info}


### Group

For housekeeping, you can define a group name by typing or selecting from the dropdown. Grouped commands will appear together in a collapsable section in the `Commands` tab 
Groups are also used in conjuction with the `Get Commands` & `Command Group State` subactions



### Action

The name of the defined [action](/Actions) to execute. Pressing this button opens the `Select Action` dialogue

![action-selector-018.png](/action-selector-018.png)

The action list can be filtered using the control in the upper right to help find what you need easier.

To assign an action, select it form the list and press the `Select` button

To unassign all action press the `Clear` button

## Options

A number of toggle switches can be set to change the behaviour of the command processing

Toggle  | Description | Notes
---|---|---
`Enabled` | Defines if the command set will be processed at all | This state can be changed programatically by the `Set Command State` subactions
`Include` | Defines if the command set is avaible to the `Get Commands` subaction | Included commands will show up in the `All` category and also in the selected `Group`
`Ignore Bot Account` | If the `Bot Account` is not blank, this toggle will ignore command processing from that account | If the `Bot Account` is the same as your `Broadcaster Account` this property is ignored
`Case Sensitive` | Requires the command to be typed with the exact case specified


### Source(s)

You can pick any combination of the following sources for the origination of the command.

|Source | Description |
|   ---:|-------------|
| `Twitch Message` | Accept command from the Twitch! chat of the `Twitch Broadcaster` account |
| `YouTube Message` | Accept commands from the YouTube chat of the `YouTube Broadcaster` account |
| `Twitch Whisper` | Accept command from whispers sent to the `Twitch Broadcaster` account |
| `Twitch Subscription Message` | Allow the command to be sent as part of a Twitch! subscription message |
| `Twitch Re-subscription Message` | Allow the command to be sent as part of a Twitch! re-sub message |



### Counters

Actions in Streamer.bot have per-session and per-command variables `counter` & `userCounter` that records how many times that command has been used. 

By default this clears when the application is closed but the following options will save the counts to the settings file so they will persist between sessions

---|---
`Persist Counter` | Save the total number of executions for this command or any of its aliases
`Persist per User Counter` | Save details of how often each user has executed this command or any of its aliases


### Cooldowns

A cooldown can be set for a command set on both a `Global` and `Per-User` basis, this prevents the main action being run again while the cooldown is active.


Option | Description | Notes 
---|---|---
`Global Cooldown` | Defines the minimum time in seconds before the command set can be used again by anyone
`User Cooldown` | Defines the minimum time in seconds before the command can be used again by that specific chat user
`Cooldown Action` | Defines which action should run if the command set is called while a cooldown is in effect | This is useful to output a message to chat to explain they have to wait, but there is no spam protection on the cooldown action 

> The `Broadcaster` is always exepmt from cooldowns. If you need to test this is working correctly use a different account
{.is-success}



## Permissions

By default, commands can be executed by anyone in chat but you may wish to restrict specific commands to certain [groups](/Settings/Groups) or even specific users, the default permissions are shown below in the image. 

![basic_command_.png](/basic_command_.png) 

### Grant Type

---|---
`Allow` | Only `Groups` / `Users` specified can use this command
`Deny` | Everyone except specified `Groups` / `Users` can use this command

>  If the `Allowed` / `Denied` pane is blank then the permission applies to everyone, otherwise it applies to only the entities listed
{.is-info}

> The `Broadcaster` is always exempt from permission settings. If you want to specifically exclude the broadcaster from an action you should define this with a `Logic > If` subaction
{.is-success}



