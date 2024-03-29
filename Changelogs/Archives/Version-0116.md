---
title: Version 0.1.16
description: Released 2022-12-31
published: true
date: 2023-08-31T01:37:45.714Z
tags: 
editor: markdown
dateCreated: 2023-08-31T01:37:45.714Z
---


* Starting **Streamer.bot** in a folder with uncommon characters should no longer cause a crash
* Fix handling of connetion retries for the **Streamer.bot** website
* Fix forget button for **Streamer.bot** Website integration, was forgetting wrong account
* Handle `Nullable<T>` generics for generic global variable methods
* Twitch Channel Follows, Channel Reward redemptions, and Hype Train completions were not being added to credits
* Gracefully handle errors related to invalid Donor Drive campaign IDs and Custom Endpoint urls
* Gracefully handle errors related to cleaning up Twitch EventSub subscriptions
* Some internal fixes to update download handling
* Setting an action to the TipeeeStream generic event, and deleting it would cause a crash
* Fix potential crash in Add Target Info sub-action when using variables
* StreamLabs, StreamElements, TipeeeStream and TreatStream test button no longer uses a random user, it now uses a fixed `Test User` for tests.  These 4 services do not do any username parsing
* Some tweaks to Twitch Present viewer routines
* Some tweaks to shut down routines
* File/Folder Watcher changed event would crash when parsing as json
* C# Methods for controlling OBS Media State were wired up incorrectly
* C# Method ObsSetMediaSource was inverting a flag for local/url sources
{.changelog-fixes}
