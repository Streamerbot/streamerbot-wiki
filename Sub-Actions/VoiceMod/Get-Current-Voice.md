---
title: Get Current Voice 
description: Get the Current Voice in Use via VoiceMod
published: true
date: 2022-07-04T22:49:39.839Z
tags: twitch, integrations, sub-action, voice, youtube, streamerbot, voicemod
editor: markdown
dateCreated: 2022-06-23T20:40:12.499Z
---

# Get Current Voice 

With the Streamer.bot *v0.1.8*{.version-badge} update came the VoiceMod Integration and various actions we can use. The first of the actions being **Get Current Voice** in use via VoiceMod


First make sure Streamer.bot is connected to VoiceMod (if you haven't done this and /or don't know how please check out the how to connect to VoiceMod [here](/en/Integrations/VoiceMod))
Once you have done this you can now proceed to the set up this Sub-Action.

![get-current-voice.png](/voicemod/get-current-voice.png){.align-center}

To do this navigate to the `Actions` tab, next you can either create a new action or use an existing one.
Next in the Sub-Action's pane you will need to add this sub action so to do this we `Right Click` in the Sub-Action pane next navigate the menus through the following `Add Sub-Action` the down the second menu to `VoiceMod` the click on the `Get Current Voice` action and that is it Streamer.bot will query VoiceMod to get the current VoiceMod voice you're using and assign in to `%currentVoiceId%`. 

