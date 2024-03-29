---
title: Version 0.1.9
description: Released 2022-06-16
published: true
date: 2023-08-31T01:32:04.280Z
tags: 
editor: markdown
dateCreated: 2023-08-31T01:32:04.280Z
---


* Obligatory misc fixes
* Updating some tooltips
* PlaySound sub-action Test button being disabled when editing an existing sub-action
* Updated import/export to properly handle Get/Set Action State sub-action
* Context menu for Twitch user crashing when clicking ban
* Gracefully handle authentication error with OBS websocket
* Editing a Queue name did not update in the list of Queues
* Prediction badges would cause a silent crash, essentially causing **Streamer.bot** to no longer react to chat
* Handle potential crash in Add Target Info sub-action
* Handle potential crash when banning an already banned user from context menu
* Potential crash when connecting to Twitch account
* Adding/deleting range actions to properly clear the action selection button
* Twitch forget broadcaster/bot account buttons finally work properly
* Streamlabs Desktop should work again, my bad on missing this for 0.1.8
{.changelog-fixes}

<span></span>

* Update Twitch Predictions to support up to 10 outcomes, new C# method as well
* Support new YouTube gifting events
* Add a context menu to the Export dialog action list, to select all actions, and all commands
* Rename Broadcasters tab to Stream Apps, to avoid any confusion
* Remove deprecated scope and update to current, this will cause a re-authentication for the Broadcaster account
* Can open multiple instances of **Streamer.bot** from different folders
* YouTube Super Chat and Super Sticker events have been updated to have range based actions
* Added new context menu item to collapse/expand all groups in commands list
* Pulsoid heart rate event now has ranges
* HypeRate heart rate event now has ranges
* Increase variable length limit to 64 characters (to handle some obsRaw variables that can parse quite long)
* Add a prefix setting to ObsRaw, to be able to customize the variable used for storing the results
* Twitch Bot account was missing `channel:moderate` scope, you will need to re-auth this account.
* Add new option to file/folder watcher to include subdirectories
* Logic If sub-action now has an else condition, and is hence forth known as the [Logif If/Else](#logic-if-else) sub-action
* [Twitch Reward C# methods](#twitch-reward-c-methods) were updated
{.changelog-updates}

<span></span>

* Add new [Send Announcement to Channel](#send-announcement-to-channel) sub-action to send a /announce to your channel
* Add <kbd>Ctrl+C</kbd> and <kbd>Ctrl+V</kbd> shortcuts for sub-actions to copy pasta.
* Add new [Get Reward Info](#get-reward-info) sub-action to add information about a Twitch reward to arguments
* Set default sort order for action queues, and save column widths and sorting on save/close
* Add new event for Twitch Announcements
* Any service that requires you to connect your account, will now timeout after 60 seconds if you close the browser, so you can try again
* Added a save button to the Execute C# Code sub-action when you edit it, this will allow you to save without closing the dialog
{.changelog-new}

## New C# Methods

```csharp
void TwitchAnnounce(string message, bool bot = false, string color = null);
```
> Even though the color parameter is present, currently, due to a Twitch limitation, only null is supported, this will use the default announce command.  When Twitch fixes this, supported values will be `blue`, `orange`, `green`, `purple`
{.is-warning}

```csharp
string TwitchPredictionCreate(string title, List<string> options, int duration);
```

## Updated C# Methods

### Twitch Reward C# Methods
The following methods have had there return value changed from void to bool, to indicate success or failure.

```csharp
bool UpdateRewardTitle(string rewardId, string title);
bool UpdateRewardPrompt(string rewardId, string prompt);
bool UpdateReward(string rewardId, string title = null, string prompt = null, int? cost = null);
```

Any use of these methods should be uneffected, as calling without using the bool is the same as calling a void method, the result is just thrown away

## Updated Sub-actions

### Logic If/Else

The Logif If/Else sub-action got a bit smarter, you can now have an else condition.

![sub-action-logic-if-else.png](/sub-action-logic-if-else.png)

## New Sub-actions

### Send Announcement to Channel

With this sub-action you can send an /announce to your channel.  While there is a drop down to pick the color, this is disabled on purpose, as the color specific commands currently do not work outside of the main Twitch chat.  Once this is enabled on Twitch's side, I will enable this dropdown

> Due to a Twitch limitation, only the default announce command is currently supported.  When Twitch fixes this, the other colors (`blue`, `orange`, `green`, `purple`) will be supported.
{.is-warning}

### Get Reward Info

This sub-action will add information about the selected reward to the arguments