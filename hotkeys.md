---
title: Hot Keys
description: Assigning actions to keyboard shortcuts
published: true
date: 2022-10-29T21:49:54.199Z
tags: 
editor: markdown
dateCreated: 2022-06-03T11:21:31.463Z
---

## Overview
The Hot Keys tab enables configuration of global keyboard shortcuts to trigger [actions](/Actions)

This is not to be confused with the [Keyboard Press](/Sub-Actions/Keyboard-Press) sub-action. Hot-Keys are for recieving input, `Keyboard Press` is for sending inputs.

> While a `Hot Key` is defined, even if it is disabled, that key combination will be unavailable to **ALL** applications other than streamer.bot while the application is running. 
This is why all Hot Keys require modifier keys to be set
{.is-warning}

> Where Left and Right versions of `Keys` or `Modifiers` exist no definition is made between them. To streamer.bot they will be treated equally
{.is-info}

![hotkeys-018.png](/hotkeys-018.png)
## Configuration
### Context Menu

<kbd>Right-Click</kbd> in the pane to show the context menu

![hotkey-context-018.png](/hotkey-context-018.png)

---|---
`Add`| Create a new Hot Key definition
`Edit` | Opens the `Edit Hotkey` dialogue for the highlighted entry | This is the same as <kbd>Double-Clicking</kbd> the entry
`Delete` | Deletes the Hot Key and frees up the button combination for Windows
`Set Action` | Shortcut to define the action for this Hot Key
`Group` | Shortcut to assign the Hot Key to a predefined group | Groups can be defined in the `Edit Hotkey` dialogue
`Enabled` | Shortcut to turn the action trigger on or off without removing the key binding

### Edit Hotkey Dialogue

![edit-global-hotkey-018.png](/edit-global-hotkey-018.png)

---|---
`Key` | The keyboard key to be bound
`Modifiers` | All selected modifier keys must be held down as the key is pressed. At least one is required | `Ctrl` `Shift` `Alt`
`Group` | The roll-up group for display on the main pane | New groups can be defined by typing in the control
`Action` | The action to run when the Hot Key combination is pressed | Opens the `Select Action` Dialogue

### Select Action

![action-selector-018.png](/action-selector-018.png)

The action list can be filtered using the control in the upper right to help find what you need easier.

To assign an action, select it form the list and press the `Select` button

To unassign all action press the `Clear` button