---
title: Version 0.1.18
description: Released 2023-02-22
published: true
date: 2023-08-31T01:39:08.255Z
tags: 
editor: markdown
dateCreated: 2023-08-31T01:39:08.255Z
---


* Fix Set Channel Tags sub-action, was limited to 5
* Handle crash from Midi In events that can not be decoded properly
* Fix Custom Websocket Client close action not being triggered
* Fix crash if a tab was hidden and you use the bottom right status to try to navigate to it
* Fix not being able to use a named hostname for an OBS connection
* Fix crash when adding a Custom Websocket server and emptying the port field
* TipeeeStream credentials were not being saved correctly, causing it to lose them every restart
* VoiceMod integration works again, for VoiceMod v2.38.1 and higher
* Fix manual disconnect of Twitch Bot Chat Client
* Fix wording in Set Action group state sub-action
* Fix the Twitch Set Follower Mode/Chat Delay methods
* Fix being able to delete Twitch Hype Train level
* Fix issue with api calls to retrieve list of Twitch banned/timed out users, Twitch changed something with this endpoint
* Fix YouTube Stream EndEvent not triggering
* Adjust SSL protocol capabilities for Chat, PubSub and EventSub connections
* Fix potential crash with OBS Websocket 5 and null values in an item's transform (not sure how this is even possible)
* Fix YouTube present viewers slider value, was using Twitch's slider bar
* Fix test button for Twitch Stream Update, it will now grab the game info from your channel, if no game is selected
* Fix visual bug with VIP and Mod still showing checked (or unchecked) on a user after selecting it.
* Fix clear check box not being disables in the Set Action Queue Pause State sub-action by default
* Fix Twitch Raid Send, Cancel and Go test not working correctly
{.changelog-fixes}

<span></span>

* Update Twitch Add Target Info to include the target's channel title, this will be available in `%targetChannelTitle%`
* Request new scope `moderator:manage:banned_users` for the Twitch Bot account, this was missing for banning users to work
* **Streamer.bot** no longer uses the `games.dat` data file for [Twitch game categories](#twitch-game-categories), it is now realtime search capable
* Updates to the [DonorDrive](#donordrive-updates) integration
* Update Add Broadcaster information to add new variables
* Move Add Follow Age to a new Followers sub-menu
* Switch to new Twitch Follow event sub beta subscription
* Switch to new Twitch Get Followers api call
* Internally handle Twitch Moderator add/remove, updating users without waiting for them to perform an action
* Update Twitch Add Target Info sub-action to include subscription tier, if user is subscribed
* Update retry timer for Twitch services to reset when cancelling the retry
* Update retry timer for Twitch services to have a hard limit of 2 minutes
* Twitch's Shout Out endpoint and EventSub subscriptions have been moved out of beta to general availability
* Rename TwitchSpeaker sub-action
{.changelog-updates}

<span></span>

* Add ability to delete an group in the Action list
* Add ability to delete a group in the Command list
* Add deletion confirmation for Commands
* Add ability to select multiple Actions, and delete them
* Add an `isTest` argument to some Twitch events, this will be set when the event comes from the Test button within **Streamer.bot**
* Read Lines From File sub-action now supports variables in the path, you can edit the path
* Read Random Line From File sub-action now supports variables in the path, you can edit the path
* Write To File sub-action now supports variables in the path, you can edit the path, as well, the path will be created if it does not exist
* **Streamer.bot** is now tracking [Twitch Bit donations](#twitch-bit-donations).
* New C# method to obtain a users total bits donated (this uses the above tracked data)
* Add 2 new sub-actions to add/remove a Twitch VIP
* Add 2 new sub-actions to add/remove a Twitch Moderator
* Add auto-indentation to Execute C# Code sub-action editor
* Add basic auto-completion for the `CPH` object in the Execute C# Code sub-action editor
* Add new C# method to get list of Twitch Rewards
* Add Incentive event to DonorDrive
* Add 2 new sub-actions to get the Latest Twitch Subscriber and Follower
* Add new sub-action to get your [Twitch Follower Count](#twitch-follower-count)
* Add new sub-action to get your [Twitch Subscriber Count and Subscriber Points](#twitch-subscriber-count)
* Add an `isTest` variable to the Community Goal event
* Add last and previous active to Twitch Add Target Info sub-action
* Request new Twitch scope, `moderator:read:followers`
* Add Twitch Chat Cleared event
* Track subscriptions in local Twitch DB
* Add new C# method TwitchIsUserSubscribed
* Add a new inline method `$length()$`, this will get the length of a string, and variables are supported, any variable used will be treated as a string
* **Streamer.bot** will now recognize when a user is given VIP, and update data internally, unfortunately, there is no event for when VIP is removed at the moment
* Provide a notice when Importing commands, that they will be disabled
* Add new sub-action, Read Specific Line from File
* Add new Twitch sub-actions, [Ban User](#twitch-ban-user), [Unban User](#twitch-unban-user), and [UnTimeout User](#twitch-untimeout-user)
* Add ability to set the queue/group of multiple actions at once
* Added some extra logging for Twitch NOTICE responses to help diagnose potential issues
{.changelog-new}

## Important Notes for Twitch
There 2 pending changes for the Twitch API:

The first involves IRC slash commands and 3rd party applications.
> As of Februray 24th, 2023, 3rd party apps will no longer be able to use IRC slash commands.  **Streamer.bot** has already been updated with support for the new API methods to perform these commands
{.is-warning}

The second, involves the old, undocumented API to retrieve a channels list of chatters.  Currently the Raid Event adds a `%raiderNames%` variable with information on who it thinks is part of the raid.  Because this end point is being retired, this variable will no longer be available, as there are no replacement methods that can be used publicly.
> As of April 3rd, 2023, the tmi endpoint for obtaining a channel's list of chatters will be removed, **Streamer.bot** will be removing the afformentioned `%raiderNames%` variable sometime in March with an update.
{.is-warning}

## New C# Methods
```cs
long TwitchGetBitsDonatedByUserId(string userId);
bool TwitchIsUserSubscribed(string userId, out string tier);
```

```cs
List<TwitchReward> TwitchGetRewards()
```
Structure of `TwitchReward`
```cs
public class TwitchReward
{
    public string Id { get; set; }
    public string Title { get; set; }
    public string Prompt { get; set; }
    public int Cost { get; set; }
    public bool InputRequired { get; set; }
    public string BackgroundColor { get; set; }
    public bool Paused { get; set; }
    public bool Enabled { get; set; }
    public bool IsOurs { get; set; }
}

```

## Twitch Game Categories
Trying to manage the games.dat file was starting to get out of hand, so with v0.1.18, it is gone completely, and in its place, when selecting specific games, you're able to perform realtime searches against Twitch's own categories, so you'll always have the most current data moving forward.

Internally, because of this change, some methods were also updated to handle the data file no longer existing.

## Twitch Data
### Twitch Bit Donations
Starting with **Streamer.bot v0.1.18**, it will now keep a record of any bit donations that it sees, this means if something comes in when it is not open, it will never know it happened (since there is no way to get past data from Twitch on this).

The total amount that has been seen is also shown in the user's information in the UI

> If you do a test event, this will be ignored and not added to whomever shows up for the test event.
{.is-info}

## DonorDrive Updates
The DonorDrive integration now pulls a list of known charities from the DonorDrive api, and uses this for the different provider types now.  This is mostly a quality of life improvement so you do not have to try and figure out the endpoint to use for a custom provider.

If the charity you are setting up, doesn't happen to be in the new list, you'll still be able to configure a custom provider

## New Sub-Actions
### Twitch Follower Count
This sub-action will get your current follower count

Variables available:
Name | Description
----:|:------------
`followerCount` | Your follower count

### Twitch Latest Follower
This sub-action will get the last user that followed your channel

Variables available:
Name | Description
----:|:------------
`latestFollower.user` | The display name of the user that followed you
`latestFollower.userName` | The login of the user that followed you
`latestFollower.userId` | The ID of the user that followed you

### Twitch Subscriber Count
This sub-action will get your current subscriber count and point total

Variables available:
Name | Description
----:|:------------
`subscriberCount` | Your subscriber count
`subscriberPoints` | The total number of subscriber points you have

### Twitch Ban User
This sub-action will let you ban a user, you will be able to either enter in a specific user nname, or use a variable.  You can also specify a reason, and use variables in this field

Variables available:
Name | Description
----:|:------------
`banResult` | `True` / `False` if the ban was successful

These variables are only available if the sub-action was successful.
Name | Description
----:|:------------
`bannedUserId` | The user id of the user that was banned
`bannedUserName` | The user login of the user that was banned
`bannedUser` | The display name of the user that was banned

### Twitch Unban User
This sub-action will let you unban a user, you will be able to either enter in a specific user name, or use a variable.

Variables available:
Name | Description
----:|:------------
`unbanResult` | `True` / `False` if the ban was successful

These variables are only available if the sub-action was successful.
Name | Description
----:|:------------
`unbannedUserId` | The user id of the user that was banned
`unbannedUserName` | The user login of the user that was banned
`unbannedUser` | The display name of the user that was banned

### Twitch UnTimeout User
This sub-action will let you ban a user, you will be able to either enter in a specific user nname, or use a variable.

Variables available:
Name | Description
----:|:------------
`banResult` | `True` / `False` if the ban was successful

These variables are only available if the sub-action was successful.
Name | Description
----:|:------------
`unTimedOutUserId` | The user id of the user that was banned
`unTimedOutUserName` | The user login of the user that was banned
`unTimedOutUser` | THe display name of the user that was banned

## Twitch Scopes
Requesting the following new scopes for the broadcaster account
* `moderator:read:followers`
{.grid-list}

Requesting the following new scopes for the bot account, as they were missing or new
* `moderator:manage:banned_users`
{.grid-list}
