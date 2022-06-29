---
title: General
description: 
published: true
date: 2022-01-30T10:26:50.785Z
tags: 
editor: markdown
dateCreated: 2021-08-25T21:32:34.610Z
---

![Settings General](/130132575-9efb23f4-d56f-4c6f-ba21-985ccefda2e9.png)

## Action Queues

All [Actions](/en/Actions) defined in Streamer.bot must be assigned to an `Action Queue`
Action Queues can be `Blocking` or `Non-Blocking` which defines their execution mode.

Mode|Description
---|---
`Non-Blocking` | Any actions sent to this queue will execute immediately and concurrently regardless of whether any actions are already in prgogrss 
`Blocking` | A blocking queue only allows a single action to execute at a time. It will hold all actions sent to it in sequence and will execute them once the current action ends

> A Blocking Queue does not affect any other Blocking Queue, if actions are sent to 2 different blocking queues, they will be allowed to run concurrently so consider grouping similar action types into the same queue if it is important that they never overlap
{.is-success}


By default the only action queue defined is `Non-Blocking` which mean all actions sent to it will trigger immediately but if actions have a duration this may lead to multiple actions happening simultaneously. 

New Action Queues can be defined here by typing a name and pressing `Add`

---


## Audio Output Device

Streamer.bot has the ability to play audio directly and can direct audio to a specific device on a per sub-action basis. This setting defines the default device to output to

`Use System Default when selected device is not found`

Use this checkbox to ensure SB is always able to output sound to a connected device. If you only ever want it to output to a specific device even if it is not connected, clear this setting

`Application Volume`

Defines the default volume at which SB will play audio. This setting is relative to the inate volume of the sound file being played.

Valid Range is `0% - 200%`

Volume can be overridden on a per sub-action basis if needed