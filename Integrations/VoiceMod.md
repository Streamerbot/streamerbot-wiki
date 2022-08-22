---
title: VoiceMod
description: Controlling VoiceMod software via Streamer.bot actions
published: true
date: 2022-08-18T19:00:49.424Z
tags: twitch, integrations, youtube, streamerbot, voicemod
editor: markdown
dateCreated: 2022-06-23T21:15:57.891Z
---

![voicemod-logo.png](/logos/voicemod.png){.align-abstopright}

# VoiceMod
With Streamer.bot *v0.1.8*{.version-badge} came with VoiceMod Integration and various actions we can use this  includes those listed below:
- Get Current Voice
- Set Random Voice
- Select Voice
- Select Voice by Id
- Set Background Effect State
- Set Censor State
- Set Hear My Voice State
- Set Mute State
- Set Voice Changer State

To do this we first need to make sure you are using Streamer.bot (v0.18 or greater) is linked to your VoiceMod.


### Connecting to VoiceMod
To do this navigate the following tabs top row of tabs click `Integrations` then on the second row of tabs click `VoiceMod`. Once you are in this tab you will see the available options `Auto Connect, Auto Reconnect ` and a button that says `Connect to VoiceMod`.  Make sure you have the VoiceMod Application open and running for it to connect successfully. If VoiceMod isn’t running, then link cannot/won’t be made.

![connect-to-voicemod.png](/voicemod/connect-to-voicemod.png){.align-center}


When Streamer.bot is connected to VoiceMod successfully you will see that the `Connect to VoiceMod` button has changed to `Disconnect from VoiceMod`. Now we are ready to use the new integration action that are available to us.


![disconnect-from-voicemod.png](/voicemod/disconnect-from-voicemod.png){.align-center}

This is it we are now ready to put the VoiceMod Integration to work.

## Available Sub-Actions

* [**Get Current Voice *Get the current selecte voice, and assign it to `%currentVoiceId%`***](/en/Sub-Actions/VoiceMod/Get-Current-Voice)
* [**Select Random Voice *Pick a random voice to use***](/en/Sub-Actions/VoiceMod/Select-Random-Voice)
* [**Select Voice *Pick a specific voice to use***](/en/Sub-Actions/VoiceMod/Select-Voice)
* [**Select Voice by Id *Pick a specific voice to use by a known id***](){.disabled}
* [**Set Background Effect State *Enable or disable the background effect of a voice***](/en/Sub-Actions/VoiceMod/Set-Background-Effect-State)
* [**Set Censor State *Enable or disable the beep tone***](/en/Sub-Actions/VoiceMod/Set-Censor-State)
* [**Set Hear My Voice State *Change whether or not you hear yourself***](/en/Sub-Actions/VoiceMod/Set-Hear-My-Voice-State)
* [**Set Mute State *Turn your mic on or off***](/en/Sub-Actions/VoiceMod/Set-Mute-State)
* [**Set Voice Changer State *Turn the voice changer on or off***](/en/Sub-Actions/VoiceMod/Set-Voice-Changer-State)
{.btn-grid .my-5}

---

- [<i class="mdi mdi-chevron-left"></i> **All Integrations *Go Back***](/en/Integrations)
{.btn-grid .my-5}