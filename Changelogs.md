---
title: Changelogs
description: List of new features, bug fixes and improvements
published: true
date: 2023-09-22T02:32:01.377Z
tags: 
editor: markdown
dateCreated: 2021-08-25T21:51:24.140Z
---

# Streamer.bot v0.2.2 (WIP)
Upcoming changes in the next release!{.subtitle}

* Fix typos
* Fix being able to run multiple instances of **Streamer.bot** from different folders
* Fix `UserName` and `UserLogin` being reversed in `UserVariableValue<T>` return value
* Fix Twitch Hype Chat `__source` values
* Tweaks to internal message parsing
* Fix potential crash in Streamlabs Desktop handling
* Fix wrong ToastId being used in Toast Activation trigger
* Fix issue related to MinMax values for triggers, and logic not working correctly
* Fix C# methods for getting/setting variables by username not comparing against the user's login
{.changelog-fixes}

<span></span>

* Twitch Hype Train progress was re-added back to credits handling
* `Perform Command` sub-action was not fully renamed to `Run a Program`
* Update Elgato Wave Link to support Real-time level monitors tht was added in 1.8.2
* Update logging of parsing 3rd party emotes to `Verbose` level
* Move `Crowd Control` triggers under `Integrations`
* Don't color a trigger as blue if there are no criteria for it
* Update `Twitch User Timedout` Trigger to support a range for the duration
* Add more cleanup to Global Variables during upgrade processes
* Set Twitch Reply To Message sub-action's MsgId field to a default value of `%msgId%` 
* Update display in `Twitch Emote Only` sub-action dialog to be `On`/`Off` instead of `Yes`/`No`
* Better handling of Twitch Chat for high volume channels
* Performance tweaks surrounding Twitch Chat handling
* More Twitch Reply information is added to the arguments, inspect an action that has a reply to see all the new fields, and note `replyTo` is no longer available.
{.changelog-updates}

<span></span>

* Add enabled/disabled color indicator to Timed Actions
* Add new [`Simulated Events`](#simulated-events)
* Add a new Dialog that can be used within **Streamer.bot** to search for Twitch user's both from the internal cache, and from within Twitch itself
* Add a way to disable unused sub-actions
* Add a way to disable unused triggers
* Allow re-organizing of triggers, this is only a visual thing
* Add new C# Method, `TwitchGetBot()`
* Add 7 new triggers for Streamlabs Desktop
* Add new historical data collection to Twitch Data. `Subscriptions`, `Gift Bombs`, and `Hype Trains` are now recorded
* Add option to disable Present Viewers timer for Twitch
* Add option to completely disable the Action History, as well as Pending items
* Add enabled/disabled color indicator to File Watcher items
* Add an option to disable the Viewers Tab, for performance reasons
* Add an option to disable Twitch Present Viewers tick completely
{.changelog-new}

## Simulated Events
Prior to **0.2.0**, one could test certain Twitch events from within the respective events tabs, and with the release of **0.2.0**, this was change to be able to test the `Triggers` directly.

With the addition of `Triggers`, this opened up the ability to have multiple actions triggered by the same event, so in order to test this, you would have to goto each action, and test the trigger manually.

With **0.2.2**, a new way of testing has been added, `Simulated Events`

`Simulated Events` are still initiated from a trigger's context menu, however, they will allow you to specify certain data (for instance, for a cheer, you pick the user, and specify the amount), and it will simulate this event application wide, so any triggers that match, will be run.

With this feature, also comes a way to not only search your local user cache, but, to also search against Twitch itself.
> The API used for searching only returns users who have streamed within the last 6 months, this is a limitation of the API, and is not possible to circumvent
{.is-warning}


# Streamer.bot v0.2.1 (Current)
 Released 2023-09-01{.subtitle}

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
* Fix `YouTube SuperChat` and `SuperSticker` triggers using the microamount and not a decimal value for range comparisons
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
* Update `GetQuote` sub-action to accept `%variables%`
* Update `Get/Set Command State` sub-actions to display the command's name instead of the command
* Update `Twitch Timeout User` sub-action to have similar fields as the `Twitch Unban User` sub-action
* Perform config upgrage on Twitch Timeout User sub-action to new format, be sure to check your timeout sub-actions!
* Range based triggers which are se to `greater than`, are now **inclusive** of that value in comparisons
* Range based triggers which have a `min and max`, are now **inclusive** of the range in comparisons
* Better handling of Twitch VIP and Moderator role information
{.changelog-updates}

<span></span>

* Add setting to commands to ignore internally parsed messages
* Add StreamElements connected/disconnected triggers
* Add Streamlabs connected/disconnected triggers
* Add 7 new triggers for Twitch connections
* Add a clear button for the action filter
* Add nerw VTubeStudioEvent `TrackingStatusChanged`, and accompanying trigger
* Add new C# method `UnsetAllUsersVar`, this will unset the specified variable for all users
* Add 4 new triggers for BetterTTV and SevenTV Adding/Removing emotes
* Add `Create` button to various triggers
* Add delete confirmation when deleting a sub-action group
* Add 3 new C# methods for interactiong with quotes
* Add `IgnoreAliases` setting to GetCommands sub-action, this will return the first command only for each command if enabled
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
# Streamer.bot v0.2.0
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

# Streamer.bot v0.1.22
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

# Archives
View changelogs for older releases{.subtitle}

* [Streamer.bot 0.1.19](/Changelogs/Archives/Version-0119)
* [Streamer.bot 0.1.18](/Changelogs/Archives/Version-0118)
* [Streamer.bot 0.1.17](/Changelogs/Archives/Version-0117)
* [Streamer.bot 0.1.16](/Changelogs/Archives/Version-0116)
* [Streamer.bot 0.1.15](/Changelogs/Archives/Version-0115)
* [Streamer.bot 0.1.14](/Changelogs/Archives/Version-0114)
* [Streamer.bot 0.1.12](/Changelogs/Archives/Version-0112)
* [Streamer.bot 0.1.11](/Changelogs/Archives/Version-0111)
* [Streamer.bot 0.1.10](/Changelogs/Archives/Version-0110)
* [Streamer.bot 0.1.9](/Changelogs/Archives/Version-019)
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