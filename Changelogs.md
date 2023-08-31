---
title: Changelogs
description: List of new features, bug fixes and improvements
published: true
date: 2023-08-31T00:39:16.715Z
tags: 
editor: markdown
dateCreated: 2021-08-25T21:51:24.140Z
---

# Streamer.bot v0.2.1 (WIP)
Upcoming changes in the next release!{.subtitle}

While 0.2.0 launch didn't go as smoothly as I had planned, after a quick fix it was off and running.  To follow up on that, 0.2.1 brings in some more fixes, and a couple of extras with it.

* Fix typos
* Fix crash in Test Trigger dialog, when clicking away from a cell with an empty value
* Fix `monthsGifted` being `any` in Twitch Gift Sub trigger test
* Fix issues with C# method `SetTwitchUsersVarById` and `SetYouTubeUserVarsById`
* Fix issues with C# method `GetUsersVar`
* Handle potential crash in VTubeStudio Trigger Hotkey sub-action dialog
* Handle potential crash in Twitch Gift Bomb handling
* Handle potential crash when editing a variable with auto-typing enabled
* Handle potential crash in CrowdControl Trigger dialogs
* Handle potential crash in Raid Start trigger test
* Handle potential crash in PerformCommand sub-action dialog when leaving a cell empty
* Handle potential crash in the Import Dialog when trying to exclude all actions/commands when there aren't any
* Handle potential crash in the `Twitch Reward Set Cooldown` sub-action
* Handle potential crash in `GetCredits` when BitLeaderboard API calls fail
* Handle potential crash in Twemoji Emote Handler
* Handle potential crash in OBS Websocket5 Version call
* Fix long startup times during DB upgrades
* Fix creation of a Midi Message trigger not saving the selected event correctly
* Handle potential crashes in OBS Websocket v4 and v5 handling
* Handle potential crash in `Write To File` sub-action when trying to write to a file user does not have permission to
* Fix UI interactions freezing the UI when connecting/disconnecting to/from various services
* Fix endless retry loop for Streamer.bot website integration when remote connection is disabled
* Fix UI feedback when connecting to VTubeStudio
* Handle potential crash in `Twitch Chat Message `trigger test
* Handle more potential crashes for Toast Notifications when trying to run on Windows 7, this is a Windows 10 and higher only feature
* Better handling of loading certain types on startup
* Handle potential crash in `CrowdControl TimedEffectUpdate` event
* Handle potential crash in `OBS GetSceneItemProperties` sub-action dialog
* Handle potential crash in Import Dialog with invalid data
* Potential crash in EventSub when a Rewards global cooldown is greater than int.MaxValue
* Handle potential crash in `Twitch Guest Star Guest Update` event
* Fix being able to make an empty query search for Twitch Game Categories
* Handle potential crash in Global Variable Viewer when encountering empty-named variables
* Handle potential crash in `YouTube Gift Membership Received` trigger test
* Fix `Process Started/Stopped` Trigger display not showing the criteria
* Fix issue with non-blocking queue and Execute Code sub-actions
* Fix all `Patreon Trigger` tests crashing
{.changelog-fixes}

<span></span>

* Remove range restriction check on posX and posY in C# method VTubeStudioMoveModel
* Add various checks throughout setting uaser globals to prevent empty or null user ids
* When subscribing to EventSub subscriptions, no longer subscribe to all if Broadcaster account is not Affiliate or Partner
* Optimize C# method `SetTwitchUsersVarById` and `SetYouTubeUsersVarsById`
* Optimize C# method `GetUsersVar`, it runs much faster depending on the circumstances
* Tweaks to Elgato Wave Link integration
* Tweaks to OBS Websocket5 library
* In the import dialog, don't show exclude all from import, if there are no actions or commands to import
* Add address/port checks when connecting to VTubeStudio
* Add address/port checks when connecting to Streamlabs Desktop
* Prevent logging of VTubeStudio auth data
* `Toast Notification Activation` trigger now adds the original toast information to the arguments
* Tweaks to Twitch VIP handling
* Tweaks to Sub-action and Trigger item locations and sorting
* Rename `Perform Command` to `Run a Program`
* Add `isSubscribed` back for YouTube users
* Better handling of VTubeStudio and timing out requests so they don't get stuck
* Add checks to VTubeStudio Raw for `undefined` json values
* Twitch Reward global cooldown updated from int to long, this will effect the C# method `UpdateRewardCooldown`
* Update GetQuote sub-action to accept `%variables%`
* Update Get/Set Command State sub-actions to display the command's name instead of the command
* Update `Twitch Timeout User` sub-action to have similar fields as the `Twitch Unban User` sub-action
* Perform config upgrage on Twitch Timeout User sub-action to new format, be sure to check your timeout sub-actions!
{.changelog-updates}

<span></span>

* Add setting to commands to ignore internally parsed messages
* Add StreamElements connected/disconnected triggers
* Add Streamlabs connected/disconnected triggers
* Add 7 new triggers for Twitch connections
* Add a clear button for the action filter
* Add nerw VTubeStudioEvent `TrackingStatusChanged`, and accompanying trigger
* Add new C# method `UnsetAllUsersVar`, this will unset the specified variable for all users
* Add 4 new triggers for BetterTTV and SevenTV Adding/Removeing emotes
* Add `Create` button to various triggers
* Add delete confirmation when deleting a sub-action group
* Add 3 new C# methods for interactiong with quotes
* Add IgnoreAliases setting to GetCommands sub-action, this will return the first command only for each command if enabled
* Add new Trigger, `Global Variable Updated`
{.changelog-new}

## Global User Variables
A note about `SetTwitchUsersVarById` and `SetYouTubeUsersVarsById`, these 2 C# methods are completely broken in **0.2.0** and should not be used, they will set all the variables for the users specified to the value passed.

## New C# Methods
```cs
void UnsetAllUsersVar(string varName, bool persisted = true);
```
```cs
QuoteData GetQuote(int quoteId);
int GetQuoteCount();
bool DeleteQuote(int quoteId);
```
The `QuoteData` class
```cs
public class QuoteData
{
    public DateTime Timestamp { get; set; }
    public int Id { get; set; }
    public string UserId { get; set; }
    public string User { get; set; }
    public string Platform { get; set; }
    public string GameId { get; set; }
    public string GameName { get; set; }
    public string Quote { get; set; }
}
```
# Streamer.bot v0.2.0 (Current)
 Released 2023-08-23{.subtitle}

What's this, an actual version bump, or at least a minor one!  This changelog is still a work in progres, there is a lot of data I need to sort through, as some has already been included in past releases.

![sb-0.2.0-001.png](/sb-0.2.0-001.png)

* Misc fixes and tweaks throughout
* Fix 7TV emotes not being parsed
* Fixes to shutdown routines
* Fix some threads not being stopped properly
* Fix maximum for Twitch Sub-counter Rollover, it's now 32,767 (from 100)
* Fix data validation in Twitch Prediction dialog
* Fix data validation in Twitch Poll dialog
* Fix Twitch EventSub related issues, potential duplicate events
* Fix Handling of DoActions across various methods to parse properly for C#
* Fix Global Variable, and GLobal User variables
* Fix FFZ emote url
* Fix potential crash in LumiaStream's Set Color sub-action
* When editing an Action Queue, Blocking was not being updated in the UI
* Fixes to bottom right status indicator and potential crashes
* Fix Twitch Broadcaster account sometimes being unflagged as broadcaster
* Fix Twitch Timeout and Ban User methods not working correctly
* Clearing confirmation dialog settings did not clear quote deletion confirmation
* Fix potential crash in Set Queue Pause State sub-actions
* Fix potential crash during shutdown of some services
* Fix potential crash in Set Action Queue State
* Fix PlaySoundFromFolder sub-action, was possible for no audio device to be selected
* Fix crash when deleting multiple actions
* Fix potential crash in Twitch EventSub library when deserializing events
* Fix potential crash in Http Service
* Fix potential crash when an action is completed
* Fix some unhandled exceptions in Streamer.bot Website Integration
* Set a minimum size for the sub-action panel on the actions tab
* Fix potential crashes related to Twitch Predictions
* Fix potential parsing error when assigning a weight value to a sub-action
* Some fixes to general OAuth authentication
* Handle a potential crash in OBS Set GDI Text sub-action dialog
* Handle a potential crash in SLOBS Set Random Filter State sub-action dialog
* Fix potential crash when getting version information of an OBS connection
* Handle potential null ref in the OBS service when a scene is changed
* Handle a potential null ref during the creation of an Execute C# Code
* Handle potential null ref when sending an ActionCompleted event to the Websocket
* Handle potential crash when a Twitch Reward Redemption is updated
* Fix changing log level not correctly setting log level for some libraries
* Fix wrong action being picked in a random action group, where there are multiple and all are disabled but 1
* Fix isSubscribed variable in arguments for Twitch users
* Fix auto-selection of newly added action
* Fix potential crash when receiving a Twitch Ad Event
* Fix potential crash in ReadRandomLinesFromFile sub-action dialog
* Handle potential crashes in MidiOut Generic sub-action dialog
* Handle potential crash in SLOBS when getting source filter list
* Fix Subscriber group in command grounds for Twitch users
* YouTube connection UI could enter a bad state from auto connect if tokens are invalid
* Fix issue with Twitch EventSub and multiple instances of Streamer.bot using the same Broadcaster account
* Handle possible crash in custom C# code when Dispose() is overridden and user code throws
* Handle potential crash in Read From File sub-actions when parsing invalid paths
* Handle potential crash in Write To File sub-action when parsing invalid paths
* Finally fix the removal of the Broadcaster flag for the Twitch broadcaster account
* Fix deletion of None group in Actions tab
* Fix deletion of None group in Commands tab
* Fix selection of duplicated action
* Fix multi-trigger commands not picking the correct command
{.changelog-fixes}

<span></span>

* Update how events are handled internally
* Tweaks to LiteDB handling
* Tweaks to Credits for Twitch, should add presence for any event now
* Add some more logging during shutdown
* Change how shutdown works from an update
* Add url check to Websocket Client creation
* Add Twitch Bot information (if available) to Websocket `GetBroadcaster` method
* Allow !commands on internal Twitch message parsing, this means !commands typed in the inline chat will work
* For those running a prerelease build (beta, or alpha), your logging will be automatically pushed to verbose
* Update how [Export](#import-export) works
* Update [Import](#import-export) to handle new features, and give it a new UI with new interactions
* Commands that are disabled will now show as red in the main window
* Add validation checks to Midi Note On sub-action
* Update Speak sub-action to allow variable support for alias
* Update how commands are stored internally
* Enable the vertical scrollbar for the command text box in the command dialog
* Better handling of shutting down the OBS Service
* Tweaks to startup procedures
* Update handling of inline variable parsing
* Add Twitch and YouTube bot information to the HTTP GetBroadcaster call
* Have the Streamer.bot tray icon always visible
* Tweaks to sub-action categories
* Update Twitch EventSub with changes to Guest Star
* Update Discord Basic Webhook sub-action to support URLs for images
{.changelog-updates}

<span></span>

* Add new sub-action to set action queue's blocking state
* Add new sub-action to set a Twitch Reward's background color
* Add C# method to update a Twitch Reward's background color
* Add new sub-action Twitch Reply To Message
* Add new C# Method, TwitchReplyToMessage
* Actions will now show red when disabled
* [Triggers](#triggers)!
* New C# methods for Triggers
* [VTube Studio](#vtube-studio) Integration!
* A new [Global Variables Viewer](#global-variables-viewer)
* New [Inline Chat Window](#inline-chat-window) feature, see Twitch and YouTube chat within **Streamer.bot**
* Add list of users gifted a sub in the Twitch Gift Bomb event
* Add support for Twitch's new Hype Chat
* Add new [Websocket request](#new-websocket-requests), `ExecuteCodeTrigger`
* Add new [Websocket request](#new-webcosket-requests), `GetCodeTriggers`
* [CrowdControl 2.0](#crowdcontrol-20) Integration!
* [Elgato Wave Link](#elgate-wave-link) Integration!
* Add new [YouTube Bot](#youtube-bot-account) account
* Add new [C# Method](#new-c-methods), ObsSendBatchRaw
* Add new [C# Methods](#new-c-methods) for using User global variables
* Add new [C# Methods](#new-c-methods) for retrieving Twitch User information
* Split out Third Party Emote Handling
* Add support for SevenTV's real-time emote updates
* Add support for BetterTTV's real-time emote updates
* Add new Important Information popup, when a new release happens, I'll be able to relay information that must be seen, only once at startup
* Add a startup splash screen
* Add new [`~globalVariable~`](#inline-global-accessor) accessor to variables
* Add new sub-action, Tray Notification, this will allow you to create a custom tray notification from the Streamer.bot tray icon
* Add new sub-action, Set Voice Control Input, allowing you to change which Input device Voice Control is using
* Add 2 new C# methods for adding a quote
* Add 2 new sub-actions, Reset Credits and Reset First Words
{.changelog-new}

## Triggers
Gone are the days of having to move through multiple tabs to assign an action to an event.

Now, you assign a Trigger directly to one or more actions that act on events.

There are currently **166** different Triggers available in **Streamer.bot**, and there will probably be more!

When upgrading from **0.1.22**, all your events that you have actions associated with, will be upgraded automatically to Triggers.

As you are using triggers, much like sub-actions, you will be able to favorite the ones you use the most by right clicking on the trigger within the menu.

Want an overview of triggers used, and which actions have them.  Within the main window, above the trigger list, there is a `?`, clicking this will open the trigger viewer, where you can see a full overview of triggers in use.  **Note** This window does not update in realtime, and requires a manual refresh if changes are made while it's open.

Also at the top of the triggers list, is a `+`, this will allow you to add triggers to the selected action.

Triggers that are disabled, will be shown as red in the list, and triggers that have the `Always Run` option set, will be shown as blue

### Behavior
This is the behaviour for triggers, when there is a mix of Any, and Range based, or other criteria based.

The behavior is as follows, for an `event`.

If a `Trigger` has a `Min/Max`, it will get all the `exact` matches, if there are none, then it will try to get the `range` matches, if there are still none, then it will get `any` matches.

If a `Trigger` is `editable`, but not a `Min/Max`, it will get a count of `Any`, and if there is a `disparity`, i.e., there is 1 Any, but say 4 with a Criteria, it will only use those with a `Criteria`

In addition to the above, you can `flag` certain Triggers to `Always Run`, this flag is only available on `editable` triggers. Once either of the two are checked, it will add any Always Run triggers, and proceed to use that list of Triggers

If neither of the two above are met, then it will just run all the triggers for the event.

### Custom Triggers
Not only are there Triggers for fixed events within **Streamer.bot**, but you'll also be able to create your own named triggers within the UI as will as in C#.  Both of which can be triggered within C#.

If you use the Custom trigger within the UI, just enter any name, and you can trigger it within C# using the following:
```cs
// the name, useArgs is a boolean that if true, will forward the args of the action to the trigger
CPH.TriggerEvent("whatever you named it in the UI");
```
To register a custom trigger in C#, that will show up in the Custom menu, use the following:
```cs
// Name, event name, and categories it sits in
CPH.RegisterCustomTrigger("Something", "mine_something", new[] { "Stuff" });
```
And to trigger it within your code:
```cs
CPH.TriggerCodeEvent("mine_something");
```
Typically you would register a trigger in the `void Init()`method, and have it compile at start 

### New Triggers
There are a couple new Triggers, that previously did not exist as events within **Streamer.bot**

#### Process Started
Trigger an action when a process has started on your PC

#### Process Stopped
Trigger an action when a process has stopped on your PC

### Other New Triggers
A general list of new events that are available through triggers

* OBS Scene Changed
* YouTube New Subscriber (handled via StreamElements)
* OBS Streaming Started
* OBS Streaming Stopped
* OBS Recording Started
* OBS Recording Stopped
{.grid-list}

## VTube Studio
A brand new integration is coming to **v0.2.0**, and that's VTube Studio!

You'll be able to react to some events from VTube Studio, as well as 5 new sub-actions to interact with it.

There are also a handful of C# methods, for those that prefer to write C# code for there actions.

### New Sub-actions
The following sub-actions are available for use with VTube Studio
* Load Model
* Load Model by Name
* Trigger Hotkey
* Trigger Hotkey by Name
* Move Model
* Color Tint
* Remove All Color Tints
* Set Expression State
{.grid-list}

### New C# Methods for VTubeStudio
```cs
bool VTubeStudioLoadModelById(string modelId);
bool VTubeStudioLoadModelByName(string modelName);
bool VTubeStudioTriggerHotkeyById(string hotkeyId);
bool VTubeStudioTriggerHotkeyByName(string hotkeyName);
bool VTubeStudioMoveModel(double seconds, bool relative, double? posX = null, double? posY = null, double? rotation = null, double? size = null);
bool VTubeStudioRandomColorTint();
bool VTubeStudioResetAllColorTints();
bool VTubeStudioColorTintAll(string hexColor, double mixWithSceneLighting = 0);
bool VTubeStudioColorTintByNumber(string hexColor, double mixWithSceneLighting, List<int> artMeshNumbers);
bool VTubeStudioColorTintByNames(string hexColor, double mixWithSceneLighting, List<string> filterValues);
bool VTubeStudioColorTintByNameContains(string hexColor, double mixWithSceneLighting, List<string> filterValues);
bool VTubeStudioColorTintByTags(string hexColor, double mixWithSceneLighting, List<string> filterValues);
bool VTubeStudioColorTintByTagContains(string hexColor, double mixWithSceneLighting, List<string> filterValues);
bool VTubeStudioActivateExpression(string expressionFile);
bool VTubeStudioDeactivateExpression(string expressionFile);
VTSModelPosition VTubeStudioGetModelPosition();
string VTubeStudioSendRawRequest(string requestType, string data);
```
```cs
public class VTSModelPosition
{
	public double PositionX { get; set; }
	public double PositionY { get; set; }
	public double Rotation { get; set; }
	public double Size { get; set; }
}
```

## CrowdControl 2.0
Yes, that's right, yet another integration, and this time it's CrowdControl 2.0!

With this integration, you can now react to 8 different events from CrowdControl.

Since CrowdControl themselves are still developing this version, there are things within **Streamer.bot** that can change as well, and new features are still pending.

## Elgato Wave Link
Yep, another integration, this time its Elgato Wave Link!  Control, and react to changes in Wave Link from within **Streamer.bot**

New triggers:
* Connected
* Disconnected
* Output Switched
* Output Volume Changed
* Output Mut CHanged
* Selected Output Changed
* Input Volume Changed
* Input Mute Changed
* Input Name Changed
* Microphone Gain Changed
* Microphone Output Volume Changed
* Microphone Balance Changed
* Microphone Setting Changed
* Filter Added
* Filter Changed
* Filter Deleted
* Filter Bypass State Changed
{.grid-list}

New sub-actions:
* Mute Microphone
* Mute Output
* Mute Input
* Set Bypass Filter State
* Set Filter State
* Set Output Monitor Device
* Get Selected Output
* Set Output Volume
* Get Output Volumes
* Set Input Volume
* Get Input Information
* Get Microphone Information
* Set Microphone Gain
* Set Microphone Output Volume
* Set Microphone Balance
* Get Filter State
{.grid-list}

### New C# Methods
In addition to new sub-actions and trigger, there are also a handful (24 to be exact) new C# methods for interacting with Elgato Wave Link
```cs
void WaveLinkOutputMute(string mixer);
void WaveLinkOutputUnmute(string mixer);
void WaveLinkOutputToggleMute(string mixer);
void WaveLinkSetOutputVolume(string mixer, int volume);
string WaveLinkGetMicrophoneIdentifier(string microphoneName);
void WaveLinkMicrophoneMute(string microphoneIdentifier);
void WaveLinkMicrophoneUnmute(string microphoneIdentifier);
void WaveLinkMicrophoneToggleMute(string microphoneIdentifier);
void WaveLinkMicrophoneSetVolume(string microphoneIdentifier, double volume);
double WaveLinkMicrophoneGetVolume(string microphoneIdentifier);
string WaveLinkGetInputIdentifier(string inputName);
void WaveLinkInputMute(string identifier, string mixer);
void WaveLinkInputUnmute(string identifier, string mixer);
void WaveLinkInputToggleMute(string identifier, string mixer);
void WaveLinkInputSetVolume(string inputIdentifier, string mixer, int volume);
long WaveLinkInputGetVolume(string inputIdentifier, string mixer);
void WaveLinkInputFilterBypassBypassed(string inputIdentifier, string mixer);
void WaveLinkInputFilterBypassEnabled(string inputIdentifier, string mixer);
void WaveLinkInputFilterBypassToggle(string inputIdentifier, string mixer);
string WaveLinkInputGetFilterIdentifier(string inputIdentifier, string filterName);
void WaveLinkInputFilterEnable(string inputIdentifier, string filterIdentifier);
void WaveLinkInputFilterDisable(string inputIdentifier, string filterIdentifier);
void WaveLinkInputFilterToggle(string inputIdentifier, string filterIdentifier);
bool WaveLinkInputGetFilterState(string inputIdentifier, string filterIdentifier);
```

## YouTube Bot Account
Yes, I've heard you, and I was finally able to figure out the best way to handle this.

Starting with **0.2.0** you can setup a bot account for YouTube, and use this as the mouth piece for talking to chat.  The YouTube send message sub-action has been udpated, as well as the C# methods.

## Import/Export
How you export actions and command has changed with **0.2.0**, no longer do you havhe to scroll through a list to select the actions you want.  Now, you can just right click on an action, and use the `Add to Export` or `Remove from Export` menu items.  Best of all, the Export window is no longer modal, which means you can keep it open off to the side, as you add your actions and commands and see it populate.  THere is also new information you can attach to an export, such as author, description and a version.

The Import window has also changed to accomodate the new data that's available with exports from **0.2.0**, but don't worry, it will still accept imports from older versions.

Importing will also properly handle new triggers, as well as updating certain data in old exports to the new trigger system.

New with the Import system, you'll be able to overwrite commands and actions, this is primarily for exports from **0.2.0**, as legacy exports altered ids, so matching them correctly is not possible. When you're presented with actions and commands to import, you can right click on an action  or a command, and include/exclude it, if its an exact match to an existing action or command, you can also flag it to be overwritten or not.

## Global Variables Viewer
Ever wonder what global variables are floating around **Streamer.bot**? will, now you can see them, and see them update in realtime with a Global Variable viewer.

In addition to seeing them, you can add new ones, edit existing ones, and even outright delete them.

## Inline Chat Window
Open up a window, and view your Twitch, and/or YouTube chat, right within **Streamer.bot** itself!

## Inline Global Accessor
You can now use `~` to access global variables directly. They will be replaced with the global variable value, if it exists at the time of parsing.

## New C# Methods
```cs
bool UpdateRewardBackgroundColor(string rewardId, string backgroundColor);
bool UpdateReward(string rewardId, string title = null, string prompt = null, int? cost = null, string backroundColor = null);
```
```cs
void TwitchReplyToMessage(string message, string replyId, bool bot = true);
```
```cs
string ObsSendBatchRaw(string data, bool haltOnFailure = false, int executionType = 0, int connectionIdx = 0);
```
```cs
void SetTwitchUserVarById(string userId, string varName, object value, bool persisted = true);
void SetYouTubeUserVarById(string userId, string varName, object value, bool persisted = true);

void SetTwitchUsersVarById(List<string> userIds, string varName, object value, bool persisted = true);
void SetYouTubeUsersVarById(List<string> userIds, string varName, object value, bool persisted = true);

void UnsetTwitchUserVarById(string userId, string varName, bool persisted = true);
void UnsetYouTubeUserVarById(string userId, string varName, bool persisted = true);

void UnsetTwitchUserById(string userId, bool persisted = true);
void UnsetYouTubeUserById(string userId, bool persisted = true);

T GetTwitchUserVarById<T>(string userId, string varName, bool persisted = true);
T GetYouTubeUserVarById<T>(string userId, string varName, bool persisted = true);

List<UserVariableValue<T>> GetTwitchUsersVar<T>(string varName, bool persisted = true);
List<UserVariableValue<T>> GetYouTubeUsersVar<T>(string varName, bool persisted = true);
```
```cs
public class UserVariableValue<T>
{
	public string UserId { get; set; }
	public string UserLogin { get; set; }
	public string UserName { get; set; }

	public string VariableName { get; set; }
	public T Value { get; set; }

	public DateTime LastWrite { get; set; }
}
```

```cs
TwitchUserInfo TwitchGetBroadcaster();
TwitchUserInfo TwitchGetUserInfoById(string userId);
TwitchUserInfo TwitchGetUserInfoByLogin(string userLogin);
TwitchUserInfoEx TwitchGetExtendedUserInfoById(string userId);
TwitchUserInfoEx TwitchGetExtendedUserInfoByLogin(string userLogin);
```
```cs
public class TwitchUserInfo
{
	public string UserName { get; set; }
	public string UserLogin { get; set; }
	public string UserId { get; set; }

	public DateTime LastActive { get; set; }
	public DateTime PreviousActive { get; set; }
	public bool IsSubscribed { get; set; }
	public string SubscriptionTier { get; set; }

	public bool IsModerator { get; set; }
	public bool IsVip { get; set; }
}
```
```cs
public class TwitchUserInfoEx
{
	public string UserName { get; set; }
	public string UserLogin { get; set; }
	public string UserId { get; set; }
	public string Description { get; set; }
	public string ProfileImageUrl { get; set; }
	public string UserType { get; set; }
	public bool IsPartner => string.Equals(UserType, "partner", StringComparison.OrdinalIgnoreCase);

	public bool IsAffiliate => string.Equals(UserType, "affiliate", StringComparison.OrdinalIgnoreCase);

	public bool IsFollowing { get; set; }
	public DateTime LastActive { get; set; }
	public DateTime PreviousActive { get; set; }
	public bool IsSubscribed { get; set; }
	public string SubscriptionTier { get; set; }

	public bool IsModerator { get; set; }
	public bool IsVip { get; set; }

	public DateTime CreatedAt { get; set; }
	public double AccountAge { get; set; }

	public string Game { get; set; }
	public string GameId { get; set; }

	public string ChannelTitle { get; set; }

	public List<string> Tags { get; set; }
}
```
```cs
void ShowToastNotification(string title, string message, string attribution = null, string iconPath = null);
void ShowToastNotification(string id, string title, string message, string attribution = null, string iconPath = null);
```
```cs
int AddQuoteForTwitch(string userId, string quote, bool captureGame = false);
int AddQuoteForYouTube(string userId, string quote);
```
## New Websocket Requests
The new `ExecuteCodeTrigger` WebSocket method will let you trigger a Custom Code Trigger by using this method in a WebSocket connection. The format of the request is as follows.
```js
{
	"method": "ExecuteCodeTrigger",
	"eventName": "<registered name of event>",
	"args": {
		"id": "<someid>"
	}
}
```


# Streamer.bot v0.1.22 (Current)
Released 2023-05-31{.subtitle}

* Fix Twitch authentication error (non-critical), caused by additional scope request.
{.changelog-fixes}

This is a hot-fix for 0.1.21 to fix a non-critical (workarounds were available) issue with Twitch Authentication, and requesting new scopes.  Seems I forgot to apply a change after updating the status indicator to still show the Twitch Broadcaster/Bot status after new scopes are required.

# Streamer.bot v0.1.21
Released 2023-05-31{.subtitle}

* General tweaks/fixes
* Fixes for some Stream deck sub-actions
* Fix some dialog text
* Update Twitch Goal Progress event to check if the goal has reached the target, and also send an End event
* Fix for Twitch out of order gift bomb/sub events
* Fix handling of clearing a queue
* Fix crash with VoiceMod and non-expected results
{.changelog-fixes}

<span></span>

* Update shared libraries
* Temporarily add T or YT after user's name in Command Dialog permissions
* Update Stream Deck sub-actions to allow variables in the Button ID
* Tweaks to Twitch's Broadcaster/Bot status indicators
* Add error handling to Execute C# Copy compiler log to clipboard
* Add error handling surrounding Execute C# Code's Init() method
* Test button for Twitch Raid broadcasts across the websocket again
{.changelog-updates}

<span></span>

* New [Stream Deck Plugin](https://streamdeck.streamer.bot)
* Request new Twitch scope, `channel:manage:guest_star`
* Add support for [Twitch Guest Star](#twitch-guest-star) events
* Add new sub-actions for [Twitch Guest Star](#twitch-guest-star) API calls
* Add new [C# Methods](#new-c-methods) for Stream Deck
* Add new [Labs](@labs) settings page
* Add new Action Queue type, see [Labs](#labs)
* Add a new Twitch Add Present User sub-action
{.changelog-new}

## Labs
With this release, to give users a chance to try new features before they're ready, with the knowledge, that they are 100% experimental, I've added a new Labs page.

### New Action Queue
The first experimental feature is an updated Action Queue, to enable this, just click the check box and restart **Streamer.bot**.  The underlying code for this new action queue uses a different container type, and is a bit easier to maintain and manage.  There is the possibility of lower CPU usage with many queues.

Be sure to give this a try, so it can be promoted to the next version sooner.

## Twitch out-of-order Gift Bomb/Sub events
I have updated the handling of gift subs and community gifting events.

Internally these are now cached, and can be associated with the respective IDs if they happen to come out of order from Twitch's IRC server.

If a single gift sub comes in, it should be handled appropriately and still fire an event for it, however, there will be a small 500ms delay, as a byproduct of this caching.

## New C# Methods
### New Methods for Stream Deck
```csharp
void StreamDeckSetBackgroundColor(string buttonId, string color);
void StreamDeckSetBackgroundColor(string buttonId, string color, int state);
void StreamDeckSetBackgroundUrl(string buttonId, string imageUrl);
void StreamDeckSetBackgroundUrl(string buttonId, string imageUrl, string color);
void StreamDeckSetBackgroundUrl(string buttonId, string imageUrl, int state);
void StreamDeckSetBackgroundUrl(string buttonId, string imageUrl, string color, int state);
void StreamDeckSetBackgroundLocal(string buttonId, string imageFile);
void StreamDeckSetBackgroundLocal(string buttonId, string imageFile, string color);
void StreamDeckSetBackgroundLocal(string buttonId, string imageFile, int state);
void StreamDeckSetBackgroundLocal(string buttonId, string imageFile, string color, int state);
void StreamDeckSetTitle(string buttonId, string title);
void StreamDeckSetTitle(string buttonId, string title, int state);
void StreamDeckSetState(string buttonId, int state);
void StreamDeckSetValue(string buttonId, string value);
void StreamDeckShowAlert(string buttonId);
void StreamDeckShowOk(string buttonId);
void StreamDeckToggleState(string buttonId);
```

### New Methods for Twitch Guest Star
```csharp
GuestStarSettings TwitchGetChannelGuestStarSettings();
bool TwitchUpdateChannelGuestStarSettings(bool? isModeratorSendLiveEnabled = null, int? slotCount = null, bool? isBrowserSourceAudioEnabled = null, string groupLayout = null, bool? regeneratgeBrowserSource = null);
GuestSession TwitchGetGuestStarSession();
GuestSession TwitchCreateGuestStarSession();
GuestSession TwitchEndGuestStarSession();
List<GuestStarInvite> TwitchGetGuestStarInvites();
bool TwitchSendGuestStarInvite(string userLogin);
bool TwitchDeleteGuestStarInvite(string userLogin);
bool TwitchAssignGuestStarSlot(string userLogin, int slot);
bool TwitchUpdateGuestStarSlot(int sourceSlot, int destinationSlot);
bool TwitchDeleteGuestStarSlot(string userLogin, int slot);
bool TwitchUpdateGuestStarSlotSettings(int slotId, bool? isAudioEnabled = null, bool? isVideoEnabled = null, bool? isLive = null, int? volume = null);
```

Supporting return classes
```csharp
public class GuestStarSettings
{
    public bool IsModeratorSendLiveEnabled { get; set; }
    public int SlotCount { get; set; }
    public bool IsBrowserSourceAudioEnabled { get; set; }
    public string GroupLayout { get; set; }
    public string BrowserSourceToken { get; set; }
}

public class GuestSession
{
    public string Id { get; set; }
    public List<GuestStar> Guests { get; set; }
}

public class GuestStar
{
    public string SlotId { get; set; }
    public bool IsLive { get; set; }
    public string UserId { get; set; }
    public string UserName { get; set; }
    public string UserLogin { get; set; }
    public int Volume { get; set; }
    public DateTime AssignedAt { get; set; }
    public MediaSettings AudioSettings { get; set; }
    public MediaSettings VideoSettings { get; set; }
}

public class MediaSettings
{
    public bool IsHostEnabled { get; set; }
    public bool IsGuestEnabled { get; set; }
    public bool IsAvailable { get; set; }
}

public class GuestStarInvite
{
    public string UserId { get; set; }
    public DateTime InvitedAt { get; set; }
    public string Status { get; set; }
    public bool IsVideoEnabled { get; set; }
    public bool IsAudioEnabled { get; set; }
    public bool IsVideoAvailable { get; set; }
    public bool IsAudioAvailable { get; set; }
}
```

## Stream Deck Plugin

Official plugin and documentation available at [https://streamdeck.streamer.bot](https://streamdeck.streamer.bot)

## Twitch Guest Star
Added subscriptions to listen to the new Twitch Guest Start EventSub subscriptions.

Added 12 new sub-actions to let the streamer interact with the new API methods for managing the Guest Star feature.

## Twitch Scopes
Requesting the following new scopes for the broadcaster account
* `channel:manage:guest_star`
{.grid-list}

# Streamer.bot v0.1.20
Released 2023-05-10{.subtitle}

* Misc tweaks/fixes
* Fix GetCommands sub-action, had an underlying change that wasn't fully propogated
* Update Read Random Line From File to not potentially crash
* Fix Read Specific Line From File to use an indexed variable if it already exists
* Fix TipeeeStream dialog text
* Fix Set Action Group State, should show correct enabled/disabled
* Fix C# Twitch Reward Group methods, they should affect pausing now, not enabled
* Fix Reward Set Group Paused State, should show paused/unpaused correctly now
* Fix crash in File Change event when file > 50kb
* Tweak tray icon text, there's now a limit of 128 characters, from 64
* Fix Get Commands Subaction, could add a new one with no variable
* Fix missing `__source` variable for Twitch Poll and Prediction events
* Fix missing `__source` variable for StreamElements events
* Fix profile image url in Twitch Raid start/send events
{.changelog-fixes}

<span></span>

* Switch Twitch Raid event to EventSub
* Update Twitch EventSub connection URL
* HotKeyPress event was missing the `__source` value
* When an action or group is set to random, ignore comments and disabled sub-actions when picking
* Add `obs.id` to OBS Event arguments
* Add `isFollowing` variable for `Twitch Add Follow Age Info` sub-action
* Add `targetIsFollowing` variable for `Twitch Add Target Info` sub-action
* For the Twitch Create Clip sub-action, updated `createClipUrl` to be the URL friendly URL for the clip, and added `createClipEmbedUrl ` that will contain the embed url
{.changelog-updates}

<span></span>

* Add new C# Method, LogError
* Add new feature set to support new Stream Deck plugin
* Add new test method for Twitch Raids
* Add an AutoType option to the `Logic If` sub-action
{.changelog-new}

## Stream Deck Plugin
Yes, you heard that right, there is a new Stream Deck plugin in the works, and will be released some time after this update, so there are features and settings available with this version to support the update.

More details will follow

## Important Notes for Twitch

> As of May 15th, 2023, Twitch is updating the EventSub URL, and moving it out of beta, this means that any versions prior to this will not connect to Twitch's EventSub
{.is-warning}

# Streamer.bot v0.1.19
Released 2023-03-10{.subtitle}

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

# Streamer.bot v0.1.18
Released 2023-02-22{.subtitle}

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

# Streamer.bot v0.1.17
Released 2023-01-20{.subtitle}

* Fix some typos
* CPH Method, EnableTimer was not correctly resetting a timer
* SetTimerState sub-action was not correctly resetting a timer's line counts
* Regression, was not listening for Twitch Community Goal events
* Issue with collapsing all action groups
* Disable OK button in Set Argument sub-action dialog when loaded, so it gets validated properly
* Fix Twitch HypeTrain end event, was missing `%contributors%` variable
* Fix command group collapsing
* Fix initial collapsed states of Command Groups
* Fix initial collapsed states of Twitch Reward Groups
* Fix start raid C# method
{.changelog-fixes}

<span></span>

* Twitch User IDs are now string across the entire application
* Twitch Channel Shield Mode EventSub events are out of beta, updated this internally
* Twitch Charity Donation event now includes the id of the donation, this has been added as a new arg `%donationId%`
* Updated Twitch `Add Target Info` to include tags
* YouTube based events have a `%broadcastId%` variable now
* Events that add primary user information, now have a `%userPreviousActive%` variable
* StreamElements, linked the YouTube provider events
* Harden file saving routines
* Move Twitch Channel Reward counters to the twitch data db file
* Improvements to the auto-updater, cancellation support and timeout.  **NOTE** This won't be useable until the **next** update.
* Disable and remove Twitch Coin Cheer events, since Twitch halted this experiment October 2022
* Enabled, Disable, Pause and Unpause Twitch Reward group context menu items no longer waits for each API call
* Update handling/broadcasting of Action start/completed
* Request new `moderator:manage:shoutouts` scope
* Switch [Twitch Shoutout Created](#twitch-shoutout-created) event internally to new Twitch EventSub event
* Twitch Charity EventSub Events have been moved out of beta status
* Fix variables shown in the TipeeeStream tip event help button
* Wired up all the `?` buttons for `YouTube` events
{.changelog-updates}

<span></span>

* Add 3 new C# methods to remove the cooldown of a command
* Add 3 new C# methods to Add To, Remove and Reset a user's cooldown that takes a string for the user id
* Add 3 new C# methods for handling adding, removing and checking if user is in group for string user ids
* Add new [Websocket Event](#websocket-events), ActionCompleted
* Ability to directly rename an Action Group, without having to edit every action
* Add filter to user permissions in Command Dialog
* Add 4 new sub-actions to [Add, Remove, Clear and Set Twitch Tags](#twitch-add-remove-clear-and-set-channel-tags)
* Add 4 new C# methods to Add, Remove, Clear and Set Twitch Tags
* Add 2 new Twitch events, [StreamOnline](#twitch-streamonline-and-offline-events) and [StreamOffline](#twitch-streamonline-and-offline-events)
* StreamElements, add a new `%provider%` variable to Tip and Merch events (can be twitch, youtube or streamelements)
* StreamElements, add a new `%tipId%` variable to the Tip event, this is StreamElements's internal tip id value
* Add new C# method to get how many channel points a user has used, Twitch only
* Add new sub-action to [clear users from a group](#clear-users-from-a-group)
* Add new C# method to clear users from a group
* Add new argument to all actions, `%actionQueuedAt%`, this is when the action was queued
* Add 2 new sub-actions for resetting reward counts
* Add 4 new C# methods for resetting reward counts
* Add an Auto Type option to the Set Argument sub-action, if disabled, the value will be treated as a string
* Add ability to rename a Command group
* Add ability to rename a Twitch Reward group
* Add 2 new sub-actions to Set the Enabled and Paused state of a Twitch Reward group
* Add 6 new C# methods to set the Enabled and Paused state of a Twitch Reward group
* Add new sub-action to send a [Twitch Shoutout](#twitch-send-shoutout), located under `Twitch` -> `Moderation`
* Add 2 new C# methods to send a Twitch Shoutout
* Add new event for when you (the broadcaster) receives a [Twitch Shoutout](#twitch-shoutout-received) from another user
* Add 2 new sub-actions to [Start and Cancel a raid](#twitch-start-and-cancel-raid) on Twitch
{.changelog-new}

## Websocket Events
### ActionCompleted
`0.1.17` introduces a new Raw event, ActionCompleted.  Subscribing to this event in the Websocket Server will get you information when an action is completed.

## New Sub-Actions
### Twitch Add, Remove, Clear and Set Channel Tags
Yes, Twitch finally added the ability to manipulate the new tags!

The Clear Channel Tags sub-action has no input, and will just clear your tags.

The Add, Remove and Set Channel Tag sub-actions all support variables.

The Add Target Info adds the following new arguments:

Name | Description
----:|:------------
`tagCount` | The number of tags
`tag#` | The tag at index position #
`tags` | A `List<string>()` object for use in C#
`tagsDelimited` | A comma delimited string of the tags

> At the moment, there is a bug in the Twitch Helix endpoint, where its unable to clear the tags completely.  So for the time being Clear Tags and Removing the last tag will fail. Once Twitch fixes this, they should start working.
>
> If you keep at least 1 tag active, you'll be able to add/remove tags at will.  And for setting all tags, at least 1 needs to be set.
{.is-warning}

### Twitch Send Shoutout
This is a basic sub-action, either use a variable, or a fixed user login to send a shoutout to the user.

> You may send a Shoutout once every 2 minutes, and to the same broadcaster once every 60 minutes.
{.is-warning}

### Clear Users From a Group
This sub-action will allow you to select one of your groups, so you can clear the users belonging to it during an action

### Twitch Start and Cancel Raid
Since the C# methods for this have existed for a bit, adding in sub-actions to perform this now as well.

## Updated Events
### Twitch Shoutout Created
With the Shoutout events being added to EventSub, this event has been moved from PubSub to EventSub, this unfortunately changes some of the variables.  This Event has also been moved to the `Moderation` tab

Variables Removed
* `%targetUserPrimaryColorHex%`
* `%targetUserProfileImageURL%`
{.grid-list}

Variables Added

Name | Description
----:|:------------
`viewerCount` | The number of users that were watching the broadcaster’s stream at the time of the Shoutout.
`cooldownEndsAt` | The DateTime of when the broadcaster may send a Shoutout to a different broadcaster.
`targetCooldownEndsAt` | The DateTime of when the broadcaster may send another Shoutout to the same broadcaster.

## New Events
### Twitch StreamOnline and Offline events
For the new Twitch StreamOnline event, this will not be triggered if you are online and Streamer.bot connects to your Twitch account.

StreamOnline Event arguments

Name | Description
----:|:------------
`startedAt` | The date, time the stream went online
`game` | The category name
`gameId` | The category id
`tagCount` | The number of tags
`tag#` | The tag at index position #
`tags` | A `List<string>()` object for use in C#
`tagsDelimited` | A comma delimited string of the tags

StreamOffline Event arguments

Name | Description
----:|:------------
`endedAt` | The date time when the stream went offline

### Twitch Shoutout Received
With the new EventSub events for Shoutouts, **Streamer.bot** can now react to receiving a Shoutout
> This event is sent only if Twitch posts the Shoutout to your activity feed.
{.is-warning}

Shoutout Received Event Arguments

Name | Description
----:|:------------
`%viewerCount%` | The number of users that were watching the from broadcaster's stream at the time of the Shoutout

## New C# Methods
```csharp
void CommandRemoveGlobalCooldown(string id);
void CommandRemoveUserCooldown(string id, int userId);
void CommandRemoveAllUserCooldowns(string id);
```

```csharp
void CommandResetUserCooldown(string id, string userId);
void CommandRemoveUserCooldown(string id, string userId);
void CommandAddToUserCooldown(string id, string userId, int seconds);
```

```csharp
bool UserIdInGroup(string userId, string groupName);
bool AddUserIdToGroup(string userId, string groupName);
bool RemoveUserIdFromGroup(string userId, string groupName);
```

```csharp
bool TwitchClearChannelTags();
bool TwitchSetChannelTags(List<string> tags);
bool TwitchAddChannelTag(string tag);
bool TwitchRemoveChannelTag(string tag);
```

```csharp
long TwitchGetChannelPointsUsedByUserId(string userId);
```

```csharp
bool ClearUsersFromGroup(string groupName);
```

```csharp
void TwitchResetRewardCounter(string rewardId);
void TwitchResetRewardUserCounters(string rewardId);
void TwitchResetUserRewardCounters(string userId, bool persisted);
void TwitchResetUserRewardCounter(string rewardId, string userId);
```

```csharp
void TwitchRewardGroupEnable(string groupName);
void TwitchRewardGroupDisable(string groupName);
void TwitchRewardGroupToggleEnable(string groupName);
void TwitchRewardGroupPause(string groupName);
void TwitchRewardGroupUnPause(string groupName);
void TwitchRewardGroupTogglePause(string groupName);
```

```csharp
bool TwitchSendShoutoutById(string userId);
bool TwitchSendShoutoutByLogin(string userLogin);
```

# Streamer.bot v0.1.16
Released 2022-12-31{.subtitle}

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

# Streamer.bot v0.1.15
Released 2022-12-22{.subtitle}

* Misc fixes/tweaks
* Testing OBS Raw should no longer crash if the call to OBS errors
* Twitch artificial present viewers tick could return YouTube users as well
* Double clicking on a Channel Reward when not connected to Twitch would cause a crash
* Double clicking in empty area, or headers in inspect variable dialog would cause a crash
* Right clicking in empty area, or headers in inspect variable dialog would cause a crash
* Add a check for OBS port being out of range
* Add a check for a possible null ref in loading 7TV emotes
* Fix being able to drag sub-action groups into groups
* First pass of networking code improvements
* Prevent channel reward costs from exceeding 2,147,483,647 points
* Fix possible crash when exporting actions
* Fix OBS Event dialog not validating correctly when editing an event
* Fix Quotes not being removed in the UI
* Fix Twitch Gift Sub Bomb test not using the correct anonymous check box
* Fix Anonymous Twitch Gift Bomb causing a silent crash
{.changelog-fixes}

<span></span>

* Add the ability to change the avatar image for the Basic Discord Hook
* Update `CPH.TwitchRunCommercial(...)` to return a `bool`, `True` if it was successful, `False` otherwise
* Add option to disable auto completion of braces and quotes in `Execute C# Code` editor, default is enabled
* Add `firstMessage` argument to `Twitch First Words` event
* Update arguments for `Twitch First Words` event to be more like a chat message event since they are near identical
* Update the Websocket message that is broadcast for a `Twitch First Words` event, this could be a breaking change
* Discord Webhook sub-action now supports `%variables%` for the Webhook URL, URL check is performed when sub-action is run now
* Prevent empty messages, and messages longer than 200 characters from being sent to YouTube, they will be logged
* Prevent empty messages, and messages longer than 500 characters from being sent to Twitch, they will be logged
* Command settings have been split from the main settings file into their own file
* Twitch Account tab has a new look
* Split various Twitch services, so when one is disconnected, it won't bring them all down
* Lumia Stream Set Color sub-action now supports variables for the color
* Split auth tokens into separate file, reducing how often main settings is saved
* Convert globals file to new database file, this should be transparent for most users
* For twitch events that provide the user's color, if it is not set, do not add the color variable
* Added new library to make use of [Twitch EventSub](#twitch-eventsub), a handful of events are moved over to this service now
* Some Twitch specific user data has been moved to its own database, this includes channel point rewards redeems and pyramid `creations`/`breakings`. This will drastically lower the file size of the users.dat file
* Twitch Rewards have been moved to their own data file
* Twitch Reward Configure sub-action, now sends calls all at once instead of waiting for results
* Some tweaks to Patreon events that come through the Streamer.bot website
* Tab order of Actions dialog and Twitch Channel Rewards dialog have been updated
* Show `<null>` in the Inspect Variable dialog, when the value is null, instead of an empty space
* Update visual display of Logic If sub-action, else will always show now
* Update Twitch Gift Sub Bomb test to send out gift subs that match the Gift Bomb event
* Still send Websocket message for Twitch gift subs that come from a sub bomb even if they're ignored
* Set Voice Control Command sub-action can now change any voice control command type, instead of `Anywhere` only
* Update tab order for most dialogs
{.changelog-updates}
 
<span></span>

* Added the ability to use [MIDI](#midi-support)!
* Request new [Twitch Scopes](#new-twitch-broadcaster-scopes)
* Add 3 new sub-actions for MIDI Out, `Note On`, `Control Change` and `Generic`
* [Batch request](#obs-websocket-v5x-batch-requests) support for v5.x OBS Raw sub-action
* Add 3 new comparison options for `Logic If` sub-action, `Equals (Ignore Case)`, `Not Equals (Ignore Case)` and `Is Null or Empty`, data is assumed to be a string
* Add an artificial Present Viewers tick to YouTube
* Add a setting to name your instance of **Streamer.bot**
* Add a `Connected` and `Disconnected` event to an OBS Websocket Connection
* Add option to `Execute C# Code` to save the result (`true/false`) to a variable
* Add option to `Execute C# Method` to save the result (`true/false`) to a variable
* Add option to disable logging of Voice Control dictation entries, this is now disabled by default
* [New C# methods](#new-c-methods) to start/cancel a raid
* Add 2 new Twitch sub-actions, Get Shield Mode Status, and Update Shield Mode Status
* Add 2 new Twitch Events, Shield Mode Start and End
* Refresh the Account tab for Twitch and Streamer.bot Integrations
* When inspecting variables in the Action History, you can now copy all variable names, and/or copy all the data as a text table
* A new menu layout for adding sub-actions, with a config option to use old style
* A way to favorite sub-actions to show in a Favorite Sub-action menu item (only applies to the new layout)
* Add a new Twitch Event, Ad Mid-Roll, this event typically fires 5s before an ad runs
* New [Service Status](#service-status) indicator in the status bar of Streamer.bot
* Add a Decrement option to the Global (Set) sub-action
* Add header options to Fetch URL sub-action
* Add new setting to customize the color of a disabled sub-action
* Add new setting to customize the color of a comment sub-action
* Add color setting to comment sub-action to be able to override application default
* New Twitch sub-action [Follow Mode](#twitch-follow-mode), and C# Method
{.changelog-new}

## MIDI Support
Yes, you read the correctly, as of **Streamer.bot** v0.1.15, there will be MIDI support!

### MIDI In
So, it will now be possible to run actions by using your MIDI Piano, and MIDI synth, oh, even your MIDI wind instrument, or anything that supports MIDI!

When adding an `Event`, you will be able to just press the key, turn the knob, or flick the wheel to have it auto populate all the settings for you.

This section is a WIP for information, but to get you started, here are some screenshots.

![midi-04.png](/midi/midi-04.png)

Add a new MIDI In device
![midi-01.png](/midi/midi-01.png)

Add a new MIDI event
![midi-03.png](/midi/midi-03.png)

Editing a MIDI event
![midi-02.png](/midi/midi-02.png)

To get started with MIDI follow these steps:

1. Add a Device, to do this, right click in the top section of the MIDI tab, and click Add
2. Pick your device from the drop down, and give it a name, and click Ok
3. Select the device you just added
4. Right click anywhere in the bottom list, and Add an event.
5. With the Add Event dialog open, you can press any of the keys on your device to have it fill in all the data for you and show an example of what the arguments will look like.

### MIDI Out
The other side of MIDI, being able to send MIDI events out to your devices or DAWs.

Much like MIDI In, you create a device mapping within Streamer.bot, and you can use 1 of 3 new sub-actions to send MIDI events.

## New Twitch Broadcaster Scopes
* `channel:manage:raids`
* `channel:read:hype_train`
* `channel:read:goals`
* `moderator:manage:shield_mode`
{.grid-list}

## Twitch EventSub
Twitch updated there eventsub to support websocket connections, so after trialing it for a bit, I have added a new library to connect to this new service, and subscribe to various events.

### Events that are now on EventSub
* Twitch Poll Events
* Twitch Prediction Events
* Twitch Channel Reward Events
* Twitch Follow Event
* Twitch Hype Train Events
* Twitch Charity Events (**improved and some new**)
* Twitch Channel Goals (**new**)
* Twitch Shield Mode (**new**)

### Twitch Charity Events
Despite there already being support for Twitch Charity Donate, switching over to EventSub has introduced 3 new events (Started, Progress and Stop), as well as update the Donate event with more data.

### Twitch Channel Goals
These are the goals you can configure, new follower goal, subscription goal, etc.  Now you can get udpates on these by way of 3 new events, Goal Begin, Goal Progress and Goal End

### Twitch Hype Train Events
The hype train events have been altered slightly, and are no longer restricted to 5 levels, they can go on forever now.  The calculations for % complete have also been tweaked and hopefully are more accurate now.

### Twitch Channel Reward Events
These events mostly remain unchanged, there is a slight re-organization of data, but is ver minimal.

### Twitch Shield Mode Events
There are 2 new events for Twitch's Shield Mode, Begin and End. You can assign actions to these and have your stream react when your Shield Mode is enabled/disabled.

### Twitch Prediction and Poll Events
Largely remain unchanged from the previous events.

## Service Status
With **Streamer.bot** v0.1.15 you can see, at a glance, if all your services are connected.

In the bottom right hand corner of **Streamer.bot**, there is now an indicator that shows if you're connected to your services.  If you click on this, you'll be presented with a detailed list of what is all connected, and, you can click on any of the services to be taken to the settings page for it.

![service-status.png](/service-status.png)

## New Sub-actions
### Twitch Follow Mode
Turn follow mode on, or off with the new sub-action, or by the new [C# method](#new-c-methods)

### MIDI Out Sub-Actions
* Control Change
* Note On
* Generic Event
{.grid-list}

## New C# Methods
> There is no way, by API to send a raid yet, can only create, and cancel a raid
{.is-info}

```csharp
bool TwitchStartRaidById(string userId);
bool TwitchStartRaidByName(string userName);
bool TwitchCancelRaid();
```

```csharp
void TwitchFollowMode(bool enabled = true, int duration = 0);
```

## OBS Websocket v5.x Batch Requests
You can now perform batch requests to a v5.x obs-websocket with OBS Raw
```json
{
  "haltOnFailure": false,
  "executionType": -1
  "requests": [
    {
      "requestType": "<string>",
      "requestData": { ... }
    }
  ]
}
```

Name | Description
----:|:------------
`haltOnFailure` | `True`/`False`, setting to true will stop processing requests if one fails, default is `False` and can be omitted
`executionType` | A number value, `-1`, `0`, `1`, `2` to indicate how to perform the requests, default is `-1` and can be omitted
`requests` | This is the array of your requests, each request takes on the same format as a single request

# Streamer.bot v0.1.14
Released 2022-10-27{.subtitle}
 
* Typos
* Blocking state of a queue was not updating visually
* OBS Take Screenshot sub-action was halting an action when used with OBS websocket v5
* Lumia Stream Send Command sub-action dialog would crash if there are no commands
* Lumia Stream disconnect button would not work
* Lumia Stream Set Color sub-action dialog could possibly crash
* Catch exceptions thrown by speech recognition initialization, log and try to be more graceful about it
* Handle potential crash with an internal Users Joined event, when an API call failed
* Small startup improvements
* Twitch Add Target Info should have the correct VIP/Subscriber boolean values now
* Some Twitch API calls weren't being routed through proper internal calls, causing tokens not to be refreshed as needed
* Some potential crashes in obs-websocket 5 data handling (there may still be more unfortunately)
* Lumia Stream set color sub-action should correctly pickup manual changes to the color field now
* Custom Websocket Server would crash when using an invalid address
* File/Folder watcher was not updating the filter correctly when changed
* Some logging was not behaving correctly, should behave now
* Some error may be caught properly now, and longer full crash **Streamer.bot**
* DoAction and C# RunAction should now create a new argument dictionary when not running immediately, no longer sharing it
* <kbd>CTRL+D</kbd> shortcut on sub-actions will now duplicate a group correctly
* VoiceMod Set Background Effect State should work correctly now
* C# method SetChannelGame should no longer throw an exception when used
* Comment sub-action should behave correctly now (no longer disappearing, or moving around on its own)
* Forgetting Twitch broadcaster account forgot bot account (woops)
* Stop saving config when a channel reward is updated
* Fix File/Folder watch init to check for existence of folder
{.changelog-fixes}

<span></span>

* New Twitch Scopes requested for both broadcaster and bot accounts
* Add new C# method, `CPH.ObsTakeScreenshot`
* Twitch commands have a new argument, `%msgId%` which is the id of the message
* Remove caret from Twitch username text boxes, so there's no indication you should type in them
* Remove caret from YouTube username text boxes, so there's no indication you should type in them
* Updates to LumiaSDK, hopefully its a bit more stable and working better
* [Twitch Whisper](#twitch-whisper) has been updated to use the new API, this is part of a change away from slash commands being deprecated
* C# method for sending a whisper on Twitch, has been updated, `bool SendWhisper(string userName, string message, bool bot = true)`
* Internally, update various methods to use API calls, instead of IRC commands, as these are being deprecated
* Update internal methods for adding/removing moderators/VIPs to use API calls
* Update internal methods for deleting a chat message, to use API call
* Read Random Line from file sub-action now includes the line number as a variable, `%randomLineNumber#%`
* MathParser-mXparser updated to v5.0.7
* Updated Google YouTube C# Libraries to current
* Twitch sub-action Set Channel Game, now adds game variables if you've picked a game from the list
* **Streamer.bot**'s built in websocket server can now listen on any address, just enter `*` for the ip address
* Custom websocket servers can now listen on any address, just enter `*` for the ip address
* Since Hosts are going away soon on Twitch, they have been removed from **Streamer.bot**
* Better handling of Twitch disconnects, this is part of ongoing improvements
* Timed Action line counts now support YouTube chat, at the moment, line counts work for either service, if you have both connected, line counts will not be used
* Update endpoint used to get a users current chatters to the new GetChatters API
* Decrease present viewers tick to 1 minute, with the change to the new GetChatters API
* Remove LootDevil support, as they closed down
* Wrap sub-action handling within an action in a try/catch, to catch generic exceptions, this will also ***halt*** an action
* Performance improvements when handling large amounts of viewers
* Performance improvements when connecting to Twitch
* Disable verbose logging on Twitch Bot Account
* Stop saving config when a channel reward is updated
* Forgetting broadcaster account forgot bot account (woops)
* Add more verbose logging
* Changes to the [Twitch Present Viewer Tick](#twitch-present-viewer-tick)
* Updates to File/Folder watch to show error if you try to enable a watcher with a missing folder
* Move [Twitch timeout and ban events](#twitch-timeout-and-ban-events) to use PubSub events, this provides who, as well as reason in addition to existing data.
* Updated line count handling for Timed Actions, this is no longer a debounced event, it should happen as the line counts increase.  This may change depending how it behaves with performance.
* Add some checks when using `Set Reward Title` and `Reward Update` sub-actions to prevent setting titles longer then 45 characters, and prompt longer then 200 characters
{.changelog-updates}

<span></span>

* **Streamer.bot** now has an [Auto Updater!](#auto-updater)
* Add a new menu item for OBS connections that lets you assign **ALL** OBS related sub-actions to that connection
* Add a new [OBS Set Color Source Color](#obs-set-color-source-color) sub-action and C# methods
* Request new scope `whispers:read` on bot account, you will need to re-authorize your bot account
* Add new CPH method for logging `LogVerbose(string logLine)`
* Add new CPH method for LumiaStream `LumiaSetToDefault()`
* Add new CPH method for LumiaStream `LumiaSendCommand()`
* Add new event for Twitch, Bot Whisper, can now react to whispers the bot account receives
* Add new command source Twitch Bot Whisper, can now react to whispers the bot account receives
* Add new CPH method for taking a screen shot in OBS, the source can be either a source, or a scene
* Add a new sub-action, `OBS`->[Get Status](#obs-get-status) to add OBS status information
* Add a new sub-action, `Twitch`->[Add Viewer Count](#twitch-add-viewer-count) to add your current Twitch viewer count as a variable
* Add new CPH methods for adding/removing moderators/VIPs
* Add internal method for clearing chat using API call
* Add new CPH method for clearing chat, `bool TwitchClearChatMessages(bool bot = true)`
* Add new CPH method for deleting a chat message, `bool TwitchDeleteChatMessage(string messageId, bool bot = true)`
* Add new CPH methods for banning/unbanning and timing out a user
* Add new CPH method for checking if an action exists, or if its enabled/disabled
* Support for [Twitch Charity](#twitch-charity), with 2 new events, Donation and Completed
* Add new sub-action to fetch the latest [Twitch Charity Campaign](#twitch-get-latest-charity-campaign)
* Support for Coin Cheer (this is experimental and could break)
* Support for [Shopify Webhooks](#shopify)!
* Add new sub-action [Discord Basic Webhook](#discord-basic-webhook), to enable posting basic text to a discord webhook
* Add new CPH method, `DiscordPostTextToWebhook` to post text to a discord webhook
* Add new event for Twitch, [Shoutout Created](#twitch-shoutout), this is triggered when the `/shoutout` command is used, if your channel has the ability
* Added option to enable/disable present viewer tick, default disabled
* Added option to change present viewer tick from 1 to 10 minutes, default of 5 minutes
* Added new context menu item for actions to set their queue
{.changelog-new}

## Auto Updater
With version 0.1.14, the ground work has been put in to include an auto updater, which means, this is the **last** version that will require you to manually update.  Moving forward, starting with version 0.1.15, you will be able to update within **Streamer.bot** itself.

If you have been using the recent betas, or are part of alpha testing, you've already been giving this feature a try!

When you launch **Streamer.bot** it will perform a check to see if there is an update, and if there is, you will see a screen pop-up similar to the one below.

![auto-updater-001.png](/update/auto-updater-001.png)

After you click `Download`, and the update is downloaded, you will be able to install the update by clicking on `Install`

![auto-updater-002.png](/update/auto-updater-002.png)

As you can see, there are update channels, `stable`, `beta`, `alpha`.  By default everyone will be on the stable channel, which are the public releases.

To be able to select any other update channel, you will need to have **Streamer.bot** connected to the website, under Integrations, and have the appropriate roles in the Discord.

## New Twitch Broadcaster Scopes
* `channel:read:charity`
* `moderator:manage:chat_messages`
* `moderator:read:chatters`
{.grid-list}

## New Twitch Bot Scopes
* `moderator:manage:chat_messages`
{.grid-list}

## Twitch Present Viewer Tick
I have gone through and changed how the present viewer tick operates, it is still possible to have the same behavior as 0.1.12, so continue reading.

The present viewer tick will always happen, but you now have the ability to have it "live update" from twitch, or artificially mark someone as present.

Under the Present Viewer action selector, there are 2 new setttings, a `Live Update` check box, and a slider bar.

When Live Update is checked, the slider next to it is how often this update will occur, between 1 and 10 minutes, this will also still execute the action at this interval.

When Live Update is not checked, the slider next to it behaves as a threshold. The timer runs every minute, and checks the current time minus the user's last active time, if this is less then the threshold, they are marked as present, otherwise they are marked as not present.  The action will still be executed, but, it will occur every minute.

The default setting is `Live Update` not checked, and the slider set to `5` minutes.  To have the same functionality as 0.1.12 and earlier, enable `Live Update` and make sure the slider is set to `5` minutes.

## Twitch Charity
The newly released Charity feature of Twitch is now supported within **Streamer.bot**

This introduces 2 new events, **Donation** and **Completed**

## Twitch Timeout and Ban Events
Switching these events to use the data that comes from PubSub, they may happen quicker, as well, more variables are available.

Both the ban and timeout events gain the following variables

Name | Description
----:|:------------
`createdAt` | The date and time the ban or timeout was created
`createdById` | The Twitch ID of the user who created the ban or timeout
`createdByUsername` | The user name of the user who created the ban or timeout
`createdByDisplayName` | The display name of the user who created the ban or timeout
`reason` | The reason for the ban or timeout

### Donation Event
The donation event occurs when someone has donated to your charity.

Variable that are included are as follows:

Name | Description
----:|:------------
`baseAmount` | The amount of the donation as a whole number
`donationAmount` | The amount of the donation in decimal form
`charity.name` | The name of the charity you are supporting
`currency.code` | The 3 letter ISO currency code
`currency.exponent` | Divide base amount by 10 to the power of this number to get the decimal value
{.vars-table}

> Twitch is providing amount values for Charity calls as whole numbers, so $42.00 will return as 4200.
{.is-warning}

### Completed Event
When donations come through, a check is made if your current donation amount matches what your goal is, and will send a completed event if this is true.

Variable that are included are as follows:

Name | Description
----:|:------------
`charity.id` | Twitch's internal ID for your campaign
`charity.timestamp` | The timestamp of the event
`charity.currency` | The 3 letter ISO currency code
`charity.donationTotal` | How much you have raised so far, asa  whole number
`charity.goalTarget` | Your campaign's target amount as a whole number
{.vars-table}

> Twitch is providing amount values for Charity calls as whole numbers, so $42.00 will return as 4200.
{.is-warning}

## Twitch Shoutout
Twitch recently added, as a beta feature a new `/shoutout` command, so for those users who have this on there channel, you can now react to when you, or a moderator uses this command, and treat it like a !so chat command!

The user who was given the shoutout will be contained in the `target*` variables.

Available variables:

Name | Description
----:|:------------
`shoutoutId` | Twitch's internal ID for the shoutout
`targetUserId` | The user's id
`targetUserLogin` | The user's login name
`targetUserDisplayName` | The user's display name
`targetUserPrimaryColorHex` | The user's primary color in hex
`targetUserProfileImageURL` | The user's profile image
{.vars-table}

## Shopify
By using the **Streamer.bot** website, you can now add webhooks to your Shopify store front!

> Supported webhook events include `Order creation` and `Order payment`
{.is-warning}

There are 2 new events within **Streamer.bot** that you can associate an action with, `Order Created`and `Order Paid`.  Both of these events will provide you with almost all the information that is provided by the webhook.

The best way to check the variables, is to setup your webhooks, and assign an empty action, then check the available variables in the `Action History` tab under `Action Queues`

## New Sub-actions
### OBS Set Color Source Color

Added a new sub-action that lets you set the color of a color source within OBS.  All fields support `%variable%` replacement, and there is an option to just set a random color.

![obs-set-color-source-color-01.png](/obs-set-color-source-color-01.png)

### OBS Get Status
This will add up to 3 new variables to your action for the selected OBS connection.

Name | Description
----:|:------------
`isConnected` | Boolean value indicating if the selected OBS connection is connected <br> `True`/`False`
`isStreaming` | Boolean value indicating if the selected OBS connection is streaming <br> `True`/`False`
`isRecording` | Boolean value indicating if the selected OBS connection is recording <br> `True`/`False`
{.vars-table}

### Twitch Add Viewer Count
This will let you add your current Twitch viewer count as a variable to your action.

> This value is only updated every 30 seconds
{.is-info}

Name | Description
----:|:------------
`viewerCount` | Your current Twitch viewer count
{.vars-table}

### Twitch Get Latest Charity Campaign
This sub-action will fetch your latest Twitch Charity campaign and add the information as variables.

Name | Description
----:|:------------
`campaignId` | Twitch's internal ID for your campaign
`charity.name` | The name of the charity you are supporting
`charity.description` | The description of the charity you are supporting
`charity.logoUrl` | The logo of the charity you are supporting
`charity.websiteUrl` | The website to the charity you are supporting
`currentAmount` | How much you have raised so far, asa  whole number
`targetAmount` | Your campaign's target amount as a whole number
{.vars-table}

> Twitch is providing amount values for Charity calls as whole numbers, so $42.00 will return as 4200.
{.is-warning}

### Discord Basic Webhook
This is the first of a few new Discord specific sub-actions that will be added.  Up first is a friendlier way to post to a webhook you setup in your discord.  This one only allows for basic text posting.

Username, content, and image can contain variables and will be parsed.

Username, and image are also optional

![discord-basic-webhook-02.png](/discord-basic-webhook-02.png)

## New C# Methods
Add the following new C# methods

### Logging
```csharp
void LogVerbose(string logLine);
```

### Twitch
```csharp
bool SendWhisper(string userName, string message, bool bot = true);
bool TwitchAddModerator(string userName);
bool TwitchRemoveModerator(string userName);
bool TwitchAddVip(string userName);
bool TwitchRemoveVip(string userName);

bool TwitchClearChatMessages(bool bot = true);
bool TwitchDeleteChatMessage(string messageId, bool bot = true);

bool TwitchBanUser(string userName, string reason = null, bool bot = false);
bool TwitchUnbanUser(string userName, bool bot = false);
bool TwitchTimeoutUser(string username, int duration, string reason = null, bool bot = false);
```

### OBS
```csharp
bool ObsTakeScreenshot(string source, string path, int quality = -1, int connection = 0);
void ObsSetColorSourceColor(string scene, string source, int a, int r, int g, int b, int connection = 0);
void ObsSetColorSourceColor(string scene, string source, string hexColor, int connection = 0);
void ObsSetColorSourceRandomColor(string scene, string source, int connection = 0);
```

### Lumia Stream
```csharp
void LumiaSendCommand(string command);
void LumiaSetToDefault();
```

### Actions
```csharp
bool ActionExists(string actionName);
```

### Discord
```csharp
bool DiscordPostTextToWebhook(string webhookUrl, string content, string username = null, bool textToSpeech = false);
```

## Twitch Whisper
Some important notes with how Twitch Whispers appear to be handled now, this is a copy from the Twitch development documentation.

The user sending the whisper must have a **verified phone number** (see the **Phone Number setting** in your **Security and Privacy settings**).

The API may silently drop whispers that it suspects of violating Twitch policies, it will still indicate success even if the message is dropped.

Rate Limits: You may whisper to a maximum of **40 unique recipients per day**. Within the per day limit, you may whisper a maximum of 3 whispers per second and a maximum of 100 whispers per minute.

The maximum message lengths are:
* 500 characters if the user you're sending the message to hasn't whispered you before.
* 10,000 characters if the user you're sending the message to has whispered you before.

Messages that exceed the maximum length are truncated.

# Streamer.bot v0.1.12
Released 2022-08-31{.subtitle}

This is a hotfix release

* OBS Websocket 5.x source visibility sub-action was not working, when the source is in a group
* OBS Websocket 4.9.x, issues with deserialization of a few calls
* Silent crash in OBS Hide Group's Sources
* Potential crash in OBS group related sub-actions, if group no longer exists when editing
{.changelog-fixes}

# Streamer.bot v0.1.11
Released 2022-08-31{.subtitle}

* Commands in an import will be disabled by default, this is more of a security precaution
* Action updates were not properly being sent to the Streamer.bot website for decks
* Pyramids not resetting correctly if a single emote is used after a previous single emote
* Twitch Reward Set Global Cooldown sub-action, properly lists rewards now
* Crash when using <kbd>Ctrl+C</kbd> on a group in an action
* `inputUrlEncoded#` variables to actually be the word, and not the entire message for each one
* Get Team Info For Target silently crashing
* Better handling for the Twitch Get Present Viewers tick, optimizations to limit potential API calls
* OBS Raw sub-action was not saving the prefix
* Silent null ref crash for timed actions when Twitch is not connected, should be completely decoupled now
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
* Inspect variables dialog saves its size now when closed
* Right click context menu on cells in the inspect variable dialog to copy the data, as text, to your clipboard
* Double clicking on a cell in the inspect variables dialog will copy the value, as text, to your clipboard
{.changelog-updates}

<span></span>

* [OBS Websocket v5.x](#obs-websocket-v5x) Support
* Added new variable `%wsIdx%` to WebsocketClient action arguments, which is the index of the client, 0 based, -1 if not found
* Added new variable `%wssIdx%` to CustomWebsocketServer action arguments, which is the index of the server, 0 based, -1 if not found
* Added new variable `%wssId%` to CustomWebsocketServer action arguments, which is the ID of the websocket server
* Add new VoiceMod sub-action to play a soundboard sound
* Add new VoiceMod sub-action to stop  playing all VoiceMod sounds
* Regex commands will now add match group values as arguments, `%match[#]%`, as well as named match groups, if you're using `?<groupName>` in your regex
* [Lumia Stream](#lumia-stream-1) integration!
* New sub-action Send Command for Lumia Stream
* New sub-action Set Color for Lumia Stream
* New sub-action Set to Default for Lumia Stream
* New integration, [Loot Devil](#loot-devil)
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

## Loot Devil
Some have been asking for it, well now it's here, you can connect Loot Devil to **Streamer.bot** now!  To use this, requires the use of the **Streamer.bot** website to configure the web hook, and connecting the application to the website to receive gifting events.

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

# Streamer.bot v0.1.10
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


Name | Description
----:|:------------
`%adLength%` | The length of the ad in seconds
`%adScheduled%` | If this ad was a scheduled ad

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

# Archives
View changelogs for older releases{.subtitle}

* [Streamer.bot 0.1.8](/Changelogs/Archives/Version-018)
* [Streamer.bot 0.1.7](/Changelogs/Archives/Version-017)
* [Streamer.bot 0.1.6](/Changelogs/Archives/Version-016)
* [Streamer.bot 0.1.5](/Changelogs/Archives/Version-015)
* [Streamer.bot 0.1.4](/Changelogs/Archives/Version-014)
* [Streamer.bot 0.1.3](/Changelogs/Archives/Version-013)
* [Streamer.bot 0.1.2](/Changelogs/Archives/Version-012)
* [Streamer.bot 0.1.1](/Changelogs/Archives/Version-011)
* [Streamer.bot 0.1.0](/Changelogs/Archives/Version-010)
* [Streamer.bot 0.0.63](/Changelogs/Archives/Version-0063)
* [Streamer.bot 0.0.62](/Changelogs/Archives/Version-0062)
* [Streamer.bot 0.0.61](/Changelogs/Archives/Version-0061)
* [Streamer.bot 0.0.60](/Changelogs/Archives/Version-0060)
* [Streamer.bot 0.0.59](/Changelogs/Archives/Version-0059)
* [Streamer.bot 0.0.58](/Changelogs/Archives/Version-0058)
* [Streamer.bot 0.0.57](/Changelogs/Archives/Version-0057)
* [Streamer.bot 0.0.56](/Changelogs/Archives/Version-0056)
* [Streamer.bot 0.0.55](/Changelogs/Archives/Version-0055)
* [Streamer.bot 0.0.54](/Changelogs/Archives/Version-0054)
* [Streamer.bot 0.0.53](/Changelogs/Archives/Version-0053)
* [Streamer.bot 0.0.52](/Changelogs/Archives/Version-0052)
* [Streamer.bot 0.0.51](/Changelogs/Archives/Version-0051)
* [Streamer.bot 0.0.50](/Changelogs/Archives/Version-0050)
* [Streamer.bot 0.0.44](/Changelogs/Archives/Version-0044)
* [Streamer.bot 0.0.43](/Changelogs/Archives/Version-0043)
* [Streamer.bot 0.0.42](/Changelogs/Archives/Version-0042)
* [Streamer.bot 0.0.41](/Changelogs/Archives/Version-0041)
* [Streamer.bot 0.0.40](/Changelogs/Archives/Version-0040)
* [Streamer.bot 0.0.39](/Changelogs/Archives/Version-0039)
* [Streamer.bot 0.0.38](/Changelogs/Archives/Version-0038)
* [Streamer.bot 0.0.37](/Changelogs/Archives/Version-0037)
* [Streamer.bot 0.0.36](/Changelogs/Archives/Version-0036)
* [Streamer.bot 0.0.35](/Changelogs/Archives/Version-0035)
* [Streamer.bot 0.0.33](/Changelogs/Archives/Version-0033)
* [Streamer.bot 0.0.32](/Changelogs/Archives/Version-0032)
* [Streamer.bot 0.0.31](/Changelogs/Archives/Version-0031)
* [Streamer.bot 0.0.30](/Changelogs/Archives/Version-0030)
{.btn-grid .my-5}