---
title: Version 0.1.1
description: 
published: true
date: 2022-07-09T19:56:34.029Z
tags: 
editor: markdown
dateCreated: 2021-08-25T21:34:58.901Z
---

# Streamer.bot v0.1.1

Visit [Streamer.bot 0.61](Version-0.61), [Streamer.bot 0.62](Version-0.62), [Streamer.bot 0.63](Version-0.63) and [Streamer.bot 0.1.0](Version-0.1.0) to see all the shiny new features and updates.

## Some fixes/changes

* Fix typos
* Fix SetSceneFilterState sub-action not populating filter list
* Add new options for Websocket Client settings to specify TLS options
* Update OBS Raw
* Fix not being able to add SLOBS Get Current scene sub-action
* Some UI QOL improvements, both the main and settings tabs are re-orderable, and can hide unused tabs
* Save button gives an indication something is happening
* Some fixes surrounding OBS Websocket and authentication states (still some quirks)
* Add a Name property to OBS Raw to help differentiate them
* Remember collapsed sub-action groups
* Fix a crash when adding a Speech To Text command when it is not listening
* Fix a potential crash when retrieving paginated data from Twitch API
* Add column to Channel Reward to indicated if we own the reward
* Update OBS and SLOBS set GDI text to support multi-line text entry
* Add Collapse/Expand all to context menu for actions
* Fix Streamlabs typo, was firing the wrong event for the generic donation action
* Fix set queue pause state not having a default state when adding the sub-action
* Fix importing actions causing all groups to become expanded, and slow updating of adding the actions
* Enable and fix Twitch Host event
* Fix pausing a queue, if it had actions queued, they still ran, seems I missed a scenario
* No longer allow empty named actions ;)
* Add enabled toggle to action dialog, for enabling/disabling actions
* Fix an issue with WebsocketSend in C# not actually sending data
* Creating a new timer did not have the repeat option checked, as it says in the description
* Founder badge was not being associated to a user as being subscribed
* Add `%isSubscribed%`, `%isModerator%`, `%isVip%` to action arguments
* Add a new sub-action `Clear Action Queue` to clear a blocking queue
* Move separators in sub-action context menu, grouping the menu items a bit better
* Add `Ctrl + Home` and `Ctrl + End` shortcut keys for moving sub-actions to top/bottom
* Misc fixes/cleanup

Join the [Discord](https://discord.gg/zuXpPpgD5K) if you have any questions, would like to share what you've created, or or would like to lend a hand!

## OBS Raw
I have gone through and updated how OBS Raw behaves, previously it would only return if the status of the call was a success or not.  Now, it will take all the JSON values returned and add them onto the argument list in the form of `obsRaw.{path}`, so `status` is now in `obsRaw.status`, so you can check this if the call was successful or not.  The values that are put on the arguments are dynamic and depend on what you are sending.

A note, array will be added as `obsRaw.data.value[0].id` for example.

If you are using OBS Raw through C#, you will be given back the JSON as a string, so you can use a JObject.Parse() to convert it to something usable in your code.

### Variable Replacement

You can also use variables in OBS Raw.  To use variables, just add the variable inbetween quotes for your json property

Example:
```json
{
  "test": "%variable%"
}
```

The underlying code will go through all the properties and do any variable replacements it finds.

## Twitch Hosts
Seems as tho this event was "broken", so, went through, fixed it up, and re-enabled it.  One note, viewer count according to Twitch's own references should be available, but what it says should happen doesn't.

The event does provide a `%viewers%` variable, which is best guess accurate, utilizing an API call to retrieve information.