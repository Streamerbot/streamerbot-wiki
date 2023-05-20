---
title: Actions
description: Learn how to configure the most important piece of Streamer.bot - Actions & Sub-Actions!
published: true
date: 2023-03-27T18:36:00.251Z
tags: subactions, guides, actions
editor: markdown
dateCreated: 2021-08-25T21:31:09.603Z
---

# Quick Links
- [<i class="mdi mdi-lightning-bolt-outline primary--text"></i> **Sub-Action Reference *All sub-actions that can be executed by your actions in Streamer.bot***](/Sub-Actions)
- [<i class="mdi mdi-creation primary--text"></i> **Event Reference *All events that can trigger your Streamer.bot actions***](/Events)
{.btn-grid .list .my-5}

# Overview
Perhaps the most important piece of Streamer.bot, **Actions** are at the center of everything you do.

**Actions** are configurable sets of [sub-actions](/Sub-Actions) that can be **triggered** by Streamer.bot's event sources, such as [Commands](/Commands), [Events](/Events), [Integrations](/Integrations), and even [your own voice](/Voice-Control)!

![actions-diagram.png](/assets/excalidraw/actions-diagram.png =800x)

This makes actions extremely **powerful**. 

Sub-actions even have the ability to trigger other actions, giving you the ability to **organize** significant pieces of your setup into consolidated sections, and **share** logic across multiple event sources.

As sub-actions are executed, another important feature of Streamer.bot comes into play, the **Argument Stack**, which consists of all [variables](/Variables) available at a given time. 

Each sub-action has the ability to populate new variables for upcoming sub-actions, read existing variables from earlier sub-actions, or even modify them!

# Guide
## The Action Pane
Here you will setup all your primary actions (such as shout outs, subscriptions, cheers, animations, etc.)

This window is split into 3 parts:
1) The list on the left are all of your `Actions` and which `Queue` they belong to.
		This pane will also show any `action groups` you have as collapsible families
    You can filter the list using the control at the top
2) On the right are all of the `sub-actions` for the `action` that is selected. 
3) Below this is the `Information` panel that summarises the selected `sub-action`.

![actions-018.png](/actions-018.png)

## Create a New Action
To begin, <kbd>Right-Click</kbd> in the Actions pane to open the [context menu](/Actions#context-menu). 


Chose `Add` to open the Add Action Dialogue

![new-action-dialogue-018.png](/new-action-dialogue-018.png)

> You can also import actions that have been shared by others by clicking the `Import` button in the upper right corner.
See [Importing and Exporting Actions](/Actions/Importing-and-Exporting) for more details
{.is-success}


### Name
The friendly name the action will be referred to in other areas of the bot

### Group
You can optionally type or select a group name, this is used to organise similar actions into collapsible families to keep the interface clean if you have a large number of actions


### Queue
All actions in Streamer.bot must be assigned to an action `Queue`. Out of the box, the `Default` queue is confiigured as a `non-blocking` queue, meaning all actions sent to it will run immediately and will be allowed to execute concurrently, meaning they can overlap. Additional action queues can be configured in the [Action Queues](/Action-Queues) tab.

> You will want to setup queues that your actions run through to keep them either separated, or to block each other (for instance, when some actions might interact with common elements in OBS). To learn more, see [Action Queues](/Settings/General)
{.is-success}



## Context Menu

![actions-context-018.png](/actions-context-018.png)

### Action Options
<kbd>Right clicking</kbd> on an action reveals a number of options that can be applied to that specific action
Option|Description|Notes
---|---
`Add` |Creates a new action and opens the `Edit` dialogue 
`Edit` |Opens the dialogue to `Rename` the action, add it to a `Group` (or create a group), change it's `Queue` and set any of the `Action Options` flags |This is the same as <kbd>double-clicking</kbd> on the action![new-action-dialogue-018.png](/new-action-dialogue-018.png)
`Delete` |Deletes the highlighted action. |*Deletion confirmation is on by default, this can be toggled on and off in the `Settings` tab*
`Duplicate` |Creates a copy of the highlighted action, including all of its sub-actions.|C# code will be duplicated into a newly renamed method so editing this will not affect the original
`Copy Action ID` |Copies the Unique ID for this action to clipboard so it can be used in C# code or external plugins
`Group` |Allows quick assignment to any previously defined `Action Group`
`Enabled` |Denotes if the action is allowed to run or not
`Always Run` |(`AR`) Means this action will execute if triggered, even if the queue it is attached to is paused.
`Random` |(`RA`) Streamerbot will pick only one sub-action (or group of sub-actions) to execute |Enabling `Random` also enables the `Weight` options on sub-actions, this allows the probability that specific subactions will be chosen to be adjusted. **In Random Action mode all sub-actions contained within a group count as a single entity and will execute the group as if it were a standalone action**
`Concurrent` |(`CC`) Streamerbot will ignore any `Delay` sub-actions and will execute all sub-actions in this action simultaneously, rather than waiting for the previous step to complete
`Collapse All` |Hides all defined `Action Groups` 
`Expand All` | Shows all defined `Action Groups`

***

## Sub Action Pane
<kbd>Right-clicking</kbd> anywhere in the Sub-Action pane will open up the context menu. This will show more options if a sub-action is selected 

![subaction-context-018.png](/subaction-context-018.png =200x)


### Context Menu Options
---|---
`Favorite Sub-Actions` | Opens the list of your favorited sub-actions. To add something to this list go to the Sub-Action e.g. YouTube --> Send Message to Channel and right click on it, now it should appear in the favorite Sub-Actions list. To remove one go to Favorite Sub-Actions and right click on the one that you'd like to remove.
`Edit Sub-Action` | Opens the properties dialogue for the selected sub-action | This is the same as <kbd>double-clicking</kbd> on the sub-action
`Copy Sub-Action` | Copies the selected Sub-Action to the clipboard | This creates a Base64 string intended to be pasted into other actions but it can also be sent to notepad or any other computer to be imported into another version of streamer.bot
`Paste Sub-Action` | Detects if the string in clipboard is Base64 and if so it will paste the subaction into this action
`Duplicate Sub-Action  ` | Clones the selected sub-action into the currently open action
`Delete Sub-Action` | Deletes the selected sub-action | This will show a confirmation dialogue by default unless you have turned it off
`Add Group` | Creates a subaction group | If the action contains any groups the `Move to Group` sub menu will show below this
`Delete Group` | Deletes the selected group | Only shows if selction is a group folder
`Rename Group` | Renames the seleccted group | Only shows if selction is a group folder
`Enabled` | Boolean flag for disabling a sub-action for diagnostic purposes | Disabled sub-actions will be highlighted with Red text
`Random` | Boolean flag to set a group folder as `Random Execution` | This will only execute a single, random sub-action from within the group.
`Weight` | The weight of the Sub-Action when the Action/Group is set on Random.
`Delete all sub-actions` | Erases all sub-actions from this action |  This will show a confirmation dialogue by default unless you have turned it off
`Move` | Submenu to change the order of sub-actions | This has the same effect as keybaord shortcuts <kbd>Ctrl + <i class="mdi mdi-arrow-up-thick"></i></kbd> and <kbd>Ctrl + <i class="mdi mdi-arrow-down-thick"></i></kbd>. Valid options are `Up`, `Down`, `Top`, `Bottom`

> You can also drag and drop items both up and down the list and into and out of group folders
{.is-info}

> Setting a group to Random will also enable the `Weight` options on sub-actions inside that group. 
Weighting is used to make a sub-action more or less likely to be chosen
{.is-success}


### Information
Shows you a small description of the sub-action you have selected