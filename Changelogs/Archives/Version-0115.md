---
title: Version 0.1.15
description: Released 2022-12-22
published: true
date: 2023-08-31T01:37:08.742Z
tags: 
editor: markdown
dateCreated: 2023-08-31T01:37:08.742Z
---


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
