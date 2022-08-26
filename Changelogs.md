---
title: Changelogs
description: List of new features, bug fixes and improvements
published: true
date: 2022-08-26T19:19:06.302Z
tags: changelogs, release-notes
editor: markdown
dateCreated: 2021-08-25T21:51:24.140Z
---

# Streamer.bot v0.1.11 (WIP)
Upcoming changes in the next release!{.subtitle}

* Commands in an import will be disabled by default, this is more of a security precaution
* Action updates were not properly being sent to the Streamer.bot website for decks
* Pyramids not resetting correctly if a single emote is used after a previous single emote
* Twitch Reward Set Global Cooldown sub-action, properly lists rewards now
* Crash when using <kbd>Ctrl+C</kbd> on a group in an action
* `inputUrlEncoded#` variables to actually be the word, and not the entire message for each one
* Get Team Info For Target silently crashing
* Better handling for the Twitch Get Present Viewers tick, optimizations to limit potential API calls
* OBS Raw sub-action was not saving the prefix
* Silent null ref crash for timed actions when Twitch is not connected, should be compeltely decoupled now
* Twitch GiftSubs from a GiftBomb were being counted twice in the sub-counter
* `CPH.RunAction` properly checks if an action is enabled when trying to run it
{.changelog-fixes}

<span></span>

* New [Twitch scopes](#twitch-new-scopes) requested
* Twitch Announcements have been updated with the new endpoint and scope, can send announcements in all colors now
* Extend First Chat event to YouTube
* Some updates to how YouTube streams are found, this is still very much a WIP and more fixes will come
* Auto strip newline and whitespace at the end of an import string when pasting
* Remove Bits from Twitch Polls, as it's being removed outright by Twitch
* `Execute C# Code` sub-action will now warn if you try to close it by the X and you have unsaved changes
{.changelog-updates}

<span></span>

* [OBS Websocket v5.x](#obs-websocket-v5x) Support
* Added new variable `%wsIdx%` to WebsocketClient action arguments, which is the index of the client, 0 based, -1 if not found
* Added new variable `%wssIdx%` to CustomWebsocketServer action arguments, which is the index of the server, 0 based, -1 if not found
* Added new variable `%wssId%` to CustomWebsocketServer action arguments, which is the ID of the websocket server
* Add new VoiceMod sub-action to play a soundboard sound
* Add new VoiceMod sub-action to stop  playing all VoiceMod sounds
* Regex commands will now add match group values as arguments, `%match[#]%`, as well as named match groups, if you're using `?<groupName>` in your regex
* [Lumia Stream](#lumia-stream) integration!
* New sub-action Send Command for Lumia Stream
* New sub-action Set Color for Lumia Stream
{.changelog-new}

## OBS Websocket v5.x

Support for OBS Websocket v5.0 comes to **Streamer.bot** v0.1.11.  For the most part this is a transparent change for users, just edit your OBS Websocket within **Streamer.bot** and change to v5.x.

Unfortunately, the OBS Raw sub-action will not work between v4.9.x and v5.x; the methods to obtain and set information are incompatible.  Even having a translation layer on this leaves too much to chance and likely have the wrong output.

> OBS Raw Sub-action will not be compatible between the 2 versions
{.is-warning}

More information on upgrading your OBS Raw sub-actions will be forthcoming.

The new OBS Raw format for OBS Websocket v5.x is the following:
```json
{
  "requestType": "request method",
  "requestData": { ... }
}
```

### Get Scene Item Properties Sub-Action

A quick note about this sub-action, while I tried to keep data structures the same between the 2 versions, the data for this one unfortunately changed. There is now a common format for the data

```json
{
  "name": "name",
  "itemId": 0,
  "visible": true,
  "locked": false,
  "transform": {
    "alignment": 0,
    "boundsAlignment": 0,
    "boundsHeight": 0.0,
    "boundsType": "string",
    "boundsWidth": 0.0,
    "cropBottom": 0,
    "cropLeft": 0,
    "cropRight": 0,
    "cropTop": 0,
    "height": 0.0,
    "positionX": 0.0,
    "positionY": 0.0,
    "rotation": 0.0,
    "scaleX": 0.0,
    "scaleY": 0.0,
    "sourceHeight": 0.0,
    "sourceWidth": 0.0,
    "width": 0.0
  }
}
```

## Lumia Stream
**Streamer.bot** gains another integration, Lumia Stream! You can now connect to Lumia Stream and set light colors from within **Streamer.bot**

## Twitch New Scopes

When you connect with your broadcaster account, the following new scopes will be requested

* `moderator:manage:announcements`
* `channel:manage:moderators`
* `channel:manage:vips`
* `user:manage:whispers`
{.grid-list}

When you connect with your bot account, the following new scopes will be requested

* `moderator:manage:announcements`
* `user:manage:whispers`
{.grid-list}

# Streamer.bot v0.1.10 (Current)
Released 2022-06-24{.subtitle}

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


| Variable | Description |
|   ---:|:---  |
| `%adLength%` | The length of the ad in seconds |
| `%adScheduled%` | If this ad was a scheduled ad |

# Streamer.bot v0.1.9
Released 2022-06-16{.subtitle}

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

# Streamer.bot v0.1.8
Released 2022-06-01{.subtitle}

* Misc fixes
* DonorDrive profile updated event was sending wrong websocket event type
* Updated the Action picker to show better message when there are no actions
* GetActionGroupState sub-action was configured wrong, also a settings upgrade to correct any existing sub-actions
* ObsSetReplayBufferState was starting/stopping stream, not the buffer
* ObsSetReplayBufferState had incorrect states
* Removal of channel reward from the UI should be working correctly now
* Get/Set Command State sub-actions would cause a crash if there are no commands
* Set Reward Cooldown sub-action would crash if no Twitch auth data was present
* OBS Set Audio Track state would toggle when explicitly setting active, this is a bug in obs-websocket 4.x, workaround applied
* The file selection button in the OBS Take Screenshot sub-action now works
* Date calculations for Follow Age Info sub-action are now correct
* Twitch Sub-Counter should no longer cause crashes if file/path is not found
* Can no longer rename a group to an empty string
* ObsSourceMute C# methods had an extra unused parameter, this has been removed
* OBS SetMediaSourceFile sub-action was not parsing scene and source names
* OBS SetImageSourceFile sub-action was not parsing scene and source names
* How play not found option works, was stopping the sound even if you were playing via default device
* Group collapsing for Actions
* Sub-action dragging to groups
* Max length for importing actions, there was a 32kb hard limit on the text box, it is now int.MaxValue
{.changelog-fixes}

<span></span>

* Vorbis library updated
* Read Random Line sub-action now has a count option, this will add however many lines count is, removing the need to add multiple sub-actions
* Update Twitch Timeout sub-action to be able to include a reason
* Some tabs related to specific Twitch features have been moved under the Twitch tab
* All streaming platforms have been moved to there own combined top level tab
* All broadcasting software tabs have been moved to there own combined top level tab
* All integrations have been moved to there own combined top level tab
* Commands have a new variable available, `%commandId%` which contains the ID of the command that was triggered, this applies for a cooldown action as well.
* Added a new variable `%userType%`, this will be present for any actions that adds user information to the arguments
* Broadcaster information and random users will no longer be added to every action, this is replaced by sub-actions for the various streaming services
* Add Target Info got a new target source, Broadcaster, which will add the broadcasters extended information to the arguments
* Requesting new [scopes for your Twitch account](#twitch-new-scopes)
* Some updates to the Sub-action context menu, slightly different behaviour and updated text
* Move some Twitch classes to a common library for better use within C# code, this may cause some breaking changes
* [StreamElements](#streamelements) now uses OAuth to access the service, you no longer need to enter your JWT token.
* File Watcher has been updated to support folder watching with filename filters
* Cleaned up how Tabs can me moved around and hidden, right click on a tab to bring up a context menu if they can be hidden
* Rename SLOBS to Streamlabs Desktop throughout the app
* Under the hood, actions have been moved to there own data file
* Minor tweaks to the way settings files are saved
* Export Actions list is now sorted alphabetically
* Remove big Twitch Connect button
* Action importing handles Execute C# Code sub-actions a bit better now, and is more intelligent on how references are handled
* Various libraries updated
* Change default options when creating a Wasapi device for the default device, now matches specific device creation
* Alter how device selection works when overriding device in Play Sound and Play Sound from Folder sub-actions
* Moved save button to a toolbar at the top of the main window
* Moved import/export to buttons on the toolbar, and removed them from the actions context menu
{.changelog-updates}

<span></span>

* Add Twitch First Time Chat indicator, there is a new argument for messages `%firstMessage%`, this is a boolean, true or false
* Wildcard can be used when subscribing to websocket events
* New sub-action [Add Team Info](#add-team-info), can get team information for a user
* ObsRaw has a new option to not add return data to the argument stack; the raw JSON will still be added.  This defaults to true to prevent breaking of existing actions
* New sub-action [Obs Hide Scene Sources](#obs-hide-scene-sources) and C# method to hide all the sources of a scene, this is the same behaviour as Obs Hide Group Sources, except for scenes.
* New sub-action [Obs Set Random Scene Source Visible](#obs-set-random-scene-source-visible) and C# method to set a random source in a scene to visible, this is the same behaviour as Obs Set Random Group Source visible, except for scenes.
* Provided as a 64-bit build
* [YouTube](#youtube-integration) has been added and is currently a WIP and is being tested.
* Added a new C# method to run an action by it's id `RunActionById(string actionId, bool runImmediately = true)`
* New sub-action [Add Broadcaster Information](#add-twitch-broadcaster-information), to add the broadcaster's information to arguments
* New sub-action [Add Random Users](#add-random-twitch-users), to add a specific number of random Twitch users to the arguments
* Parse the subscription length from Twitch messages and pass that information forward, will be added as `%monthsSubscribed%` if it is greather then 0
* Sub-actions can now be enabled/disabled, disabled sub-actions are marked as red in the list
* Added new [C# methods](#new-c-methods)
* Now parsing the badge-info tag from Twitch chat, and passing the subscriber duration along
* The `Ignore Bot` flag for commands now takes into account if the bot account is the same as the broadcaster account and does nothing instead of ignoring, applies to Twitch only
* VoiceMod integration! Control VoiceMod from **Streamer.bot**
* Direct [Pulsoid integration](#pulsoid-integration)
* Direct [HypeRate integration](#hyperate-integration)
* [OBS Connections](#obs-connections) can be flagged as default, and/or forced.
* New sub-action [Set Voice Control Command State](#set-voice-control-command-state) to set the state of a Voice Control Command
* New sub-action [Set Voice Control Command](#set-voice-control-command) to set the command of an anywhere type Voice Control Command
* Integration with [PolyPop](#polypop-integration)
* Messages sent via the broadcaster to twitch are now looped back to itself with emote parsing in tow
* Twemoji parsing for Twitch messages, this will parse Unicode emotes to images
* Broadcaster information is auto added for certain events where a source is known
* A new authorization success page will show, instead of a single line of text
* Twitch/YouTube message sub-actions support multi-line, dialogs have been updated as well
* Add new GetBroadcaster request to websocket
* Add new GetBroadcaster endpoint to http server
* Add new Broken event to Pyramids
* New event for StreamElements, Merch, trigger actions from merchandise purchases
* [Action Queues](#action-queues), you can now see actions running in realtime, and see a history of them
* [Streamer.bot](#streamerbot-website-integration) Website integration
* Integration with [Kofi](#kofi-integration)
* Integration with [Patreon](#patreon-integration)
* Added C# Compiler settings, specifically, you can add common references that will be included with all Execute C# Code sub-actions
* Custom C# libraries used as references, can now be places in a dlls subfolder
* Added the StreamElements merch event
* Twitch Badges are now parsed and added as arguments for relevant events
* Integration with [TipeeeStream](#tipeestream-integration)
* Integration with [TreatStream](#treatstream-integration)
* Added new Log sub-action, to allow logging from within an action
* Execute C# Code window sizing is saved now, it will open at the last used size
* Add selected file information to arguments for Play Sound from Folder sub-action; %randomSoundFile% contains the full path of the file and %randomSoundFileName% contains just the file name
* Commands can be imported/exported along side actions
* In Execute C# Code window, you can right click to copy the compile log to clipboard
* Add filtering to Actions list, this will only filter on the action name at the moment
* Add filtering to Commands list, this will only filter on the command at the moment
* Add filtering to Action selection dialog, this will only filter on the action name at the moment
{.changelog-new}

## YouTube Integration

Probably one of the most requested features has finally been added, more details will be added to this section over the next few days.

You'll be able to authorize with your YouTube account, and monitor chat, giving you the ability to react to chat messages, super chat, super stickers and more!

More information will follow!

See [YouTube](/Platforms/YouTube) for information on how to get started!

## 64-bit Build

Moving forward, **Streamer.bot** will be offered in a 64-bit build, as opposed to a 32-bit build. This opens up the ability to interface with more librariries and tools using the integrated C# capabilities.

## Twitch New Scopes

When you connect with your broadcaster account, the following new scopes will be requested

* `moderator:manage:banned_users`
* `moderator:read:blocked_terms`
* `moderator:manage:blocked_terms`
* `moderator:manage:automod`
* `moderator:read:automod_settings`
* `moderator:manage:automod_settings`
* `moderator:read:chat_settings`
* `moderator:manage:chat_settings`
* `whispers:edit`
* `user:read:follows`
{.grid-list}

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
{.grid-list}

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
Released 2022-01-16{.subtitle}

* Get/Set Action State sub-action had incorrect title in dialog
* OBS Set Replay Buffer state was using incorrect data, should work correctly now
* Fix typo in Logic if
* Voice control commands will delete correctly now if it's not active
* Set Media Source should set a local file correctly now
* /me no longer causes issues with Twitch emote parsing
* 7TV DNS resolution failures should no longer cause a startup crash
* GetClips should be working correctly now when specifying date ranges
{.changelog-fixes}

> With the addition to being able to specify date ranges/counts for clips, they are no longer returned in newest to oldest, they are returned oldest to newest, as this is how the Twitch API returns the data.  There is no mechanism in the API to change the sort order.  Wiki entries will be updated to indicate this
{.is-info}

* Command cooldown action now applies to any command type, instead of exact/start only
* FetchURL is now type aware, the variable the result is put into will attempt to match its contents to the proper type, this is an interm update until more can be done.  If you want explicit control, use C# to fetch data
* Updated Newtonsoft.Json library to 13.0.1
{.changelog-updates}


# Streamer.bot v0.1.6
Released 2021-12-27{.subtitle}

* Changing category would cause a crash
* Clearing chat caused the Banned event to fire
* Multi-word commands are now checked correctly
* Custom websocket server would crash when the connection was terminated
{.changelog-fixes}

# Streamer.bot v0.1.5
Released 2021-12-25{.subtitle}

*  Typos
*  Regression in Perform Command, variables were not being parsed
*  Better handling of OBS events, and issues surrounding editing
*  Better handling of OBS/SLOBS sub-actions where a scene is empty, signifying the source exists in any scene
*  Anonymous cheers could cause a crash with credits
*  Some underlying issues with Streamlabs/Streamelements sockets
*  Add error handling when importing actions, should no longer crash in the event something is malformed
*  Handle WASAPI init errors on playback, specifically if its unable to initialize the device
*  Some additional error handling in websocket server/client dialogs
*  Rare scenario where fetching mod/vip lists internally could cause a crash
*  Handle data issues with SLOBS not adhering to its on JSON structures
*  Grouping in OBS Events was not being handled properly (typo)
*  Custom WebsocketServer message event was emitting the wrong type of event internally
*  GetCredits method was putting Hype Train conductors in the wrong field
*  Twitch Slow mode sub-action was not being deserialized properly
*  Read Lines from File and Read Random Line from File sub-actions, input validation input was not working correctly
*  Creating/editing reward sub-actions when there are none could cause a potential crash
*  Fix culture parsing of decimals for streamlabs and stream elements testing of donations, decimals should work for all cultures now
*  Potential crash in some sub-actions and empty scenes
*  Drag/drop of sub-action was not properly marking cached info as dirty
*  Voice control UI was not selecting the saved input device on startup
*  Issues with Twitch dropping connection, this maybe an on going fix, trying to refine why this behaviour is happening.  This manifests as if the bot stops reacting to most Twitch actions.
*  Actions were not being flagged as dirty when using drag/drop to re-organize sub-actions, making it look like they were not being saved
*  Streamlabs donation events were being ignored, they should go through now
*  Resuming a queue should now correctly fire off any actions that were in the queue
*  Masimum values for max redeems per user/per stream are set to correct maximums now, should no longer cause a crash
*  Data type mismatch when creating Stream Markers (oops)
*  Exporting actions with a queue did not preserve is the queue was blocking
*  Importing actions did not correctly show blocking/non-blocking queue info (visual only)
*  Custom websocket server firing incorrect actions
{.changelog-fixes}

<span></span>

*  [Delay](#delay-sub-action) sub-action can now accept variables
*  Twitch Slow Mode sub-action (and C# method) has been updated to allow specifiying the delay time
*  Update [Twitch Clip C# Methods](#twitch-clip-c-methods) related methods, see section for more details
*  %s are auto removed for the variable in the LogicIf dialog
*  Add Insert and Delete as usable keys for Hot Keys and Keyboard Press
*  [Set Reward Cost](#set-reward-cost) sub-action can now accept variables, and give an operator option to add, subtract, multiply or divide the value
*  [Set Argument](#set-argument) sub-action has been updated with full parsing support for its value, and the increment option removed, see section for more details
*  New way to [pick actions](#new-way-to-pick-actions) for events!
*  Added `%rewardCost%` and `%rewardPrompt%` to the variables for reward redemptions
*  The action list in the action sub-action is now sorted alphabetically
*  Action lists returned by the HTTP server and Websocket GetActions requests are now sorted alphabetically
*  Timed Actions have been decoupled from the Twitch connection, they will now start on application start
*  Resolution for Timed Actions has been lowered to 1s from 53, this is tenetive and needs testing internally
*  Add game box art (`%gameBoxArt%` and `%oldGameBoxArt%`) to the stream update event
*  Global Get/Set sub-actions have been extended to parse the variable name, bringing support for `%variable%` parsing for the variable name itself
*  Setting auto reset first words cache time to -1 will disable this check on startup
*  Alter how commands start with check is performed, so a command of `!so` wouldn't trigger on `!socials`
{.changelog-updates}

<span></span>

*  New sub-action to set the [OBS Replay Buffer State](#obs-replay-buffer-state), as well as C# methods
*  Added 2 new [C# Methods](#obs-color-helpers) to translate colors to OBS color
*  Added a new [C# Helper Method](#obs-helper-methods) to get a connection index by name
*  New sub-action [Set Reward Title](#set-reward-title), along with a C# method
*  New sub-action [Set Reward Prompt](#set-reward-prompt), along with a C# method
*  New sub-action [Update Reward](#update-reward), where you can set the title, prompt and cost of a reward in one call, along with a C# method
*  Added ability to double click to edit Websocket Servers and Clients
*  Added new variable `%spokenTextInput%` to Speech To Text events for Commands, this is the text spoken without the trigger word, and is only support for Start based commands
*  Added new variable `%spokenCommand%` to Speech to Text events that will contain the command that triggered the event
*  A new Twitch scope will be requested on first start, Commercial Edit
*  New sub-action [OBS Get Scene Item Properties](#obs-get-scene-item-properties) to get the properties of a scene item, as well as a C# method
*  New sub-action [Start Commercial](#start-commercial) to start commercials on your channel, as well as C# methods
*  New sub-action [OBS Set Media Source File](#obs-set-media-source-file) to set the file of an OBS Media Source, as well as C# methods
*  New sub-action [OBS Set Image Source File](#obs-set-image-source-file) to set the file of an OBS Image Source, as well as C# methods
*  Support for [DonorDrive](#donordrive) services! This includes ExtraLife, StackUp and any other charity drives that use DonorDrive.
*  The first [Inline Function](#inline-function) has arrived!
*  Added new keys to [Hot Keys and Keyboard Presses](#new-hot-keys-and-keyboard-presses)
*  Add new [C# Methods](#command-cooldown-methods) to alter the cooldowns of a command
*  New sub-action [Get Commands](#get-commands) to get a list of your commands
*  New sub-action [Run Commercial](#run-commercial) to run a commercial on your channel, as well as a C# method
*  Added option to Gift Subs to ignore those that come from a Gift Bomb, there is also a variable `%fromGiftBomb%` that can be checked
*  With the new way actions are selected, most lists have a new menu item to select the action without needing to edit
*  The user list in the Timeout User sub-action is now sorted alphabetically, and I've updated the control to support auto complete suggestions to help find user names.
*  New sub-action [Get Command State](#get-command-state) to get the state of a command, or command group
*  New sub-action [Get Action State](#get-action-state) to get the state of an action, or action group
*  Added some [new action wide variables](#new-action-wide-variables)
*  New sub-action [TwitchSpeaker Speak](#twitchspeaker-speak) to provide a simpler way to get TwitchSpeaker to speak for you, as well as a C# method
*  3 new Twitch events can be broadcast across the websocket, message deletion, user timeout and user ban
*  New sub-action **Break** that will halt the action from continuing, mostly used when debugging
*  Added new events for twitch message deletion, user being timed out, and a user being banned
{.changelog-new}

## DonorDrive

You can add either your team, or personal campaign for ExtraLife, StackUp or any other charity that uses DonorDrive, and attach an action to a donation event.

This is not limited to just 1, you can add multiple as well.

More info to be filled in.

## Inline Function

Up until now, the only thing that could be parsed were `%variables%`, I have finally added the first function to this, `$math()$`.

Anywhere there is full parsing, you can now perform math operations, and also use variable within the math function itself.

Here is just a simple example of an action:
* Set Argument `%x%` to `1`, `%x%` is now 1
* Set Argument `%x%` to `$math(%x%+1)$`, incrememnt `%x%` by `1`, `%x%` is now `2`
* Set Argument `%x%` to `$math(%x%^2)$`, set `%x%` to `%x%` to the power of `2`, `%x%` is now `4`
* Set Argument `%x%` to `$math(%x%*16)$`, set `%x%` to `%x%` times `16`, `%x%` is now `64`

A page with the possible usages of the `math` function will be added as well, as it is more then just your basic arithmetic (yes, you can even do derivatives or integrals if you wanted to).

## New Way to Pick Actions

With this update, I've completely removed the mess of dropdowns to select events.  This was slowing down the application with the amount of updates this could generate to keep track of any changes to your actions.

There is now a clickable button that will bring up a dialog with your actions grouped and sorted like they are on the main actions page.  This dialog is very much a WIP, and will evolve over time.

In addition to events, most dialogs where you picked actions (Commands, Channel Reward, Timed Actions, etc) have also received this update.

As an added bonus, most of the lists where you edit these kinds events, now have a new context menu item to be able to change the action without having to go in and edit the command, reward, etc.

## Set Argument

With the addition of the `$math()$` inline function, the **Set Argument** sub-action has been updated to fully support parsing its value, and the Increment option has been removed, as you can now use the math function to do this.

![sub-action-set-argument-002.png](/sub-action-set-argument-002.png)

> A configuration upgrade will happen, converting any Set Argument that is flagged as increment will have its value converted to `$math(Variable+Value)$`, there is the possibility this may not fully work, so it is advised to check any Set Arguments you have that were converted.
{.is-info}

## New Hot Keys and Keyboard Presses

A few new keys were added to be the list of keys usable for Hot Keys and Keyboard Press

* Semi Colon `;:`
* Forward Slash `/?`
* Tilde `~`
* Opening Square Brace `[{`
* Backslash `\|`
* Closing Square Brace `]}`
* Double Quote `"`
* Comma `,<`
* Minus Sign `-_`
* Period `.>`
* Plus Sign `+=`
* Break
* Scroll Lock
* Media Next Track
* Media Previous Track
* Media Stop
* Media Play/Pause
* Media Volume Mute
* Media Volume Down
* Media Volume Up

## Twitch Clip C# Methods

Previously, the C# calls to get Twitch clips, only allowed getting all the clips, leaving it upto you to sort through them afterwards.  If there were many clips for a user, this could take a while to fetch, and as it wsa a paginated call, it was only grabbing 20 at a time leading to further slow down.

The first fix, it now fetches 100 at a time (the maximum allowed per call),  This means, ever paged call takes approximately 800 milliseconds to complete.

The methods for fetching clips have been updated to allow for a count to be specified, and it will only grab that many clips for a user, default sorted newest to oldest.

They have also been updated to specific a date range (start and end date) to look for clips, as well as a day timespan, to specifiy the past 7 days, or the past 30 days, etc.

```csharp
List<ClipData> GetClipsForUser(int userId, int count);
List<ClipData> GetClipsForUser(int userId, DateTime start, DateTime end);
List<ClipData> GetClipsForUser(int userId, DateTime start, DateTime end, int count);
List<ClipData> GetClipsForUser(int userId, TimeSpan duration);
List<ClipData> GetClipsForUser(int userId, TimeSpan duration, int count);
List<ClipData> GetClipsForUser(string userName, int count);
List<ClipData> GetClipsForUser(string username, DateTime start, DateTime end);
List<ClipData> GetClipsForUser(string username, DateTime start, DateTime end, int count);
List<ClipData> GetClipsForUser(string username, TimeSpan duration);
List<ClipData> GetClipsForUser(string username, TimeSpan duration, int count);
List<ClipData> GetClipsForGame(int gameId, int count);
List<ClipData> GetClipsForGame(int gameId, DateTime start, DateTime end);
List<ClipData> GetClipsForGame(int gameId, DateTime start, DateTime end, int count);
List<ClipData> GetClipsForGame(int gameId, TimeSpan duration);
List<ClipData> GetClipsForGame(int gameId, TimeSpan duration, int count);
```

## New Action Wide Variables

If Twitch is connected, actions will have the following five variables available to them

| Variable | Description |
|   ---:|-------------|
| `%broadcastUser%` | The Twitch display name of the broadcast account |
| `%broadcastUserName%` | The Twitch user name of the broadcast account |
| `%broadcastUserId%` | The Twitch user ID of the broadcast account |
| `%broadcastIsAffiliate%` | true/false value indicating if the broadcast account is an affiliate |
| `%broadcastIsPartner%` | true/false value indicating if the broadcast account is a partner |

## New Sub-Actions

### Set Reward Title

Change the Title of an existing reward, this also supports the use of `%variables%`

![sub-action-set-reward-title-001.png](/sub-action-set-reward-title-001.png)

#### New C# Method

```csharp
void UpdateRewardTitle(string rewardId, string title);
```

### Set Reward Prompt

Change the prompt of a reward, this also supports the use of `%variables%`

![sub-action-set-reward-prompt-001.png](/sub-action-set-reward-prompt-001.png)

> There is a bug on Twitch's side with the API call, it is not possible to set the prompt to an empty value once it has been set.  This issue also happens with Twitch's own editing of a reward on the website
{.is-info}

#### New C# Method
```csharp
void UpdateRewardPrompt(string rewardId, string prompt);
```

### Update Reward

Change the title, prompt and/or cost of a reward in 1 sub-action.

![sub-action-reward-update-001.png](/sub-action-reward-update-001.png)

#### New C# Method
```csharp
void UpdateReward(string rewardId, string title = null, string prompt = null, int? cost = null);
```

### OBS Replay Buffer State

New sub-action to control the Replay Buffer state, no longer need to use OBS Raw to achieve this

![sub-action-obs-set-replay-buffer-state-001.png](/sub-action-obs-set-replay-buffer-state-001.png)

#### New C# Methods for OBS Replay Buffer State
```csharp
void ObsSetReplayBufferState(int state, int connection = 0);
void ObsReplayBufferStart(int connection = 0);
void ObsReplayBufferStop(int connection = 0);
void ObsReplayBufferSave(int connection = 0);
```

### OBS Get Scene Item Properties

New sub-action that will make a `GetSceneItemProperties` call to the websocket, and much like OBS Raw, will add the results into your arguments in the form of `props.<path>`

#### New C# Methods for OBS Get Scene Item Properties
```csharp
string ObsGetSceneItemProperties(string scene, string source, int connection = 0);
```

### Run Commercial

Allows you to start a commercial on your channel.  Commercials can be either 30s, 60s, 90s, 120s, 150s, or 180s in duration.

![sub-action-run-commercial-001.png](/sub-action-run-commercial-001.png)

#### New C# Method

```csharp
void TwitchRunCommercial(int duration);
```

### OBS Set Media Source File

Allows you to change the file of an OBS Media source, `%variables%` are supported.

![sub-action-obs-set-media-source-file-001.png](/sub-action-obs-set-media-source-file-001.png)

#### New C# Method
```csharp
void ObsSetMediaSourceFile(string scene, string source, string file, int connection = 0);
```

### OBS Set Image Source File

Allows you to change the file of an OBS Image source, `%variables%` are supported.

![sub-action-obs-set-image-source-file-001.png](/sub-action-obs-set-image-source-file-001.png)

#### New C# Method
```csharp
void ObsSetImageSourceFile(string scene, string source, string file, int connection = 0);
```

### Get Commands

Will give you a list of your commands, into the variable of your choice.  Can be limited down by command group, or if the user doing the command has permissions

![sub-action-get-commands-001.png](/sub-action-get-commands-001.png)

2 variables will be added, the first will be a comma delimited string of your commands, that will be placed in the variable you picked, as well, a list of the commands (for use in C#) will be placed in `[VariableName]List`, so from the screenshot, `%commandsList%` would contain a `List<string>` of your commands

### Get Command State

Using this sub-action you can get the state of a command, whether its enabled or disabled, as well as get the state of a group of commands, if they're all enabled or disabled, or mixed.

#### Variables provided for `Get Command State`

| Variable | Description |
|   ---:|-------------|
| `%commandState%` | The state of the command `true`/`false` |

#### Variable provided for `Get Command Group State`

| Variable | Description |
|   ---:|-------------|
| `%commandGroupState%` | The state of the command group, see table below for information |
| `%commandsEnabled%` | A `Dictionary<Guid, Guid>` of command ID, action IDs, of commands that are enabled |
| `%commandsDisabled%` | A `Dictionary<Guid, Guid>` of command ID, action IDs, of commands that are disabled |

#### Possible values for `%commandGroupState%`

| Value | Description |
|   ---:|-------------|
| `0` | All disabled |
| `1` | All enabled |
| `2` | Mixed |

### Get Action State

Using this sub-action you can get the state of an action, whether its enabled or disabled, as well as get the state of a group of actions, if they're all enabled or disabled, or mixed.

#### Variables provided for `Get Action State`

| Variable | Description |
|   ---:|-------------|
| `%actionState%` | The state of the action `true`/`false` |

#### Variables provided for `Get Action Group State`

| Variable | Description |
|   ---:|-------------|
| `%actionGroupState%` | The state of the command group, see table below for information |
| `%actionsEnabled%` | A list of action IDs that are enabled |
| `%actionsDisabled%` | A list of action IDs that are disabled |

#### Possible values for `%actionGroupState%`

| Value | Description |
|   ---:|-------------|
| `0` | All disabled |
| `1` | All enabled |
| `2` | Mixed |

### TwitchSpeaker Speak

To simplify uusing TwitchSpeaker with **Streamer.bot**, you can us this sub-action to have messages spoken by TwitchSpeaker.  Before you'd have to use the UDP broadcast sub-action.

#### New C# Method
```csharp
void TtsSpeak(string voiceAlias, string message, bool badWordFilter = false);
```

> This requires you to be using TwitchSpeaker for TTS
{.is-info}

## New C# Methods
### OBS Color Helpers
```csharp
long ObsConvertRgb(int a, int r, int g, int b);
long ObsConvertColorHex(string colorHex);
```

### OBS Helper Methods
```csharp
int ObsGetConnectionByName(string name);
```

### Command Cooldown Methods
> The ID can be retreived by right clicking a command, and clicking the Copy Command ID option
{.is-info}

```csharp
void CommandResetGlobalCooldown(string id);
void CommandAddToGlobalCooldown(string id, int seconds);
void CommandResetUserCooldown(string id, int userId);
void CommandAddToUserCooldown(string id, int userId, int seconds);
void CommandResetAllUserCooldowns(string id);
void CommandAddToAllUserCooldowns(string id, int seconds);
```

# Streamer.bot v0.1.4
Released 2021/10/23{.subtitle}

*  Various typos
*  Editing a channel reward and setting max per stream works correctly now
*  Creating or duplicating a channel reward correctly says its owned now
*  Add Follow Age Info was not allowing variable entry
*  Streaming with no game category selected would cause a crash
*  Community Goal contribution event was tied to the wrong underlying event
*  Added a flag to testing the follow event, so it can bypass the built in follow/unfollow protection
*  Potential crash when a websocket or http server port was in use
*  Harden some of the code surrounding Twitch tokens, hopefully less crashes
*  Community goal percent completed calculation was wrong
*  Enabling/disabling commands by group was not correctly working
*  Re-enable maximize box on main window
*  Poll update and complete events were executing the wrong action setting
*  The Twitch Raid start event sends the profile image url at 70x70, updated this to be the larger 300x300
*  PlaySound/PlaySoundFromFolder C# methods were not properly waiting for sound to complete
*  Handle potential crash on startup related to voice control
*  Was not correctly forgetting bot account
*  Poll/Prediction Create, Update and Complete actions were being stored but not shown, the visual bug has been fixed.
*  Find Refs in C# Execute could cause a crash if there is a bad image (a dll) in your application folder
*  Some hardening of code surrounding export to clipboard
*  SetTimerState sub-action not resetting the timer correctly when enabling
*  StreamElements/Streamlabs events no longer try to resolve the user to a seen viewer
*  Community goal help text
*  S potential deadlock that could occur with OBS Websockets
*  Setting a source's mute state in SLOBS should work correctly now
{.changelog-fixes}

<span></span>

*  Credits no longer include the Broadcaster or Bot account in any lists
*  [Perform Command](#perform-command) sub-action is being updated with new options and capabilities
*  [ReadLinesFromFile](#readlinesfromfile-and-readrandomlinesfromfile) and [ReadRandomLinesFromFile](#readlinesfromfile-and-readrandomlinesfromfile) were updated to parse variables, and attempt auto-typing
*  Added `%obsRaw._json%` variable to the OBS Raw sub-action, it contains the result as is, so it could be parsed in a C# action
*  Missed some variables in [Twitch Prediction](#twitch-predictions) completion event
*  Missed some variables in [Twitch Polls](#twitch-polls) completeion event
*  [Commands](#commands) got a bit of an overhaul, check the section for more details
*  When adding actions, group will be auto filled based on selection
*  Improved shutdown time
*  Change how [Twitch Gift Sub Bombs/Gift Subs](#twitch-gift-sub-bombgift-subs) are handled
*  OBS Set Source Filter State sub-action will now list the global audio sources if they are in use, and will be shown in the list before the scene sources
*  When switching scenes in most OBS sub-actions, an attempt will be made to pre-select the same named source if possible, this is an ongoing update
*  Variable replacements now supports inline formatting, using any of the standard C# formatting options, example `%donatedValue:N2%` would give a number with 2 decimal places, if the value is a number
*  Set Argument subaction can now accept variables as values, be sure to use %s, so you can assign a variable to another variable
*  Logic If now supports variable names as comparison values, be sure to use %s
*  UDP Broadcast sub-action now behaves similarly to OBS Raw in how replacements are done, invalid characters should no longer be an issue, and numbers will be treated as numbers
*  Add new `%messageCheermotesStripped%` variable to a cheer event, that retains all the emotes, and only stiprs cheermotes
*  Allow variable usage for SLOBS Set Active Scene sub-action
*  Made the text entry for the Twitch Send Message sub-action a bit biger and wrap lines, so more can be seen
{.changelog-updates}

<span></span>

*  New [Hot Key Support](#hot-key-support)
*  [Confirimation dialog](#confirmation-dialogs) when deleting an action, a sub-action, or all sub-actions
*  [Confirimation dialog] when closing bot.
*  Minimize/Close to tray option
*  Expanded OBS capability with [OBS Events](#obs-events) being able to trigger actions
*  New [OBS Take Screenshot](#obs-take-screenshot) sub-action
*  New [OBS Set Audio Track State](#obs-set-audio-track-state) sub-action
*  New [OBS Set Media State](#obs-set-media-state) sub-action
*  New [Twitch Set Channel Title](#twitch-set-channel-title) sub-action
*  New [Twitch Set Game](#twitch-set-game) sub-action
*  Add ability to enable/disable all actions in a group from context menu
*  Block port 4444 from being used for **Streamer.bot's** own internal websocket server
*  Introduced a new option for commands, [Command Cooldown Action](#command-cooldown-action), check for more details
*  You can now drag sub-actions around to move them **this is still a bit experimental and might have some issues**
*  Ogg Vorbis is now a supported playback format for sound files
*  Commands now have a **Case Sensitive** option
*  Added C# methods for creating [Twitch Predictions](#twitch-predictions)
*  Add C# methods to enable/disable [Commands](#commands)
*  Added 2 new variables, `%createdAt%` and `%accountAge%` to the Get Target Info sub-action, accountAge will be given in seconds
*  Update [Twitch Polls](#twitch-polls) to be able to handle the `/endpoll` command (Poll Terminated action)
*  Add option to export actions to file
*  Add indicator to exporting to clipboard that it was successful
*  Add new context menu item when right clicking a user to perform some twitch actions, at the moment, just banning and adding/removing mod/vip status
*  New Set Command Group State sub-action
*  New Set Action Group State sub-action
*  Quote settings now shows all your quotes, and can be deleted, this is just the start of UI for quotes
*  Add ability to duplicate a group and all of it's sub-actions
*  When connecting to Twitch, your list of mods and vips are updated automatically
*  [Experimental Linux Support](#experimental-linux-support) **READ THIS SECTION FOR IMPORTANT INFORMATION**
*  Add new sub-action for enabling/disabling slow mode in your twitch channel
*  Add new sub-action for creating a clip, as well as a C# method. **NOTE, There is no control over the clip created, title, length, etc**
*  Add new sub-action for creating a stream marker, as well as a C# method; you can provide a description for the marker
* **Misc:** Update some libraries that are used
{.changelog-new}

<span></span>

## Hot Key Support
After much requesting, it's here, Global Hot Key support!  There is also a new sub-action to send keyboard presses! 

The keys you can use for creating a global hotkey are currently limited to keys that make sense, and can always be expanded.

The sub-action for keyboard presses, at the moment, is really meant for pressing global hot keys, and may evolve over time to be able to specify a specific window/application.

![sub-action-keyboard-press.png](/sub-action-keyboard-press.png)

## Perform Command
The **Perform Command** sub-action has had a bit of an overhaul to give you more options in setting up to run a command.

![sub-action-perform-command.01.png](/sub-action-perform-command.01.png)

The new additions allow you to set the working directory, the arguments to use (which supports variable replacement), as well as being able to set environment variables (also supporting variable replacement).

**Note:** *There was a bug in the old version where it could not run commands with arguments properly.*

For example, the following could be used for executing a python script.

| Property | Value |
|      ---:|-------|
| Command | `C:\Python27\pythonw.exe` |
| Working Directory | `C:\StreamStuff` |
| Arguments | `C:\StreamStuff\sub-printer.py` |

Environment Variables could be:

| Key | Value |
| ---:|-------|
| `USER` | `%user%` |
| `TIER` | `%tier%` |
| `MESSAGE` | `%message%` |

## ReadLinesFromFile and ReadRandomLinesFromFile
Read Line From sub-actions have options to now parse variables in the line read, and to auto-type instead of always adding as a string

![sub-action-readlinesfromfile-01.png](/sub-action-readlinesfromfile-01.png)

![sub-action-readrandomlinefromfile-01.png](/sub-action-readrandomlinefromfile-01.png)

## OBS Events
New with this version, you can now assign triggers to events that OBS transmits across the websocket connection.

![obs-events-01.png](/obs-events-01.png)

The data that an event emits, is added onto the arguents the same way it is with results from `OBS Raw`, as well as a `%obsEvent._json%` variable that can be parsed in C# (`JObject.Parse()`) for easier use.

OBS events are per-connection based.

## Confirmation Dialogs
When closing **Streamer.bot** you'll be prompted if you're sure you want to close, with the option of not asking again.

![close-prompt.png](/close-prompt.png)

When you delete an action, or a sub-action, you will be prompted to confirm the deletion, with the option of not asking again.

![delete-confirm.png](/delete-confirm.png)

You can reset these confirmations under the `User Interface` tab in `Settings`

## Twitch Predictions
Seems I missed adding in some variables to the completion event, unlike polls where a winner is determined by a fixed vote, predictions are resolved, and the broadcaster or a moderator pick the specific winner.

In addition, I added a `%prediction._json%` argument, which contains a JSON string of the event that can be parsed in C# (`JObject.Parse()`) for easier use.

| Value | Description |
|   ---:|-------------|
| `%prediction.winningIndex%` | Either a 0 or 1 depending on which outcome was chosen as the winner |
| `%prediction.winningOutcome.id%` | The ID of the winning outcome |
| `%prediction.winningOutcome.title%` | The title of the winning outcome |
| `%prediction.winningOutcome.users%` | How many users voted for this prediction |
| `%prediction.winningOutcome.points%` | The total number of channel points used by users |
| `%prediction.winningOutcome.color%` | The colour of the winning outcome |

### Prediction C# Methods
There are 4 new C# methods that can be used to create a prediction from C# code.

```csharp
string TwitchPredictionCreate(string title, string firstOption, string secondOption, int duration);
void TwitchPredictionCancel(string predictionId);
void TwitchPredictionLock(string predictionId);
void TwitchPredictionResolve(string predictionId, string winningId);
```

## Twitch Polls
Even tho a poll can technically end in a tie, I added the winning choice information into the arguments.

In addition, I added a `%poll._json%` argument, which contains a JSON string of the event that can be parsed in C# (`JObject.Parse()`) for easier use.

| Value | Description |
|   ---:|-------------|
| `%poll.winningIndex%` | The index of the winning choice, from 0 to 4 |
| `%poll.winningChoice.id%` | The ID of the winning choice |
| `%poll.winningChoice.title%` | The title of the winning choice |
| `%poll.winningChoice.votes%` | Number of regular votes |
| `%poll.winningChoice.bitVotes%` | Number of bit based votes |
| `%poll.winningChoice.rewardVotes%` | Number of channel point based votes |
| `%poll.winningChoice.totalVotes%` | Total number of votes for the choice |

### New Action
When using `/endpoll` in your chat to stop an active poll, its sent through as terminated, not completed; a new assignable action to the terminated event has been added.

## Commands
After seeing and hearing the feedback, commands got a bit of an overhaul.

To start with, something simple, when you add a new command, if you happened to right click on an existing command and picked add, the new command will be auto-set to the group of the selected command.  Right clicking add while on a group line itself, will also auto assign the group when adding a command.

You can now have multiple "commands" for a single command, also, Regex based input is supported.

> Regex comparisons can be heavy; even with the precompilations that exist for C#, they can become slow if the expression itself is not optimized.  There are no limits on how many you can create, but just be aware, every message that comes through is checked against all commands to see if any should be run.
{.is-warning}

The introduction of regex, is just simple at the moment, and may get a bit more complex afterwards (for example, regex capture groups being added as arguments)

One other thing to note, the `%rawInput%` variable for commands, specificially the **Start** location, auto strips the command from the start, at the moment, with a regex based command, it will behave like **Anywhere** and not remove the matched section(s), I may alter this slightly and add a 2nd variable that gives you both, one with, and one without, I'm unsure yet.

![commands-multi-01.png](/commands-multi-01.png)

![commands-regex-01.png](/commands-regex-01.png)

### Command C# Methods
Two new C# methods were added to be able to enable/disable a command.  Unlike other methods that only need a title, this requires the ID of the command, this can be retreived by right clicking on a command and selecting `Copy Command Id`

```csharp
void EnableCommand(string id);
void DisableCommand(string id);
```

## Command Cooldown Action
From the suggestion board, letting a user know that a command was on cooldown was requested, and instead of just hard coding this, I've added this as a configurable action instead.

A cooldown action can only trigger from a command that has a location of `Start` or `Exact`, regex based commands, or anywhere location will not trigger this action, even if it is on cooldown.

Also, only a `Message`, `Subscription` and `ReSubscription` can trigger a cooldown action.

There is a new column in the `Commands` list that shows the `Cooldown Action` associated with a command.

Available variables:

| Value | Description |
|   ---:|-------------|
| `%command%` | The command that was used |
| `%cooldownLeft%` | How many seconds are left for the cooldown, and is the maximum of the global and user cooldown left |
| `%globalCooldownLeft%` | How many seconds are left for the global cooldown of the command |
| `%userCooldownLeft%` | How many seconds are left for the user cooldown of the command |

There is also a new websocket event that can be subscribed to, `CooldownEvent` for `Commands`

![sub-action-commandcooldown-01.png](/sub-action-commandcooldown-01.png)

The most basic subaction you could add, would be a `Twitch Message` with the message `%user%, %command% is on cooldown for %cooldownLeft%s`

## Twitch Gift Sub Bomb/Gift Subs
In previous versions, when someone dropped a gift bomb (more then 2 gift subs in a single go), only the gift bomb event itself was triggered, and all associated gift sub events for it were silently discarded.

With this version, the gift subs are no longer discarded, they are now also sent, and there is an argument `%fromGiftBomb%` that will exist. If this is true, the sub is from a gift bomb, if false, its not.

I've also added `%subBombCount%` which will give the number of gift subs, if ths gift sub belongs to a gift bomb.

One last new argument is `%cumulativeMonths%`, this can have how many months the user receiving the gift sub has been subscribed for, if its 1, they are a new subscription, if its > 1, then its a resub.  There are chances where it can be 0 from what I've seen.  So this value could be used to welcome a new gifted subscriber.

## New Sub-Actions

### OBS Take Screenshot
Up until now, you had to use OBS Raw to take a screenshot in OBS, here is a sub-action ot make things a bit simpler.

![sub-action-obs-takescreenshot-01.png](/sub-action-obs-takescreenshot-01.png)

`Scene`, `Source` and `File Path` all support variable replacements, and after a screenshot is successfully taken, the full file path is added back onto the arguments as `%screenshotFile%`.

There is a new date time friendly variable that can be used, `%filedatetime%` which is of the format `yyyyMMdd.hhmmss`.

### OBS Set Audio Track State
With this sub-action you can alter which audio tracks a source can be active on

![sub-action-setaudiotrackstate-01.png](/sub-action-setaudiotrackstate-01.png)

> This sub-action ***requires*** obs-websocket version 4.9.1
{.is-info}

## OBS Set Media State
Control the state of media playback, you'll be able to `Play`, `Pause`, `Restart`, `Stop`, `Next`, `Previous` the specified media.

![sub-action-obs-setmediastate-01.png](/sub-action-obs-setmediastate-01.png)

The following C# methods were also added to control media via code.
```csharp
void ObsSetMediaState(string scene, string source, int state, int connection = 0);
void ObsMediaPlay(string scene, string source, int connection = 0);
void ObsMediaPause(string scene, string source, int connection = 0);
void ObsMediaRestart(string scene, string source, int connection = 0);
void ObsMediaStop(string scene, string source, int connection = 0);
void ObsMediaNext(string scene, string source, int connection = 0);
void ObsMediaPrevious(string scene, string source, int connection = 0);
```

## Twitch Set Channel Title
Using this sub-action, you'll be able to set the title of your channel, either to a fixed value, or using variables.

![sub-action-setchanneltitle-01.png](/sub-action-setchanneltitle-01.png)

The following C# method was also added to set your channel title via code.
```csharp
bool SetChannelTitle(string title);
```

An example action that you can assign to a `!title` command
```
TlM0RR+LCAAAAAAABACVVNmOm0gUfR9p/sGylLdgUSx2EykP3XTbhlYzwhuYoR9qA9MulrDYjaP8+xQQp7GtaBQsC7jn1rnnnuLW97//GgyGB5oXUZoMvwzA5zaQwJjyt+GSlvoOJgllq6hkdNihEJc8u+AJ/zbvg8H37sahiDTLFBWiAMhjQUUTRVDGgAp36hgKqiJTWVEIgEDuuNpF3ypaNeWSirGPKE0gYrThK/OKfsR72gY/xQ166tqcME+rrEny+NWLQ3aEdbGomlYDyIoebQ4Tksb3bWu3KE4TXOU5Tcpb7MaOC0valLLVx/V8yuHRSLKq/PShqmecLGp3QFMlYUwJERQZEgGKARYoVUQJUDIZg/HVwiONwl2jShyJl0hZZ01NoF6Gz95cuN1pSAh9b5g+oj8+/66l3jasDN7dghYVK6/EEVrgPMp+ejq8QveUZvcsOtAbT7sdoQHljmN6ZW0L6l983+GC02Ph+y8RztMiDcqR9bTy/WnOtR3TfO/7B2UkjmRRBprvxwVOcxahEWFs2Kd7vayL6pLqKWm7I66VoRiHa5mdyGxT/nMUnx/t7Egcs4DOS7iV3ndYfglt8GAsHZXHVMbxyaOdmni+idCMvRkz84CkY7hwd2wrb0RvGWYNTjmXbjNp6xohljdvW2lzwvW9ZjxZB5R4DCd2tZlpOpK0wnOm1fNsWnuyhYxkkZHZO1v/WmOS51Vh6eHeJPG0Nubmjois4vVF41EMt66ZYFBEOJ7KXOORuHbkLtU1ApaIY1Z5dZh1faWm7rDY0Hcn4lhvnmudnu1WY9sPvz+un8JqLW0q7wkwLFs7T1pzwFxDd1F4y4eT59ohmd2NjXlZb11iouQBkLkYnfUFHR9Dc4u1nG4X19eWvdTVleeo+5XDe5KmCfdpb7BNteVec24R1Wd+JqLZ+v9q1J67ADhWQjI3gddiTON7w//p16svMcspTuMsYr/5FAllsF6WML8d/970KjggGgKqcKdNVEGZUFFAeAIETCkKAsB/WPrT6dWa608HGPQG+Pz4en1gzRqadrRe++ccYzArKOmhHdgSdZndgX0Gf/wHhK9EBUQGAAA=
```

## Twitch Set Game
Using this sub-action, you'll be able to set the game for your channel, again using a fixed game that you can set from a list, or by using variables

![sub-action-setchannelgame-01.png](/sub-action-setchannelgame-01.png)

![sub-action-setchannelgame-02.png](/sub-action-setchannelgame-02.png)

The following C# methods were also added to set a game via code.
```csharp
GameInfo SetChannelGame(string game);
bool SetChannelGameById(string gameId);

public class GameInfo
{
		public int Id { get; set; }
		public string Name { get; set; }
		public string BoxArtUrl { get; set; }
}
```

An example aciton that you can assign to a `!game` command
```
TlM0RR+LCAAAAAAABACVVctu2kAU3VfqPyCk7mLkJ+DughPATuMUiG1wncW8MA7jR/2Amqr/3hkbBAF1UUsI5p65Z84913f4/flTp9PdkbyI0qT7tSPdNYEExIStugtSGhuQJIROeKQFASrZ5oLhP/i60/ndfjEowjwLA62P4AALfayqgirJQwGA/oAt+0ofaiKBUr/lapJ+VqTipyUVpecoSQCkhPOVeUXO8QtpnaO2zllcsyXM0yrje3z2XMQB3YO6mFe80DWgxQVrDhKcxvdNZbcoShNU5TlJylvsxo0PjjRbirTKERct3n2Ih8dSvuRgbyZZVX7p3m4wG0uvgNZnoKqqBpW1oANREVQVi4KuKKIwJAoZAl0fDofSVeKeROGGVyH2rsSUdcbFSP0rCUcvPzSn1ZBg8osznaN/7v5lwUXXeLPmpKhoeaUNkwLlUXZswXXJW0KyexrtyE0L2gaSNWENQuSqEw1ofA0Cj+lN90UQPEcoT4t0Xfbsx9cgGOdMzz7Nt0GwU3tiTxEVSQ+CuEBpTiPYw5R2L+nePp4L65IYKW6Kw0s7gzEKHYUe8MQtX/bi08Ms22PPKoD3HK7kXxukPIczaWQuPI3FNMrwwcMstdDUjeCEvpsTawflfThfbuhKcUV/EWYcJ4zLmFF5tTRDpLjvK9k9oPpeNx/tHUx8ipJZ5U50A8p64Xvj6mkyrn3FhmaMN9BzX7Fnv/tL+2BSMWt1pZbh0dg0NocT9jRrzmj0nM7y5XHpOxrjcMLvi9EGxfjg1Vay8iT6GjNsYeFvdL5zlHnN6kmejO0p/8F5DCtHdiv/UaJIsTe+7DDAmvJcc2pTbIxEeEhDIjcaX3h8vTAbfSxfbzW6BZId2wi3Rw+2Fo7HtTm1NlikFfNNNB/EcLW0EiQVEYrHCvN2j5ezaLnQHCjZIopp5dfhkXdrcf+/UZvCeG7zulcepgyIXE/LYawrMBo19b1Eo8GZb66b0bG2pdjoQbEr4qVVmdN5jT2nwdbMQ/65enuznKA0ziL6j9cXEwrqRQny2xvmYuA1fYg0HSCBQCIKKh6obODVgbCWIegrcA36ZPC/A6/z539nXrqY+dPPt+s7ccJpmnF8u7xKKQVZQfAF2oINUbuz/Us4gX/+AqlLhx2lBgAA
```

## Experimental Linux Support

> There is no guarentee this will work 100%, there are areas of the app that may not function correctly, so this will be a complete work in progress depending on time/effort.
{.is-warning}

It is possible to run this current version (**0.1.4**) using wine/wine64 within Linux

The entire network stack was re-written to make this possible, as it was a major blocker.

I've been doing some tests using the staging version of Wine, which is v6.19 in Ubuntu 20.04 LTS.

For your Wine setup, you'll want the following:
```
winetricks dotnet472
winetricks d3dcompiler_47
winetricks dxvk
```
You will also want to make sure gnutls (for 32-bit, lib32-gnutls).

This information should also apply to TwitchSpeaker, one area that will not work in TwitchSpeaker are SAPI5 voices, and the Azure voices may also not work. Again, this is very experimental.

A dedicated page on the wiki will likely be created for those who are using/testing it under Linux to list what works and what the current issues are.

> Running **Streamer.bot** and/or **TwitchSpeaker** under Linux is considered to be experimental, so expect bugs/issues.
{.is-warning}

# Archives
View changelogs for older releases{.subtitle}

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
{.btn-grid .my-5}