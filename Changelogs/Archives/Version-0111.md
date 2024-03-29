---
title: Version 0.1.11
description: Released 2022-08-31
published: true
date: 2023-08-31T01:35:00.555Z
tags: 
editor: markdown
dateCreated: 2023-08-31T01:35:00.555Z
---


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