---
title: Version 0.1.10
description: Released 2022-06-24
published: true
date: 2023-08-31T01:33:15.080Z
tags: 
editor: markdown
dateCreated: 2023-08-31T01:33:15.080Z
---


* An issue with authentication for some integrations
* Crash when an else action in an if/else sub-action is not set on export
* Display of if/else sub-action
* Weighted sub-action option was not being shown correctly, and will also show but be disabled if random is disabled for action or group
* Visual indicator of how many actions/commands are checked updates properly now
* Able to type a reason in the Twitch Timeout sub-action now
* No longer soft errors when getting bits leaderboard, this was not breaking anything
* Updated UI for Gift Subs to avoid confusion, ranges are gift sub milestones for the gifter
* Gift Sub and Gift bomb test events when anonymous should work now
* Importing/Exporting commands clears the persistent counters
{.changelog-fixes}

<span></span>

* Add a hard limit of how many items are shown in Actions pending/history
* Better handling of primary config on startup and alert if issue detected
* Remove unused check box, Use Bot Account for Messaged in Twitch Accounts tab
{.changelog-updates}

<span></span>

* Add new option for high volume actions to not be included in Action Queue display
* Added 2 new properties to `CPH` class to get the Twitch Client ID, and the Broadcaster's access token
* New Twitch event [Ad Run](#twitch-ad-run-event)
* Add context menu item for commands to reset counters
* Save the UI positioning of the Action/SubAction list in the Actions tab
{.changelog-new}

## New C# Properties

Added the ability to get **Streamer.bot's** Twitch Client ID by using `CPH.TwitchClientId`, and the broadcaster's access token by using `CPH.TwitchOAuthToken`

I will not be adding the same capability to the YouTube information, since there are quotas involved.

## Twitch Ad Run Event

There is a new event that will be triggered when an ad is run on your channel.

> This event may get some tweaking over time as I can gather more data
{.is-info}


Name | Description
----:|:------------
`%adLength%` | The length of the ad in seconds
`%adScheduled%` | If this ad was a scheduled ad