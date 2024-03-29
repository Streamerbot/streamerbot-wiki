---
title: Version 0.1.19
description: Released 2023-03-10
published: true
date: 2023-08-31T01:39:45.955Z
tags: 
editor: markdown
dateCreated: 2023-08-31T01:39:45.955Z
---


* DonorDrive would not reconnect properly
* DonorDrive incentive event was not being triggered
* Some DonorDrive events were not propagating to the UI
* DonorDrive events on the UI were not being sorted correctly when new events happened
* Fix Patreon events not firing
* Fix potential issue with Kofi events
* Fix internal tracking of moderator/vips
* Fix isModerator and isVip related variables for actions, and add target info sub-action
* Update Twitch Clear Chat sub-action to use broadcaster account
* Prevent Test button of some OBS sub-actions when using variables from crashing
* Fix C# method ClearUsersFromGroup()
{.changelog-fixes}

<span></span>

* Twitch EventSub Follow event has been updated to version 2
* Twitch Raid event no longer includes raider's names, see note below
* Remove option to use old style Sub-action menu
* Tweaks to Twitch EventSub connection
* Tweaks to how Twitch retry timers were handled
* Some tweaks to internal viewer object, hopefully duplicate users no longer show
* Play Sound sub-action now supports variables
* Play Sound from Folder sub-action now supports variables
{.changelog-updates}

## Important Notes for Twitch

Currently the Raid Event adds a `%raiderNames%` variable with information on who it thinks is part of the raid.  Because the `tmi` end point is being retired, this variable will no longer be available, as there are no replacement methods that can be used publicly.
> As of April 3rd, 2023, the tmi endpoint for obtaining a channel's list of chatters will be removed, **Streamer.bot** will be removing the aforementioned `%raiderNames%` variable sometime in March with an update.
{.is-warning}
