---
title: Changelogs
description: List of new features, bug fixes and improvements
published: true
date: 2022-07-22T14:29:55.129Z
tags: changelogs, release-notes
editor: markdown
dateCreated: 2021-08-25T21:51:24.140Z
---

# Streamer.bot v0.1.10 (Current)

* **Fix:** Fix an issue with authentication for some integrations
* **Fix:** Fix crash when an else action in an if/else sub-action is not set on export
* **Fix:** Fix display of if/else sub-action
* **Fix:** Weighted sub-action option was not being shown correctly, and will also show but be disabled if random is disabled for action or group
* **Fix:** Visual indicator of how many actions/commands are checked updates properly now
* **Fix:** Able to type a reason in the Twitch Timeout sub-action now
* **Fix:** No longer soft errors when getting bits leaderboard, this was not breaking anything
* **Fix:** Updated UI for Gift Subs to avoid confusion, ranges are gift sub milestones for the gifter
* **Fix:** Gift Sub and Gift bomb test events when anonymous should work now
* **Fix:** Importing/Exporting commands clears the persistent counters
* **Update:** Add a hard limit of how many items are shown in Actions pending/history
* **Update:** Better handling of primary config on startup and alert if issue detected
* **Update:** Remove unused check box, Use Bot Account for Messaged in Twitch Accounts tab
* **New:** Add new option for high volume actions to not be included in Action Queue display
* **New:** Added 2 new properties to `CPH` class to get the Twitch Client ID, and the Broadcaster's access token
* **New:** New Twitch event [Ad Run](#twitch-ad-run-event)
* **New:** Add context menu item for commands to reset counters
* **New:** Save the UI positioning of the Action/SubAction list in the Actions tab

## New C# Properties

Added the ability to get **Streamer.bot's** Twitch Client ID by using `CPH.TwitchClientId`, and the broadcaster's access token by using `CPH.TwitchOAuthToken`

I will not be adding the same capability to the YouTube information, since there are quotas involved.

## Twitch Ad Run Event

There is a new event that will be triggered when an ad is run on your channel.

> This event may get some tweaking over time as I can gather more data
{.is-info}


| Variable | Description |
|   ---:|:---  |
| `%adLength%` | The length of the ad in seconds |
| `%adScheduled%` | If this ad was a scheduled ad |

# Streamer.bot v0.1.9

* **Fixed:** Obligatory misc fixes
* **Fixed:** Updating some tooltips
* **Fixed:** PlaySound sub-action Test button being disabled when editing an existing sub-action
* **Fixed:** Updated import/export to properly handle Get/Set Action State sub-action
* **Fixed:** Context menu for Twitch user crashing when clicking ban
* **Fixed:** Gracefully handle authentication error with OBS websocket
* **Fixed:** Editing a Queue name did not update in the list of Queues
* **Fixed:** Prediction badges would cause a silent crash, essentially causing **Streamer.bot** to no longer react to chat
* **Fixed:** Handle potential crash in Add Target Info sub-action
* **Fixed:** Handle potential crash when banning an already banned user from context menu
* **Fixed:** Potential crash when connecting to Twitch account
* **Fixed:** Fix adding/deleting range actions to properly clear the action selection button
* **Fixed:** Twitch forget broadcaster/bot account buttons finally work properly
* **Fixed:** Streamlabs Desktop should work again, my bad on missing this for 0.1.8
* **Update:** Update Twitch Predictions to support up to 10 outcomes, new C# method as well
* **Update:** Support new YouTube gifting events
* **Update:** Add a context menu to the Export dialog action list, to select all actions, and all commands
* **Update:** Rename Broadcasters tab to Stream Apps, to avoid any confusion
* **Update:** Remove deprecated scope and update to current, this will cause a re-authentication for the Broadcaster account
* **Update:** Can open multiple instances of **Streamer.bot** from different folders
* **Update:** YouTube Super Chat and Super Sticker events have been updated to have range based actions
* **Update:** Added new context menu item to collapse/expand all groups in commands list
* **Update:** Pulsoid heart rate event now has ranges
* **Update:** HypeRate heart rate event now has ranges
* **Update:** Increase variable length limit to 64 characters (to handle some obsRaw variables that can parse quite long)
* **Update:** Add a prefix setting to ObsRaw, to be able to customize the variable used for storing the results
* **Update:** Twitch Bot account was missing `channel:moderate` scope, you will need to re-auth this account.
* **Update:** Add new option to file/folder watcher to include subdirectories
* **Update:** Logic If sub-action now has an else condition, and is hence forth known as the [Logif If/Else](#logic-if-else) sub-action
* **Update:** [Twitch Reward C# methods](#twitch-reward-c-methods) were updated
* **New:** Add new [Send Announcement to Channel](#send-announcement-to-channel) sub-action to send a /announce to your channel
* **New:** Add <kbd>Ctrl+C</kbd> and <kbd>Ctrl+V</kbd> shortcuts for sub-actions to copy pasta.
* **New:** Add new [Get Reward Info](#get-reward-info) sub-action to add information about a Twitch reward to arguments
* **New:** Set default sort order for action queues, and save column widths and sorting on save/close
* **New:** Add new event for Twitch Announcements
* **New:** Any service that requires you to connect your account, will now timeout after 60 seconds if you close the browser, so you can try again
* **New:** Added a save button to the Execute C# Code sub-action when you edit it, this will allow you to save without closing the dialog

## New C# Methods

```csharp
void TwitchAnnounce(string message, string color = null);
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

# Streamer.bot v0.1.8
* **Fixed:** Misc fixes
* **Fixed:** DonorDrive profile updated event was sending wrong websocket event type
* **Fixed:** Updated the Action picker to show better message when there are no actions
* **Fixed:** GetActionGroupState sub-action was configured wrong, also a settings upgrade to correct any existing sub-actions
* **Fixed:** ObsSetReplayBufferState was starting/stopping stream, not the buffer
* **Fixed:** ObsSetReplayBufferState had incorrect states
* **Fixed:** Removal of channel reward from the UI should be working correctly now
* **Fixed:** Get/Set Command State sub-actions would cause a crash if there are no commands
* **Fixed:** Set Reward Cooldown sub-action would crash if no Twitch auth data was present
* **Fixed:** OBS Set Audio Track state would toggle when explicitly setting active, this is a bug in obs-websocket 4.x, workaround applied
* **Fixed:** The file selection button in the OBS Take Screenshot sub-action now works
* **Fixed:** Date calculations for Follow Age Info sub-action are now correct
* **Fixed:** Twitch Sub-Counter should no longer cause crashes if file/path is not found
* **Fixed:** Can no longer rename a group to an empty string
* **Fixed:** ObsSourceMute C# methods had an extra unused parameter, this has been removed
* **Fixed:** OBS SetMediaSourceFile sub-action was not parsing scene and source names
* **Fixed:** OBS SetImageSourceFile sub-action was not parsing scene and source names
* **Fixed:** Fix how play not found option works, was stopping the sound even if you were playing via default device
* **Fixed:** Fix group collapsing for Actions
* **Fixed:** Fix sub-action dragging to groups
* **Fixed:** Fix max length for importing actions, there was a 32kb hard limit on the text box, it is now int.MaxValue
* **Update:** Vorbis library updated
* **Update:** Read Random Line sub-action now has a count option, this will add however many lines count is, removing the need to add multiple sub-actions
* **Update:** Update Twitch Timeout sub-action to be able to include a reason
* **Update:** Some tabs related to specific Twitch features have been moved under the Twitch tab
* **Update:** All streaming platforms have been moved to there own combined top level tab
* **Update:** All broadcasting software tabs have been moved to there own combined top level tab
* **Update:** All integrations have been moved to there own combined top level tab
* **Update:** Commands have a new variable available, `%commandId%` which contains the ID of the command that was triggered, this applies for a cooldown action as well.
* **Update:** Added a new variable `%userType%`, this will be present for any actions that adds user information to the arguments
* **Update:** Broadcaster information and random users will no longer be added to every action, this is replaced by sub-actions for the various streaming services
* **Update:** Add Target Info got a new target source, Broadcaster, which will add the broadcasters extended information to the arguments
* **Update:** Requesting new [scopes for your Twitch account](#twitch-new-scopes)
* **Update:** Some updates to the Sub-action context menu, slightly different behaviour and updated text
* **Update:** Move some Twitch classes to a common library for better use within C# code, this may cause some breaking changes
* **Update:** [StreamElements](#streamelements) now uses OAuth to access the service, you no longer need to enter your JWT token.
* **Update:** File Watcher has been updated to support folder watching with filename filters
* **Update:** Cleaned up how Tabs can me moved around and hidden, right click on a tab to bring up a context menu if they can be hidden
* **Update:** Rename SLOBS to Streamlabs Desktop throughout the app
* **Update:** Under the hood, actions have been moved to there own data file
* **Update:** Minor tweaks to the way settings files are saved
* **Update:** Export Actions list is now sorted alphabetically
* **Update:** Remove big Twitch Connect button
* **Update:** Action importing handles Execute C# Code sub-actions a bit better now, and is more intelligent on how references are handled
* **Update:** Various libraries updated
* **Update:** Change default options when creating a Wasapi device for the default device, now matches specific device creation
* **Update:** Alter how device selection works when overriding device in Play Sound and Play Sound from Folder sub-actions
* **Update:** Moved save button to a toolbar at the top of the main window
* **Update:** Moved import/export to buttons on the toolbar, and removed them from the actions context menu
* **New:** Add Twitch First Time Chat indicator, there is a new argument for messages `%firstMessage%`, this is a boolean, true or false
* **New:** Wildcard can be used when subscribing to websocket events
* **New:** New sub-action [Add Team Info](#add-team-info), can get team information for a user
* **New:** ObsRaw has a new option to not add return data to the argument stack; the raw JSON will still be added.  This defaults to true to prevent breaking of existing actions
* **New:** New sub-action [Obs Hide Scene Sources](#obs-hide-scene-sources) and C# method to hide all the sources of a scene, this is the same behaviour as Obs Hide Group Sources, except for scenes.
* **New:** New sub-action [Obs Set Random Scene Source Visible](#obs-set-random-scene-source-visible) and C# method to set a random source in a scene to visible, this is the same behaviour as Obs Set Random Group Source visible, except for scenes.
* **New:** Provided as a 64-bit build
* **New:** [YouTube](#youtube-integration) has been added and is currently a WIP and is being tested.
* **New:** Added a new C# method to run an action by it's id `RunActionById(string actionId, bool runImmediately = true)`
* **New:** New sub-action [Add Broadcaster Information](#add-twitch-broadcaster-information), to add the broadcaster's information to arguments
* **New:** New sub-action [Add Random Users](#add-random-twitch-users), to add a specific number of random Twitch users to the arguments
* **New:** Parse the subscription length from Twitch messages and pass that information forward, will be added as `%monthsSubscribed%` if it is greather then 0
* **New:** Sub-actions can now be enabled/disabled, disabled sub-actions are marked as red in the list
* **New:** Added new [C# methods](#new-c-methods)
* **New:** Now parsing the badge-info tag from Twitch chat, and passing the subscriber duration along
* **New:** The `Ignore Bot` flag for commands now takes into account if the bot account is the same as the broadcaster account and does nothing instead of ignoring, applies to Twitch only
* **New:** VoiceMod integration! Control VoiceMod from **Streamer.bot**
* **New:** Direct [Pulsoid integration](#pulsoid-integration)
* **New:** Direct [HypeRate integration](#hyperate-integration)
* **New:** [OBS Connections](#obs-connections) can be flagged as default, and/or forced.
* **New:** New sub-action [Set Voice Control Command State](#set-voice-control-command-state) to set the state of a Voice Control Command
* **New:** New sub-action [Set Voice Control Command](#set-voice-control-command) to set the command of an anywhere type Voice Control Command
* **New:** Integration with [PolyPop](#polypop-integration)
* **New:** Messages sent via the broadcaster to twitch are now looped back to itself with emote parsing in tow
* **New:** Twemoji parsing for Twitch messages, this will parse Unicode emotes to images
* **New:** Broadcaster information is auto added for certain events where a source is known
* **New:** A new authorization success page will show, instead of a single line of text
* **New:** Twitch/YouTube message sub-actions support multi-line, dialogs have been updated as well
* **New:** Add new GetBroadcaster request to websocket
* **New:** Add new GetBroadcaster endpoint to http server
* **New:** Add new Broken event to Pyramids
* **New:** New event for StreamElements, Merch, trigger actions from merchandise purchases
* **New:** [Action Queues](#action-queues), you can now see actions running in realtime, and see a history of them
* **New:** [Streamer.bot](#streamerbot-website-integration) Website integration
* **New:** Integration with [Kofi](#kofi-integration)
* **New:** Integration with [Patreon](#patreon-integration)
* **New:** Added C# Compiler settings, specifically, you can add common references that will be included with all Execute C# Code sub-actions
* **New:** Custom C# libraries used as references, can now be places in a dlls subfolder
* **New:** Added the StreamElements merch event
* **New:** Twitch Badges are now parsed and added as arguments for relevant events
* **New:** Integration with [TipeeeStream](#tipeestream-integration)
* **New:** Integration with [TreatStream](#treatstream-integration)
* **New:** Added new Log sub-action, to allow logging from within an action
* **New:** Execute C# Code window sizing is saved now, it will open at the last used size
* **New:** Add selected file information to arguments for Play Sound from Folder sub-action; %randomSoundFile% contains the full path of the file and %randomSoundFileName% contains just the file name
* **New:** Commands can be imported/exported along side actions
* **New:** In Execute C# Code window, you can right click to copy the compile log to clipboard
* **New:** Add filtering to Actions list, this will only filter on the action name at the moment
* **New:** Add filtering to Commands list, this will only filter on the command at the moment
* **New:** Add filtering to Action selection dialog, this will only filter on the action name at the moment

## YouTube Integration

Probably one of the most requested features has finally been added, more details will be added to this section over the next few days.

You'll be able to authorize with your YouTube account, and monitor chat, giving you the ability to react to chat messages, super chat, super stickers and more!

More information will follow!

See [YouTube](/Platforms/YouTube) for information on how to get started!

## 64-bit Build

Moving forward, **Streamer.bot** will be offered in a 64-bit build, as opposed to a 32-bit build. This opens up the ability to interface with more librariries and tools using the integrated C# capabilities.

## Twitch New Scopes

When you connect with your broadcaster account, the following new scopes will be requested

* moderator:manage:banned_users
* moderator:read:blocked_terms
* moderator:manage:blocked_terms
* moderator:manage:automod
* moderator:read:automod_settings
* moderator:manage:automod_settings
* moderator:read:chat_settings
* moderator:manage:chat_settings
* whispers:edit
* user:read:follows
{.links-list}

Since I needed to add the moderation scopes, I decided to finally add the whipser edit scope, this will allow the broadcaster account to send whispers.  The restrictions by twitch are still in place!

## New C# Methods

Add the following new C# methods

### User Variables
```csharp
T GetTwitchUserVar<T>(string userName, string varName, bool persisted = true);
T GetYouTubeUserVar<T>(string userName, string varName, bool persisted = true);
void SetTwitchUserVar(string userName, string varName, object value, bool persisted = true);
void SetYouTubeUserVar(string userName, string varName, object value, bool persisted = true);
void UnsetTwitchUserVar(string userName, string varName, bool persisted = true);
void UnsetYouTubeUserVar(string userName, string varName, bool persisted = true);
void UnsetTwitchUser(string userName, bool persisted = true);
void UnsetYouTubeUser(string userName, bool persisted = true);
```

### YouTube Methods
```csharp
void SendYouTubeMessage(string message);
```

### Actions

```csharp
bool RunActionById(string actionId, bool runImmediately = true);
```

### Websocket Custom Servers

```csharp
int WebsocketCustomServerGetConnectionByName(string name);
```

## OBS Connections

OBS connections have 2 new properties in the context menu when you <kbd>Right-click</kbd> on them, Default and Forced.

Setting a connection to default means if the OBS Websocket an OBS sub-action is using is not found, it will use the default selected OBS connection.

Setting a connection to forced, will override all OBS sub-actions and OBS C# methods to use this connection until it is toggled off, or **Streamer.bot** is restarted.

## Streamer.bot Website Integration

Decks, it's all about Decks!  With this integration, Decks can now be fully remote!  They can be opened on any browser, any device, anywhere in the world and control your **Streamer.bot** through button presses.

Under the `Integrations` tab, there is a new `Streamer.bot Website` tab, <kbd>Click</kbd> the `Settings` tab and connect to the **Streamer.bot Website**, this uses the same login mechanism that you used to sign into the website to create your Decks

Expect more things to come with this new feature!

A huge thanks to Whipstickgostop for getting the website side of things all working!

## Kofi Integration

A long asked for integration is finally here, you'll be able to react to events that come from Kofi!

Since Kofi uses WebHooks, this functionality is done through the **Streamer.bot** website, and configured there.

> This **REQUIRES** you to be connected to the Streamer.bot Website to use
{.is-info}

## Patreon Integration

You can now react to Patreon events as they happen!

Patreon also uses WebHooks, so this is done through the **Streamer.bot** website as well.

> This **REQUIRES** you to be connected to the Streamer.bot Website to use
{.is-info}

## VoiceMod Integration

With 0.1.8, you'll be able to select voices, and change options of VoiceMod from within **Streamer.bot**

The following new Sub-Actions are available:
* Get Current Voice
* Select Voice
* Select Random Voice
* Set Censor State
* Set Hear My Voice State
* Set Mute State
* Set Voice Changer State
{.links-list}

New C# Methods available for use.

```csharp
void VoiceModSelectVoice(string voiceId);
string VoiceModGetCurrentVoice();
bool VoiceModGetHearMyselfStatus();
bool VoiceModHearMyVoiceOn();
bool VoiceModHearMyVoiceOff();
bool VoiceModGetVoiceChangerStatus();
bool VoiceModVoiceChangerOn();
bool VoiceModVoiceChangerOff();
void VoiceModCensorOn();
void VoiceModCensorOff();
```
## Pulsoid Integration

**Streamer.bot** now has a direct integration with Pulsoid, attach an action to the Heart Rate Pulse event to receive your heart rate events.

The Heart Rate event happens every second while data is being transmitted from Pulsoid, be aware of this.

| Variable | Description |
|   ---:|-------------|
| `%measuredAt%` | Time the measurement was taken |
| `%heartRate%` | Heart Rate value |

## HypeRate Integration

**Streamer.bot** now has a direct integration with HypeRate.io, attach an action to the Heart Rate Pulse event to receive your heart rate events.

The Heart Rate event happens every second while data is being transmitted from HypeRate, be aware of this.

| Variable | Description |
|   ---:|-------------|
| `%heartRate%` | Heart Rate value |

## StreamElements

The need to find and enter your JWT token are gone.  You can now authenticate with StreamElements to give **Streamer.bot** access to your account to use features from this service.

If you were using StreamElements prior to this version, you will need to login in order to resume functionality.

## PolyPop Integration

Requires the plugin [PolyPop WebSocket Plugin](https://github.com/Jabbey92/PolyPopWebsocketPlugin/releases/tag/1.0) from Jabbey92 in order to work.

Once configured, you'll be able to trigger PolyPop alerts from within **Streamer.bot** using the PolyPop Trigger Alert sub-action

## TipeeeStream Integration
Assign an action to donations that are sent through TipeeeStream

## TreatStream Integration
Assign an action to whenever someone sends you a treat through TreatStream!

## Action Queues

A brand new tab at the top level, `Action Queues` has been added, you'll be able to find your Queues here now, instead of a drop down on the `General` tab under `Settings`.  You'll be able to add, create, delete your queues, pause them, resume them from here as well.

In addition to this, there are 2 additional tabs under `Action Queues`; `Pending Actions` and `Action History`

### Pending Actions

Here you will be able to see **Streamer.bot** working, showing you actions as they get queued up, and when they start running.

<kbd>Right clicking</kbd> on an Action will let you inspect the variables that the action was run with.

### Action History

Here you will be able to see actions that have complete, along with how long it took for them to run.

<kbd>Right clicking</kbd> on an action will bring up a context menu, letting you inspect the variables this action was run with, inspecting the variables after it was completed, as well as requeuing the action as if it was just ran.

## New Sub-Actions

### Obs Hide Scene Sources

Much like it's counter part, Obs Hide Group sources, this will hide all the sources within a scene.

### Obs Set Random Scene Source Visible

Much like it's counter part, Obs Set Random Group Source Visible, this will set a random source within a scene to visible.

### Set Voice Control Command State

Set the state of a Voice Control Command, either enable it or disable it, or toggle its current state.

### Set Voice Control Command

Set the command of a Voice Control Command to the value specified, supports parsing of values.
> This only works for Voice Control Commands that are Anywhere
{.is-info}


# Streamer.bot v0.1.7
* **Fixed:** Get/Set Action State sub-action had incorrect title in dialog
* **Fixed:** OBS Set Replay Buffer state was using incorrect data, should work correctly now
* **Fixed:** Fix typo in Logic if
* **Fixed:** Voice control commands will delete correctly now if it's not active
* **Fixed:** Set Media Source should set a local file correctly now
* **Fixed:** /me no longer causes issues with Twitch emote parsing
* **Fixed:** 7TV DNS resolution failures should no longer cause a startup crash
* **Fixed:** GetClips should be working correctly now when specifying date ranges

> With the addition to being able to specify date ranges/counts for clips, they are no longer returned in newest to oldest, they are returned oldest to newest, as this is how the Twitch API returns the data.  There is no mechanism in the API to change the sort order.  Wiki entries will be updated to indicate this
{.is-info}

* **Update:** Command cooldown action now applies to any command type, instead of exact/start only
* **Update:** FetchURL is now type aware, the variable the result is put into will attempt to match its contents to the proper type, this is an interm update until more can be done.  If you want explicit control, use C# to fetch data
* **Update:** Updated Newtonsoft.Json library to 13.0.1

# Streamer.bot v0.1.6
* **Fixed:** Changing category would cause a crash
* **Fixed:** Clearing chat caused the Banned event to fire
* **Fixed:** Multi-word commands are now checked correctly
* **Fixed:** Custom websocket server would crash when the connection was terminated

# Archives
* [Streamer.bot 0.1.5](/en/Changelogs/Archives/Version-015)
* [Streamer.bot 0.1.4](/en/Changelogs/Archives/Version-014)
* [Streamer.bot 0.1.3](/en/Changelogs/Archives/Version-013)
* [Streamer.bot 0.1.2](/en/Changelogs/Archives/Version-012)
* [Streamer.bot 0.1.1](/en/Changelogs/Archives/Version-011)
* [Streamer.bot 0.1.0](/en/Changelogs/Archives/Version-010)
* [Streamer.bot 0.0.63](/en/Changelogs/Archives/Version-0063)
* [Streamer.bot 0.0.62](/en/Changelogs/Archives/Version-0062)
* [Streamer.bot 0.0.61](/en/Changelogs/Archives/Version-0061)
* [Streamer.bot 0.0.60](/en/Changelogs/Archives/Version-0060)
* [Streamer.bot 0.0.59](/en/Changelogs/Archives/Version-0059)
* [Streamer.bot 0.0.58](/en/Changelogs/Archives/Version-0058)
* [Streamer.bot 0.0.57](/en/Changelogs/Archives/Version-0057)
* [Streamer.bot 0.0.56](/en/Changelogs/Archives/Version-0056)
* [Streamer.bot 0.0.55](/en/Changelogs/Archives/Version-0055)
* [Streamer.bot 0.0.54](/en/Changelogs/Archives/Version-0054)
* [Streamer.bot 0.0.53](/en/Changelogs/Archives/Version-0053)
* [Streamer.bot 0.0.52](/en/Changelogs/Archives/Version-0052)
* [Streamer.bot 0.0.51](/en/Changelogs/Archives/Version-0051)
* [Streamer.bot 0.0.50](/en/Changelogs/Archives/Version-0050)
* [Streamer.bot 0.0.49](/en/Changelogs/Archives/Version-0049)
* [Streamer.bot 0.0.48](/en/Changelogs/Archives/Version-0048)
* [Streamer.bot 0.0.47](/en/Changelogs/Archives/Version-0047)
* [Streamer.bot 0.0.46](/en/Changelogs/Archives/Version-0046)
* [Streamer.bot 0.0.45](/en/Changelogs/Archives/Version-0045)
* [Streamer.bot 0.0.44](/en/Changelogs/Archives/Version-0044)
* [Streamer.bot 0.0.43](/en/Changelogs/Archives/Version-0043)
* [Streamer.bot 0.0.42](/en/Changelogs/Archives/Version-0042)
* [Streamer.bot 0.0.41](/en/Changelogs/Archives/Version-0041)
* [Streamer.bot 0.0.40](/en/Changelogs/Archives/Version-0040)
* [Streamer.bot 0.0.39](/en/Changelogs/Archives/Version-0039)
* [Streamer.bot 0.0.38](/en/Changelogs/Archives/Version-0038)
* [Streamer.bot 0.0.37](/en/Changelogs/Archives/Version-0037)
* [Streamer.bot 0.0.36](/en/Changelogs/Archives/Version-0036)
* [Streamer.bot 0.0.35](/en/Changelogs/Archives/Version-0035)
* [Streamer.bot 0.0.34](/en/Changelogs/Archives/Version-0034)
* [Streamer.bot 0.0.33](/en/Changelogs/Archives/Version-0033)
* [Streamer.bot 0.0.32](/en/Changelogs/Archives/Version-0032)
* [Streamer.bot 0.0.31](/en/Changelogs/Archives/Version-0031)
* [Streamer.bot 0.0.30](/en/Changelogs/Archives/Version-0030)
{.links-list}