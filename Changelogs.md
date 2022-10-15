---
title: Changelogs
description: List of new features, bug fixes and improvements
published: true
date: 2022-10-15T15:18:22.095Z
tags: 
editor: markdown
dateCreated: 2021-08-25T21:51:24.140Z
---

# Streamer.bot v0.1.14 (WIP)
Upcoming changes in the next release!{.subtitle}
 
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
* <kbd>CTRL+D</kbd> shortcut on sub-actions will not duplicate a group correctly
* VoiceMod Set Background Effect State should work correctly now
* C# method SetChannelGame should no longer throw an exception when used
* Comment sub-action should behave correctly now (no longer disappearing, or moving around on its own)
* Forgetting Twitch broadcaster account forgot bot account (woops)
* Stop saving config when a channel reward is updated
* Added option to enable/disable present viewer tick
* Added option to change present viewer tick from 1 to 10 minutes
* By default present viewer tick is now disabled
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
{.changelog-updates}

<span></span>

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
{.changelog-new}

## New Twitch Broadcaster Scopes
* `channel:read:charity`
* `moderator:manage:chat_messages`
* `moderator:read:chatters`
{.grid-list}

## New Twitch Bot Scopes
* `moderator:manage:chat_messages`
{.grid-list}

## Twitch Charity
The newly released Charity feature of Twitch is now supported within **Streamer.bot**

This introduces 2 new events, **Donation** and **Completed**

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

# Streamer.bot v0.1.12 (Current)
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
## [Pulsoid](https://pulsoid.net/?from=streamerbot) Integration

**Streamer.bot** now has a direct integration with Pulsoid, attach an action to the Heart Rate Pulse event to receive your heart rate events.

The Heart Rate event happens every second while data is being transmitted from Pulsoid, be aware of this.

Name | Description
----:|:------------
| `%measuredAt%` | Time the measurement was taken |
| `%heartRate%` | Heart Rate value |

## HypeRate Integration

**Streamer.bot** now has a direct integration with HypeRate.io, attach an action to the Heart Rate Pulse event to receive your heart rate events.

The Heart Rate event happens every second while data is being transmitted from HypeRate, be aware of this.

Name | Description
----:|:------------
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