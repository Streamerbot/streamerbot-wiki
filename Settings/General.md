---
title: General
description: 
published: true
date: 2022-07-09T19:59:06.541Z
tags: 
editor: markdown
dateCreated: 2021-08-25T21:32:34.610Z
---

*v0.1.0 - v0.1.7*{.version-badge} | *v0.1.8+*{.version-badge}
---|---
![Settings General](/130132575-9efb23f4-d56f-4c6f-ba21-985ccefda2e9.png)|![settings-general-018.png](/settings-general-018.png)


## Action Queues

*v0.1.8+*{.version-badge}

> **[Action Queues](/en/Action-Queues)** have been moved to their own top-level tab in 0.1.8 and have a complete UI overhaul. Click the link for more information
{.is-info}


*v0.1.0 - v0.1.7*{.version-badge}

All **[Actions](/en/Actions)** defined in Streamerbot must be assigned to an `Action Queue`

By default all actions will trigger immediately but if actions have a duration this may lead to multiple actions happening simultaneously.

New Action Queues can be defined here by typing a name and pressing `Add` > `Blocking`

If an Action Queue is set as `Blocking` then Streamerbot will not run the next triggered action until the currently running one completes.

This can be useful for sound clips or event alerts so they play sequentially rather than all at once


## Audio Output Device

streamer.bot has the ability to play audio directly and can direct audio to a specific device on a per sub-action basis. This setting defines the default device to output to

`Use System Default when selected device is not found`

Use this checkbox to ensure Streamerbot is always able to output sound to a connected device. If you only ever want it to output to a specific device even if it is not connected, clear this setting

`Application Volume`

Defines the default volume at which Streamerbot will play audio. This setting is relative to the inate volume of the sound file being played.

Valid Range is `0% - 200%`

Volume can be overridden on a per sub-action basis if needed

---

- [<i class="mdi mdi-chevron-left"></i> **Settings *Go Back***](/en/Settings)
{.btn-grid .my-5}