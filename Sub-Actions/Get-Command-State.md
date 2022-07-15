---
title: Get Command State
description: Retrieve the commands current state
published: true
date: 2022-07-09T19:59:54.091Z
tags: subactions, commands, streamerbot, actions
editor: markdown
dateCreated: 2022-05-23T21:53:34.525Z
---

# Get Command State 

This sub action allows Streamer.bot to gather information on a single commands state.

You could use this to check if a command is enabled or disable in the bot. This value is store in a Boolean variable `commandState` and can only be `True` or `False`. With this sub action you could have it trigger other sub-actions.

## Adding this to your sub actions

To add this to your sub actions all you need to do is go to the action you want this sub action to be included in. Next right click in the sub action section and then navigate to the following `Add Sub-Action` then `Commands` now click `Get Command State`  

![get_command_state.png](/get-command-state/get_command_state.png){.align-center}

Next the bot will ask what command you want to get the state information from.

![get_command_state_dialog_box.png](/get-command-state/get_command_state_dialog_box.png){.align-center}

Select the command and then click `Ok` and that it you have successfully added this sub action.
